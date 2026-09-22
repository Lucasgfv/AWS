# AWS Cloud Studies & Atividades

---

## 1. Amazon S3
*Tópicos de estudo teórico e laboratórios.*

* [ ] **Managing the Lifecycle of Objects**
* [ ] **Hosting a Static Website using Amazon S3**

---

## 2. Atividade Prática: Sistema de Estabilização

> **Cenário:** Solicitação de soluções para migração do módulo computacional da infraestrutura local para a AWS.
> 
> **Solução Adotada:** Implantar o sistema em **duas instâncias Amazon EC2** distribuídas em **Availability Zones (AZs) distintas**.
> 
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


ATV S3  
Objetivos do laboratório
- Executar uma instância do Amazon EC2.
- Configure um script de dados do usuário para exibir os detalhes da instância em um navegador.


<img width="858" height="613" alt="image" src="https://github.com/user-attachments/assets/800ab2f4-8fdb-412e-a9de-cdef522d87b5" />

P2

<img width="843" height="581" alt="image" src="https://github.com/user-attachments/assets/422ce896-fb06-4eb5-9d8e-a646a489f9a7" />

p3
<img width="847" height="585" alt="image" src="https://github.com/user-attachments/assets/d0e31945-2256-490d-ab05-53cac5470311" />

p4 (1. Na nova guia do navegador, revise o conteúdo do arquivo.
- Este script instala um servidor web que exibe informações da instância na porta 80.
- Observe que o bloco de código em seu arquivo pode ser maior do que o mostrado no exemplo da captura de te)


<img width="838" height="573" alt="image" src="https://github.com/user-attachments/assets/b7172e7a-ee6d-4d9f-bc8e-d91774b47309" />


<img width="1229" height="644" alt="image" src="https://github.com/user-attachments/assets/15653c37-89f6-4289-a16c-e38eff946e80" />

<img width="1211" height="601" alt="image" src="https://github.com/user-attachments/assets/59193af2-553f-4dbb-848b-59313953e58d" />

<img width="1220" height="599" alt="image" src="https://github.com/user-attachments/assets/c3d2cb7f-de66-4993-9d99-44e32f6ba28c" />

<img width="1227" height="588" alt="image" src="https://github.com/user-attachments/assets/a78b09f3-d412-4693-9eed-10ef7b881509" />

<img width="1217" height="588" alt="image" src="https://github.com/user-attachments/assets/22c8e26a-7e25-4bc0-be0c-2b39d04686fb" />

<img width="1206" height="576" alt="image" src="https://github.com/user-attachments/assets/80c10543-21a6-46e9-abb9-004f636532fa" />

<img width="1219" height="611" alt="image" src="https://github.com/user-attachments/assets/14dc6bfb-b045-43ca-90b9-a4fb9de9910d" />

<img width="1225" height="594" alt="image" src="https://github.com/user-attachments/assets/6e74dae4-86e0-4b3a-8169-b846bae8db50" />

<img width="1203" height="581" alt="image" src="https://github.com/user-attachments/assets/f28c37e9-e7b5-4206-93b8-dbf2debe658b" />

<img width="1230" height="634" alt="image" src="https://github.com/user-attachments/assets/29c35e2a-c5a5-4170-9c75-d11be5ce6666" />

<img width="1205" height="580" alt="image" src="https://github.com/user-attachments/assets/bfc1cc7d-9a3e-4ddc-938f-60321076bc7e" />

<img width="1213" height="586" alt="image" src="https://github.com/user-attachments/assets/391452ab-7fd1-4c21-b629-e5973c1ba6ee" />

<img width="1215" height="590" alt="image" src="https://github.com/user-attachments/assets/e57bd148-ae81-4a2a-b76b-55554740f424" />

<img width="1206" height="573" alt="image" src="https://github.com/user-attachments/assets/b6f2bd3a-c310-4f72-a694-563efe068e9f" />

<img width="1207" height="595" alt="image" src="https://github.com/user-attachments/assets/3dc27b99-124c-4404-b211-bc133fa4cfd8" />

<img width="1235" height="636" alt="image" src="https://github.com/user-attachments/assets/98ea560c-e78e-433a-bc45-4d7294a3a527" />




