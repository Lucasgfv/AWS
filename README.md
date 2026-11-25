# Estudos e laboratórios AWS

Repositório de estudos práticos sobre Amazon Web Services, com fundamentos, arquiteturas e registros de laboratórios realizados no Console AWS.

> **Atenção a custos e segurança:** alguns laboratórios criam recursos que podem gerar cobrança. Use dados fictícios, aplique o princípio do menor privilégio e exclua os recursos quando terminar.

## Conteúdo

| Área | Conteúdo |
|---|---|
| Fundamentos | [Infraestrutura global, alta disponibilidade, EC2, EBS, DNS e Well-Architected](docs/fundamentos.md) |
| Laboratório 1 | [Amazon EC2 e inicialização com User Data](laboratorios/01-ec2-user-data/README.md) |
| Laboratório 2 | [Gerenciamento de instâncias EC2 e volumes EBS](laboratorios/02-ec2-ebs/README.md) |
| Laboratório 3 | [Amazon VPC, sub-redes, rotas e Security Groups](laboratorios/03-vpc-security-groups/README.md) |
| Laboratório 4 | [Estimativa de custos com AWS Pricing Calculator](laboratorios/04-estimativa-de-custos/README.md) |
| Laboratório 5 | [Amazon RDS, backups, Multi-AZ e réplica de leitura](laboratorios/05-rds/README.md) |
| Laboratório 6 | [Amazon DynamoDB](laboratorios/06-dynamodb/README.md) |

Consulte também o [índice completo](docs/INDICE.md).

## Estrutura

```text
AWS/
├── README.md
├── CONTRIBUTING.md
├── SECURITY.md
├── docs/
│   ├── INDICE.md
│   └── fundamentos.md
├── laboratorios/
│   ├── 01-ec2-user-data/
│   ├── 02-ec2-ebs/
│   ├── 03-vpc-security-groups/
│   ├── 04-estimativa-de-custos/
│   ├── 05-rds/
│   └── 06-dynamodb/
└── arquivo-original/
```

## Serviços abordados

- Amazon EC2 e User Data;
- Amazon EBS;
- Amazon VPC, sub-redes, tabelas de rotas e Security Groups;
- AWS Pricing Calculator;
- Amazon RDS, backups, Multi-AZ e réplicas de leitura;
- Amazon DynamoDB;
- infraestrutura global, DNS e AWS Well-Architected Framework.

## Como estudar por este repositório

1. Comece pelos [fundamentos](docs/fundamentos.md).
2. Siga os laboratórios na ordem numérica.
3. Antes de criar recursos, verifique a Região e a estimativa de custos.
4. Registre como validou o resultado de cada atividade.
5. Exclua recursos que não serão mais usados e confirme que deixaram de gerar cobrança.

## Segurança

Não publique chaves, tokens, arquivos de credenciais, estados do Terraform ou capturas com dados sensíveis. Veja a [política de segurança](SECURITY.md).

## Contribuições

Consulte [CONTRIBUTING.md](CONTRIBUTING.md) para manter a mesma organização nos próximos conteúdos.

## Material anterior

O conteúdo anterior foi preservado em [`arquivo-original/`](arquivo-original/) para manter as anotações e evidências sem perda de informação durante a reorganização.

ATV 07:
<img width="1442" height="811" alt="screenshot_20261124205951" src="https://github.com/user-attachments/assets/6d7e55d5-fbe3-4789-a3c2-ec05cf759943" />
<img width="1184" height="570" alt="image" src="https://github.com/user-attachments/assets/84cdda39-2fe9-4bc7-a5b7-bb9acd543816" />

ATV 8
<img width="1442" height="811" alt="screenshot_20261124213537" src="https://github.com/user-attachments/assets/d87be176-21ad-4c2d-aff5-f5894e876aa9" />
<img width="1074" height="593" alt="image" src="https://github.com/user-attachments/assets/ec9170b0-f01e-4d3b-9798-3834c8504388" />
