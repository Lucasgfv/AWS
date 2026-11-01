# Laboratório 5 — Amazon RDS: Multi-AZ, backups e réplica de leitura
Bbanco de dados NA PRATICA

A seguradora deseja ajudar seus administradores de
banco de dados a gastar menos tempo em tarefas
operacionais, como aplicacao de patches e
gerenciamento de infraestrutura de bbanco de dados.
Eles tambem desejam uma solucao que melhore a
disponibilidade e eficiência do bbanco de dados.

OBJETIVOS DE APRENDIZADO

Crie uma instancia de bbanco de dados Amazon
RDS.

- Habilite backups em seu bbanco de dados.

- Habilite varias AZs para sua implantação do
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
bbanco de dados permanece inalterado
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