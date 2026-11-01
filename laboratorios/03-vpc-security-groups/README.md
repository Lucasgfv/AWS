# Laboratório 3: Redes e Conectividade entre Aplicações (VPC)
* **Objetivos:** Estruturação de topologia de rede isolada, subnets públicas/privadas, tabelas de rotas e conectividade entre aplicações.

<details>
<summary><b>Passo a Passo e Evidências</b></summary>

* **Etapa 1: Definição de VPC e Subnets**  
  ![Lab 3 - Registro 1](https://github.com/user-attachments/assets/0bfc6a2d-52f3-4f4c-8293-5e2c3d4f50fe)  
  ![Lab 3 - Registro 2](https://github.com/user-attachments/assets/d51f958c-5ed3-46e2-b496-1afa548cafd3)  
  ![Lab 3 - Registro 3](https://github.com/user-attachments/assets/eea8173b-55ba-4f56-817d-b6a920091e49)  
  ![Lab 3 - Registro 4](https://github.com/user-attachments/assets/f78a8844-8dff-4aff-b633-94aba8d4f055)  
  ![Lab 3 - Registro 5](https://github.com/user-attachments/assets/ae85ab4f-567c-4227-a355-5a1af8a22221)  
  ![Lab 3 - Registro 6](https://github.com/user-attachments/assets/57e36573-eeb1-4722-a3d1-7612acc8fa85)  
  ![Lab 3 - Registro 7](https://github.com/user-attachments/assets/060b1b5f-1ec5-4932-90d2-35711bd292de)

* **Etapa 2: Internet Gateways e Tabelas de Roteamento**  
  ![Lab 3 - Registro 8](https://github.com/user-attachments/assets/de0486e7-902f-4f28-b335-eb83c417959f)  
  ![Lab 3 - Registro 9](https://github.com/user-attachments/assets/35044a21-f9b6-4cef-aad8-0f975c414f5c)  
  ![Lab 3 - Registro 10](https://github.com/user-attachments/assets/f29a1dad-14bb-49d2-af29-1baa7b683ce0)  
  ![Lab 3 - Registro 11](https://github.com/user-attachments/assets/b5715da2-72f1-4e75-9d8a-6569deec9658)  
  ![Lab 3 - Registro 12](https://github.com/user-attachments/assets/93dcf13d-2740-4510-8a71-ce0c02de0deb)  
  ![Lab 3 - Registro 13](https://github.com/user-attachments/assets/c3dce96b-9ba3-4b14-a8f7-44c2a8815eb4)  
  ![Lab 3 - Registro 14](https://github.com/user-attachments/assets/c3104707-0417-488d-8503-ddeaff8dbb0d)

* **Etapa 3: Associação de Recursos e Testes de Conectividade**  
  ![Lab 3 - Registro 15](https://github.com/user-attachments/assets/ffd87440-7e37-44e6-97e5-ac450f4595f2)  
  ![Lab 3 - Registro 16](https://github.com/user-attachments/assets/ed973600-8090-4d5a-b19b-979988c4bff4)  
  ![Lab 3 - Registro 17](https://github.com/user-attachments/assets/624ae9ad-4f55-4bfe-868d-900fcf6ef94f)  
  ![Lab 3 - Registro 18](https://github.com/user-attachments/assets/2e5c4496-3a7d-4b71-b283-005603670266)  
  ![Lab 3 - Registro 19](https://github.com/user-attachments/assets/48a68f4e-deef-4a40-954a-2acdcfbd94d0)  
  ![Lab 3 - Registro 20](https://github.com/user-attachments/assets/703c10d2-34f6-4b66-a644-bfe95e568231)  
  ![Lab 3 - Registro 21](https://github.com/user-attachments/assets/7c4f8a03-4bba-4d3e-844b-e4abd13d0fe8)
</details>

### Resumo Prático: Configuração de Security Groups entre Camadas (Web → BD)
<img width="1764" height="992" alt="screenshot_20260926153229" src="https://github.com/user-attachments/assets/b706873d-f7f0-4e69-8e2b-51e13a868659" />

#### 1. Conceito Principal

* **Comunicação Segura:** Para ligar servidores em sub-redes distintas (ex.: Web Server e Database Server), a melhor prática na AWS é referenciar o **Security Group de origem** em vez de usar endereços IP estáticos ou redes abertas (`0.0.0.0/0`).


* **Stateful (Com monitorização de estado):** Os Security Groups da AWS guardam o estado da sessão. Ao permitir a entrada no banco de dados, o tráfego de resposta é autorizado automaticamente, desde que a saída do servidor web mantenha as configurações padrão.

---

#### 2. Passo a Passo de Configuração

1. **Identificação dos Grupos:**
* Obter o ID do grupo de origem: `WebServerSecurityGroup` (ex.: `sg-03bf...`).


* Localizar o grupo de destino: `DbServerSecurityGroup` (ex.: `sg-01aa...`).




2. **Edição das Regras de Entrada (*Inbound Rules*):**
* Aceder a **VPC** > **Grupos de segurança** e selecionar o grupo de base de dados (`DbServerSecurityGroup`).


* Clicar no separador **Regras de entrada** e depois em **Editar regras de entrada**.




3. **Criação da Regra:**
* **Tipo:** `MYSQL/Aurora` (protocolo TCP, porta `3306`).


* **Origem (*Source*):** Selecionar `Personalizado` (*Custom*), digitar as letras iniciais do ID (ex.: `sg-03bf`) e clicar obrigatoriamente na sugestão apresentada pelo menu suspenso.


* Salvar as alterações em **Salvar regras**.





---

#### 3. Erros Comuns e Como Resolver

* **Erro de conversão de regra (CIDR vs SG):** A AWS não permite editar uma regra já gravada com IP/CIDR (ex.: `0.0.0.0/0`) para transformá-la diretamente numa referência a outro grupo de segurança (`sg-...`).


* *Solução:* Excluir a linha antiga com erro e clicar em **Adicionar regra** para configurar a linha do zero.




* **Seleção do Security Group:** Apenas colar o texto do ID não conclui o vínculo. É indispensável clicar na etiqueta sugerida pela consola para que a AWS vincule o ID corretamente.


* **Validações de Laboratório:** Ao submeter relatórios ou testes de avaliação, garantir a inserção exata do nome do grupo de destino solicitado (`DbServerSecurityGroup`), evitando preencher com a descrição de outro recurso.