<img width="1496" height="722" alt="image" src="https://github.com/user-attachments/assets/118d6ab4-0ca5-47c5-8b89-3515725d0470" /># AWS Cloud Studies & Atividades

---

## 1. Amazon S3
*Tópicos de estudo teórico e laboratórios.*

* [ ] **Managing the Lifecycle of Objects**
* [ ] **Hosting a Static Website using Amazon S3**

---

## 2. Atividade Prática: Sistema de Estabilização

> **Cenário:** Solicitação de soluções para migração do módulo computacional da infraestrutura local para a AWS.  
> **Solução Adotada:** Implantar o sistema em **duas instâncias Amazon EC2** distribuídas em **Availability Zones (AZs) distintas**.  
> **Benefício:** Aumenta a alta disponibilidade, resiliência e tolerância a falhas do sistema de estabilização da ilha aproveitando a Infraestrutura Global da AWS.

![Arquitetura da Solução](https://github.com/user-attachments/assets/2657b341-7e0c-4b94-9894-84bc379c2788)

---

## 3. Material de Apoio e Conceitos-Chave

<details>
<summary><b>1. Infraestrutura Global AWS & Alta Disponibilidade</b></summary>

> **Nota 1/6 — Visão Geral:**  
> Esta solução melhora a confiabilidade e disponibilidade do sistema de estabilização da ilha ao migrar seu módulo computacional da infraestrutura local para a Infraestrutura Global AWS.

> **Nota 3/6 — Regiões e Zonas de Disponibilidade:**  
> Uma Região AWS é um cluster geográfico de data centers. Cada Região contém três ou mais Zonas de Disponibilidade (AZs), fornecendo um acordo de nível de serviço (SLA) de 99,99%. Cada AZ consiste em um ou mais data centers discretos com energia, rede e conectividade redundantes.

> **Nota 6/6 — Resiliência Multi-AZ:**  
> Melhorias de disponibilidade são alcançadas executando o módulo computacional em instâncias EC2 separadas em várias AZs dentro da Região. As AZs são identificadas por um código de Região AWS com um identificador de letra (por exemplo, `us-east-1a`).

![AWS Global Infrastructure Benefits](https://github.com/user-attachments/assets/f89e3056-7032-410f-8d8e-2771ab523592)
</details>

<details>
<summary><b>2. Amazon EC2 (Compute, Storage & Networking)</b></summary>

> **Nota 2/6 — Visão Geral do EC2:**  
> A migração do módulo computacional usa capacidade de computação Amazon EC2 na Região Leste dos EUA (Norte da Virgínia — `us-east-1`).

* **Visão Geral:**  
  ![EC2 Overview](https://github.com/user-attachments/assets/70800b00-0a2a-41ac-9965-8248b301c8d3)

* **Armazenamento e Rede:**  
  ![EC2 Storage & Networking](https://github.com/user-attachments/assets/e3d2a043-0120-45cd-9f36-b526726c55b4)
</details>

<details>
<summary><b>3. Amazon EBS (Elastic Block Store)</b></summary>

> **Nota 4/6 — Armazenamento em Bloco:**  
> Os dados do módulo computacional residem em um volume Amazon EBS anexado à instância EC2. O Amazon EBS oferece armazenamento em bloco de alto desempenho otimizado para o Amazon EC2.

* **Visão Geral:**  
  ![Amazon EBS](https://github.com/user-attachments/assets/04469eda-a2eb-4545-86c0-b3d7126b468e)

* **Recursos e Benefícios:**  
  ![Amazon EBS Features](https://github.com/user-attachments/assets/f2e6eaa0-6e46-4653-b170-2c4f196e703d)

* **Comparativo de Tipos de Volumes:**  
  ![EBS Volume Comparison](https://github.com/user-attachments/assets/d235cdc3-a97e-4c9f-8de6-f245e00f783b)
</details>

<details>
<summary><b>4. DNS, Well-Architected & Ferramentas de Apoio</b></summary>

> **Nota 5/6 — Resolução de Nomes (DNS):**  
> O módulo é acessível através de seu endereço IP público (como `192.168.2.1`) ou nome DNS (como `example.com`).

* **Fluxo de DNS:**  
  ![DNS](https://github.com/user-attachments/assets/bf150392-69ec-4776-860a-94083477659a)

* **AWS Well-Architected Framework:**  
  ![AWS Well-Architected Overview](https://github.com/user-attachments/assets/2f822f25-7511-4a5e-94c7-9b3060efe123)

* **AWS Trusted Advisor:**  
  ![AWS Trusted Advisor](https://github.com/user-attachments/assets/d18e8d49-9496-4951-b464-66ccbfe2bec7)
</details>

---

## 4. Laboratórios Práticos

### Laboratório 1: Execução de EC2 e Configuração de User Data
* **Objetivos:**
  * Executar uma instância Amazon EC2.
  * Configurar um script de inicialização (*user data*) para instalar um servidor web e exibir os metadados da instância via HTTP (porta 80).

<details>
<summary><b>Passo a Passo e Evidências</b></summary>

#### Parâmetros e Instruções
* **Passo 1:**  
  ![Lab 1 - Instrução 1](https://github.com/user-attachments/assets/800ab2f4-8fdb-412e-a9de-cdef522d87b5)

* **Passo 2:**  
  ![Lab 1 - Instrução 2](https://github.com/user-attachments/assets/422ce896-fb06-4eb5-9d8e-a646a489f9a7)

* **Passo 3:**  
  ![Lab 1 - Instrução 3](https://github.com/user-attachments/assets/d0e31945-2256-490d-ab05-53cac5470311)

* **Passo 4 — Script de Inicialização (User Data):**  
  > Script de bootstrap para instalação do servidor web na porta 80.  
  ![Lab 1 - Script User Data](https://github.com/user-attachments/assets/b7172e7a-ee6d-4d9f-bc8e-d91774b47309)

#### Execução no Console AWS
* **Configuração da AMI e Tipo de Instância:**  
  ![Lab 1 - Etapa 1](https://github.com/user-attachments/assets/15653c37-89f6-4289-a16c-e38eff946e80)  
  ![Lab 1 - Etapa 2](https://github.com/user-attachments/assets/59193af2-553f-4dbb-848b-59313953e58d)  
  ![Lab 1 - Etapa 3](https://github.com/user-attachments/assets/c3d2cb7f-de66-4993-9d99-44e32f6ba28c)  
  ![Lab 1 - Etapa 4](https://github.com/user-attachments/assets/a78b09f3-d412-4693-9eed-10ef7b881509)  
  ![Lab 1 - Etapa 5](https://github.com/user-attachments/assets/22c8e26a-7e25-4bc0-be0c-2b39d04686fb)

* **Rede, Security Groups e Storage:**  
  ![Lab 1 - Etapa 6](https://github.com/user-attachments/assets/80c10543-21a6-46e9-abb9-004f636532fa)  
  ![Lab 1 - Etapa 7](https://github.com/user-attachments/assets/14dc6bfb-b045-43ca-90b9-a4fb9de9910d)  
  ![Lab 1 - Etapa 8](https://github.com/user-attachments/assets/6e74dae4-86e0-4b3a-8169-b846bae8db50)  
  ![Lab 1 - Etapa 9](https://github.com/user-attachments/assets/f28c37e9-e7b5-4206-93b8-dbf2debe658b)

* **Launch, Inicialização e Validação Web:**  
  ![Lab 1 - Etapa 10](https://github.com/user-attachments/assets/29c35e2a-c5a5-4170-9c75-d11be5ce6666)  
  ![Lab 1 - Etapa 11](https://github.com/user-attachments/assets/bfc1cc7d-9a3e-4ddc-938f-60321076bc7e)  
  ![Lab 1 - Etapa 12](https://github.com/user-attachments/assets/391452ab-7fd1-4c21-b629-e5973c1ba6ee)  
  ![Lab 1 - Etapa 13](https://github.com/user-attachments/assets/e57bd148-ae81-4a2a-b76b-55554740f424)  
  ![Lab 1 - Etapa 14](https://github.com/user-attachments/assets/b6f2bd3a-c310-4f72-a694-563efe068e9f)  
  ![Lab 1 - Etapa 15](https://github.com/user-attachments/assets/3dc27b99-124c-4404-b211-bc133fa4cfd8)  
  ![Lab 1 - Etapa 16](https://github.com/user-attachments/assets/98ea560c-e78e-433a-bc45-4d7294a3a527)
</details>

---

### Laboratório 2: Gerenciamento e Escalonamento de Instâncias
* **Objetivos:** Provisionamento detalhado de recursos computacionais e configuração de storage persistente.

<details>
<summary><b>Passo a Passo e Evidências</b></summary>

* **Etapa 1: Provisionamento e Seleção de Recursos**  
  ![Lab 2 - Registro 1](https://github.com/user-attachments/assets/8c730b00-48e8-4b48-a37f-1f11fdd3b075)  
  ![Lab 2 - Registro 2](https://github.com/user-attachments/assets/1f6f6606-6a5a-4335-a4b3-784e37ce9d07)  
  ![Lab 2 - Registro 3](https://github.com/user-attachments/assets/0784fb8c-d613-42e2-ada2-897a7a7c372e)  
  ![Lab 2 - Registro 4](https://github.com/user-attachments/assets/e0f2c721-8ab1-4115-a499-f819d54d5ce9)  
  ![Lab 2 - Registro 5](https://github.com/user-attachments/assets/f9ea9d0e-7259-4e6b-ace9-efb2fc97874d)  
  ![Lab 2 - Registro 6](https://github.com/user-attachments/assets/7e7b7498-6c87-43cf-8607-c858eed11ab5)

* **Etapa 2: Configurações de Rede e Volumes**  
  ![Lab 2 - Registro 7](https://github.com/user-attachments/assets/2ce5337f-68d9-4be7-b300-e886833d6dff)  
  ![Lab 2 - Registro 8](https://github.com/user-attachments/assets/83370a06-f6d0-4f19-b9f5-b5cd995df4b6)  
  ![Lab 2 - Registro 9](https://github.com/user-attachments/assets/b5374224-7160-4365-8f97-8185fc901315)  
  ![Lab 2 - Registro 10](https://github.com/user-attachments/assets/517e0270-2944-447b-ab60-a1567823c2fd)  
  ![Lab 2 - Registro 11](https://github.com/user-attachments/assets/e7d8106d-6b6f-4a4f-8673-048c2fc02e35)  
  ![Lab 2 - Registro 12](https://github.com/user-attachments/assets/bb83ba86-c9ae-42ef-b6c1-fee158d0427d)

* **Etapa 3: Regras de Firewall e Associações**  
  ![Lab 2 - Registro 13](https://github.com/user-attachments/assets/54bb9235-0352-4169-b7fc-88cebbf33827)  
  ![Lab 2 - Registro 14](https://github.com/user-attachments/assets/165338ac-9593-43c6-a396-8f222260f996)  
  ![Lab 2 - Registro 15](https://github.com/user-attachments/assets/8abb7935-6a22-4e29-b715-55bc716fc988)  
  ![Lab 2 - Registro 16](https://github.com/user-attachments/assets/5cdf6886-95f9-4ce8-9923-d7de959433b9)  
  ![Lab 2 - Registro 17](https://github.com/user-attachments/assets/b48b6c83-7be0-42f6-a51a-7de43ead6395)  
  ![Lab 2 - Registro 18](https://github.com/user-attachments/assets/0114f673-137a-4aee-b8d2-962b835959b5)

* **Etapa 4: Validação de Estado e Testes Finais**  
  ![Lab 2 - Registro 19](https://github.com/user-attachments/assets/249d6733-e7c4-4376-a7ab-6277cabff2d6)  
  ![Lab 2 - Registro 20](https://github.com/user-attachments/assets/b868c249-f375-40c7-9a34-74b1ef9b07db)  
  ![Lab 2 - Registro 21](https://github.com/user-attachments/assets/db6a1077-ccea-423d-8487-b5e81a0d5cad)  
  ![Lab 2 - Registro 22](https://github.com/user-attachments/assets/8af766fc-b672-4f39-bc2c-6aa24a0bbecc)  
  ![Lab 2 - Registro 23](https://github.com/user-attachments/assets/ec9d2d06-27c8-4e21-b32b-f5634a9dc229)  
  ![Lab 2 - Registro 24](https://github.com/user-attachments/assets/20ee7f33-7ef2-4b6c-b5e9-7a3a9f48c14a)
</details>

---

### Laboratório 3: Redes e Conectividade entre Aplicações (VPC)
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


ATV 4 CAlcauladora de stimageiva de uso AWS:


<img width="1762" height="991" alt="screenshot_20261003144223" src="https://github.com/user-attachments/assets/89d9dba9-f9d6-41b1-944f-a3d265791871" />

ATV5:
BANCO DE DADOS NA PRATICA

A seguradora deseja ajudar seus administradores de
anco de dados a gastar menos tempo em tarefas
operacionais, como aplicacao de patches e
gerenciamento de infraestrutura de banco de dados.
Eles tambem desejam uma solucao que melhore a
disponibilidade e eficiência do banco de dados.

OBJETIVOS DE APRENDIZADO

Crie uma instancia de banco de dados Amazon
RDS.

/ Habilite backups em seu banco de dados.

/ Habilite varias AZs para sua implantação do
Amazon RDS.

/ Crie uma réplica de leitura do Amazon RDS.

<img width="1035" height="538" alt="image" src="https://github.com/user-attachments/assets/e08f9c0e-d74f-441d-9b32-aabb4362dfed" />

A alta disponibilidade é alcançada através
da implantação Multi-AZ, onde o Amazon
RDS replica sincronamente dados da
instância primária para uma instância
standby em uma AZ diferente.

<img width="1103" height="592" alt="image" src="https://github.com/user-attachments/assets/7ebb1bb9-0e53-46fa-a245-f0fcbb123337" />

Durante falhas da instância primária, o
Amazon RDS automaticamente realiza
failover para a instância standby e
redireciona solicitações sem intervenção
manual.



<img width="1046" height="557" alt="image" src="https://github.com/user-attachments/assets/04adc9ae-4641-4756-989c-d746c617ffa7" />

O registro do nome DNS da instancia do
banco de dados permanece inalterado
durante o failover, fornecendo
recuperação automática da aplicação sem
ação administrativa.

Pratica:
<img width="1517" height="719" alt="image" src="https://github.com/user-attachments/assets/3629aaa4-44e1-49bd-9793-a4380fb980a7" />
<img width="1521" height="744" alt="image" src="https://github.com/user-attachments/assets/1b115d54-cd48-48b0-8571-29aa512662c3" />
<img width="1544" height="761" alt="image" src="https://github.com/user-attachments/assets/5dbedca0-402a-4392-b82a-879b4ce6f55e" />
<img width="1525" height="740" alt="image" src="https://github.com/user-attachments/assets/cfc89a47-cb79-4fc8-ab98-55d4f852d597" />
<img width="1513" height="742" alt="image" src="https://github.com/user-attachments/assets/d609099e-997c-4d19-bf95-43f04ae69021" />
<img width="1517" height="737" alt="image" src="https://github.com/user-attachments/assets/6eb25b67-bf19-465e-9f70-72d6a38b452a" />
<img width="1504" height="720" alt="image" src="https://github.com/user-attachments/assets/d1117857-1492-4e17-a4b0-891a0064afd4" />
<img width="1529" height="782" alt="image" src="https://github.com/user-attachments/assets/d7e34597-9766-4ffe-b033-39381f837f45" />
<img width="1513" height="747" alt="image" src="https://github.com/user-attachments/assets/3623b4c7-6ba0-42bd-ae42-262825589298" />
<img width="1517" height="748" alt="image" src="https://github.com/user-attachments/assets/8cd04845-af97-4eb2-9123-d37563763f42" />
<img width="1510" height="726" alt="image" src="https://github.com/user-attachments/assets/f9f95d1b-6d30-4761-8f40-8c056b98aab4" />
<img width="1504" height="735" alt="image" src="https://github.com/user-attachments/assets/01a99457-83a1-4550-aa7f-86ea232a741e" />
<img width="1510" height="736" alt="image" src="https://github.com/user-attachments/assets/c2c59e26-6265-40f1-80a5-5d4a43488158" />
<img width="1510" height="728" alt="image" src="https://github.com/user-attachments/assets/ea7ccf88-bdfe-47cf-9a7d-090742c02168" />
<img width="1550" height="796" alt="image" src="https://github.com/user-attachments/assets/2f69acfb-d7b2-4561-b21a-170d3e51a96a" />
<img width="1515" height="738" alt="image" src="https://github.com/user-attachments/assets/9228b31e-1a23-47e6-a06f-1ec8fc7dfee3" />
<img width="1511" height="760" alt="image" src="https://github.com/user-attachments/assets/528d50e5-6b8d-47e7-87be-f5268592524e" />
<img width="1490" height="737" alt="image" src="https://github.com/user-attachments/assets/8c35bfe7-fa87-4ad3-9444-234b3189ca42" />
<img width="1528" height="750" alt="image" src="https://github.com/user-attachments/assets/083a7021-cd80-4577-8ad2-6d27920a3a63" />
<img width="1505" height="719" alt="image" src="https://github.com/user-attachments/assets/9548c6ae-82a9-442a-8c14-843f15e5ef36" />
<img width="1522" height="725" alt="image" src="https://github.com/user-attachments/assets/144ff5ca-a9af-4621-bdce-7d66d313488c" />




ATV 6
Implemente o Amazon DynamoDB para armazenar e processar dados de comportamento do espectador, incluindo consumo de conteúdo e análise de dispositivos.

Esta solução implementa o Amazon DynamoDB para capturar e armazenar históricos de visualização de conteúdo em streaming.
<img width="961" height="712" alt="image" src="https://github.com/user-attachments/assets/2c2a8f70-5eb0-4f21-8991-9c082bc9832c" />
Conceito

Neste laboratório prático, você vai:
- Criar um banco de dados NoSQL como uma tabela do Amazon DynamoDB.
- Adicionar registros, com esquema dinâmico, à tabela do DynamoDB.
- Consultar a tabela do DynamoDB.

Objetivos do laboratório
- Crie um banco de dados NoSQL como uma tabela do Amazon DynamoDB.
- Adicione registros, com esquema dinâmico, à tabela do DynamoDB.
- Consulte a tabela do DynamoDB.

<img width="1062" height="735" alt="image" src="https://github.com/user-attachments/assets/d94fd0b9-af84-4629-9eb8-fae93d112cd6" />
<img width="1022" height="692" alt="image" src="https://github.com/user-attachments/assets/d219739d-fd3b-47cf-851f-498e830f2001" />
<img width="1050" height="728" alt="image" src="https://github.com/user-attachments/assets/bb92bdf0-1327-4630-94f6-103ad658b849" />
<img width="1041" height="722" alt="image" src="https://github.com/user-attachments/assets/69429900-6298-41f6-a8be-6fc0c779a9be" />
<img width="1046" height="716" alt="image" src="https://github.com/user-attachments/assets/3461a9ce-f7b1-4ad5-971e-681f82f068ce" />
<img width="1510" height="720" alt="image" src="https://github.com/user-attachments/assets/9d417bd7-c0e4-49ea-ac0d-d14b71e3bc70" />
<img width="1496" height="722" alt="image" src="https://github.com/user-attachments/assets/34e75bdc-7d78-4dd5-a787-4dc44b31141e" />
<img width="1509" height="742" alt="image" src="https://github.com/user-attachments/assets/130df1dd-b61b-4ada-b745-c702ecc8caa4" />
<img width="1047" height="713" alt="image" src="https://github.com/user-attachments/assets/6d2c17ad-0e44-4282-90b1-a150a5fc31e9" />
<img width="1504" height="723" alt="image" src="https://github.com/user-attachments/assets/e52cf35d-95c3-4423-a199-31015c1ef41c" />
<img width="1502" height="734" alt="image" src="https://github.com/user-attachments/assets/da74ba76-fe51-4ca3-bb80-58f56c78c25b" />
<img width="1489" height="724" alt="image" src="https://github.com/user-attachments/assets/b7415f1b-60f6-4d15-bd25-e35b7476de21" />
<img width="1503" height="718" alt="image" src="https://github.com/user-attachments/assets/1ac09594-5547-4c48-a08d-2c90fe4abfd8" />
<img width="1496" height="724" alt="image" src="https://github.com/user-attachments/assets/f61976db-fcfe-4ce6-bd05-f9d43ea5f9ff" />
<img width="1495" height="738" alt="image" src="https://github.com/user-attachments/assets/acef6d7d-1169-4a7a-844e-393ddb83b626" />
<img width="1499" height="728" alt="image" src="https://github.com/user-attachments/assets/5967d461-7295-4059-acf4-f78a0803f29e" />
<img width="1507" height="734" alt="image" src="https://github.com/user-attachments/assets/85eef6f1-1a24-431f-a474-10a72ccb835a" />
<img width="1509" height="773" alt="image" src="https://github.com/user-attachments/assets/3a17aac5-50fa-4e9e-ab7b-a710337f5322" />
<img width="1507" height="756" alt="image" src="https://github.com/user-attachments/assets/ea72f935-113d-4eda-b8be-05f5020e3235" />
<img width="1509" height="732" alt="image" src="https://github.com/user-attachments/assets/b994acd3-4b4b-4f6b-aa7e-b99fcd293484" />
<img width="1506" height="764" alt="image" src="https://github.com/user-attachments/assets/52bff293-88a7-4585-ac4f-151d747c7eb3" />
<img width="1505" height="743" alt="image" src="https://github.com/user-attachments/assets/b5f8809c-7be7-4d23-a9c6-3daca84990ce" />
<img width="1762" height="991" alt="screenshot_20261009061033" src="https://github.com/user-attachments/assets/7a805257-5cf4-43c6-ac17-f0d234eda5b8" />




