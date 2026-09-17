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
