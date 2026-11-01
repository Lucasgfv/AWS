# Laboratório 6 — Amazon DynamoDB
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