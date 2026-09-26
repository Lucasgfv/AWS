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



ATV 2:
<img width="1487" height="722" alt="image" src="https://github.com/user-attachments/assets/8c730b00-48e8-4b48-a37f-1f11fdd3b075" />

<img width="1409" height="698" alt="image" src="https://github.com/user-attachments/assets/1f6f6606-6a5a-4335-a4b3-784e37ce9d07" />

<img width="1533" height="784" alt="image" src="https://github.com/user-attachments/assets/0784fb8c-d613-42e2-ada2-897a7a7c372e" />

<img width="1447" height="698" alt="image" src="https://github.com/user-attachments/assets/e0f2c721-8ab1-4115-a499-f819d54d5ce9" />

<img width="1504" height="724" alt="image" src="https://github.com/user-attachments/assets/f9ea9d0e-7259-4e6b-ace9-efb2fc97874d" />

<img width="1501" height="727" alt="image" src="https://github.com/user-attachments/assets/7e7b7498-6c87-43cf-8607-c858eed11ab5" />

<img width="1509" height="728" alt="image" src="https://github.com/user-attachments/assets/2ce5337f-68d9-4be7-b300-e886833d6dff" />

<img width="1516" height="784" alt="image" src="https://github.com/user-attachments/assets/83370a06-f6d0-4f19-b9f5-b5cd995df4b6" />

<img width="1500" height="727" alt="image" src="https://github.com/user-attachments/assets/b5374224-7160-4365-8f97-8185fc901315" />

<img width="1509" height="740" alt="image" src="https://github.com/user-attachments/assets/517e0270-2944-447b-ab60-a1567823c2fd" />

<img width="1507" height="724" alt="image" src="https://github.com/user-attachments/assets/e7d8106d-6b6f-4a4f-8673-048c2fc02e35" />

<img width="1507" height="726" alt="image" src="https://github.com/user-attachments/assets/bb83ba86-c9ae-42ef-b6c1-fee158d0427d" />

<img width="1509" height="721" alt="image" src="https://github.com/user-attachments/assets/54bb9235-0352-4169-b7fc-88cebbf33827" />

<img width="1511" height="738" alt="image" src="https://github.com/user-attachments/assets/165338ac-9593-43c6-a396-8f222260f996" />

<img width="1495" height="770" alt="image" src="https://github.com/user-attachments/assets/8abb7935-6a22-4e29-b715-55bc716fc988" />

<img width="1504" height="727" alt="image" src="https://github.com/user-attachments/assets/5cdf6886-95f9-4ce8-9923-d7de959433b9" />

<img width="1510" height="730" alt="image" src="https://github.com/user-attachments/assets/b48b6c83-7be0-42f6-a51a-7de43ead6395" />

<img width="1515" height="744" alt="image" src="https://github.com/user-attachments/assets/0114f673-137a-4aee-b8d2-962b835959b5" />

<img width="1509" height="738" alt="image" src="https://github.com/user-attachments/assets/249d6733-e7c4-4376-a7ab-6277cabff2d6" />

<img width="1502" height="722" alt="image" src="https://github.com/user-attachments/assets/b868c249-f375-40c7-9a34-74b1ef9b07db" />

<img width="1524" height="783" alt="image" src="https://github.com/user-attachments/assets/db6a1077-ccea-423d-8487-b5e81a0d5cad" />

<img width="1514" height="769" alt="image" src="https://github.com/user-attachments/assets/8af766fc-b672-4f39-bc2c-6aa24a0bbecc" />

<img width="1517" height="741" alt="image" src="https://github.com/user-attachments/assets/ec9d2d06-27c8-4e21-b32b-f5634a9dc229" />

<img width="1503" height="725" alt="image" src="https://github.com/user-attachments/assets/20ee7f33-7ef2-4b6c-b5e9-7a3a9f48c14a" />

ATV 3

Conceito de rede, conectividade entre aplicacoes diferentes / vpc

<img width="1392" height="748" alt="image" src="https://github.com/user-attachments/assets/0bfc6a2d-52f3-4f4c-8293-5e2c3d4f50fe" />

<img width="1397" height="702" alt="image" src="https://github.com/user-attachments/assets/d51f958c-5ed3-46e2-b496-1afa548cafd3" />

<img width="1406" height="673" alt="image" src="https://github.com/user-attachments/assets/eea8173b-55ba-4f56-817d-b6a920091e49" />

<img width="1383" height="666" alt="image" src="https://github.com/user-attachments/assets/f78a8844-8dff-4aff-b633-94aba8d4f055" />

<img width="1387" height="666" alt="image" src="https://github.com/user-attachments/assets/ae85ab4f-567c-4227-a355-5a1af8a22221" />

<img width="1397" height="672" alt="image" src="https://github.com/user-attachments/assets/57e36573-eeb1-4722-a3d1-7612acc8fa85" />

<img width="1392" height="685" alt="image" src="https://github.com/user-attachments/assets/060b1b5f-1ec5-4932-90d2-35711bd292de" />

<img width="1372" height="666" alt="image" src="https://github.com/user-attachments/assets/de0486e7-902f-4f28-b335-eb83c417959f" />

<img width="1376" height="676" alt="image" src="https://github.com/user-attachments/assets/35044a21-f9b6-4cef-aad8-0f975c414f5c" />

<img width="1378" height="661" alt="image" src="https://github.com/user-attachments/assets/f29a1dad-14bb-49d2-af29-1baa7b683ce0" />

<img width="1373" height="665" alt="image" src="https://github.com/user-attachments/assets/b5715da2-72f1-4e75-9d8a-6569deec9658" />

<img width="1378" height="660" alt="image" src="https://github.com/user-attachments/assets/93dcf13d-2740-4510-8a71-ce0c02de0deb" />

<img width="1376" height="670" alt="image" src="https://github.com/user-attachments/assets/c3dce96b-9ba3-4b14-a8f7-44c2a8815eb4" />

<img width="1412" height="697" alt="image" src="https://github.com/user-attachments/assets/c3104707-0417-488d-8503-ddeaff8dbb0d" />

<img width="1402" height="667" alt="image" src="https://github.com/user-attachments/assets/ffd87440-7e37-44e6-97e5-ac450f4595f2" />

<img width="1382" height="657" alt="image" src="https://github.com/user-attachments/assets/ed973600-8090-4d5a-b19b-979988c4bff4" />

<img width="1405" height="676" alt="image" src="https://github.com/user-attachments/assets/624ae9ad-4f55-4bfe-868d-900fcf6ef94f" />

<img width="1390" height="675" alt="image" src="https://github.com/user-attachments/assets/2e5c4496-3a7d-4b71-b283-005603670266" />

<img width="1378" height="666" alt="image" src="https://github.com/user-attachments/assets/48a68f4e-deef-4a40-954a-2acdcfbd94d0" />

<img width="1392" height="671" alt="image" src="https://github.com/user-attachments/assets/703c10d2-34f6-4b66-a644-bfe95e568231" />

<img width="1390" height="696" alt="image" src="https://github.com/user-attachments/assets/7c4f8a03-4bba-4d3e-844b-e4abd13d0fe8" />










