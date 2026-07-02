# ETL Habit Insights Pipeline

Pipeline ETL desenvolvido em Python para extrair dados de uma API REST, enriquecê-los com Inteligência Artificial Generativa e persistir as informações transformadas de volta à aplicação.

**Status**: Concluído

**Tipo de projeto**: Pipeline ETL

**Domínio**: Aplicativo de Hábitos (cenário fictício)

**Ferramenta principal**: Python

**Objetivo**: Automatizar a extração, enriquecimento e atualização de dados de usuários por meio de um pipeline ETL integrado à IA Generativa.

---

## Sobre o projeto

Aplicativos voltados ao acompanhamento de hábitos dependem da qualidade dos dados para oferecer experiências personalizadas aos usuários.

Neste projeto foi desenvolvido um pipeline ETL completo capaz de extrair informações de uma API REST, enriquecê-las automaticamente utilizando Inteligência Artificial Generativa e atualizar os registros na própria API.

O projeto simula um cenário real de engenharia de dados, demonstrando como diferentes tecnologias podem ser integradas para automatizar processos de tratamento e enriquecimento de dados.

---

## Contexto de negócio

Aplicativos de hábitos armazenam informações sobre objetivos, frequência e comportamento dos usuários. Entretanto, esses dados isoladamente oferecem pouco valor se não forem transformados em informações úteis.

Neste cenário, o pipeline automatiza a geração de recomendações personalizadas para cada usuário, agregando inteligência aos dados existentes sem necessidade de intervenção manual.

---

## Objetivo

Desenvolver um pipeline ETL que permita:

- extrair dados de usuários a partir de uma API REST;
- integrar informações provenientes de um arquivo CSV;
- enriquecer os dados utilizando Inteligência Artificial Generativa;
- atualizar automaticamente os registros na API;
- demonstrar a aplicação de boas práticas de engenharia de dados.

---

## Arquitetura do Pipeline

```text
CSV (IDs dos usuários)
        │
        ▼
Extração dos dados via API REST (GET)
        │
        ▼
Transformação com IA Generativa
(Geração de insights personalizados)
        │
        ▼
Carga dos dados enriquecidos na API (PUT)
```

---

## Capacidades do pipeline

- Extração de dados a partir de arquivo CSV
- Consumo de API REST
- Processamento de dados em JSON
- Enriquecimento de informações com IA Generativa
- Atualização automática dos registros na API
- Estrutura modular baseada nas etapas do ETL
- Separação entre Extract, Transform e Load

---

## Principais etapas

### Extract

- Leitura dos IDs dos usuários a partir de um arquivo CSV
- Consulta dos dados completos de cada usuário via API REST por meio de requisições HTTP GET
- Filtragem automática de usuários inválidos

### Transform

- Geração automática de insights personalizados utilizando GPT-4o-mini
- Enriquecimento dos registros com recomendações baseadas nos hábitos de cada usuário
- Estruturação das informações em formato JSON

### Load

- Atualização individual dos usuários na API utilizando requisições HTTP PUT
- Validação do sucesso das operações por meio dos códigos de resposta HTTP

---

## Principais resultados

- Automatização completa do fluxo ETL utilizando Python.
- Integração entre arquivo CSV, API REST e Inteligência Artificial Generativa em um único pipeline.
- Geração de recomendações personalizadas para cada usuário com base em seus hábitos e frequência semanal.
- Persistência automática dos dados enriquecidos na API, simulando um ambiente de produção.
- Organização do código em etapas independentes, favorecendo manutenção, reutilização e escalabilidade.

---

## Tecnologias utilizadas

- Python
- Pandas
- Requests
- OpenAI API
- GPT-4o-mini
- JSON
- MockAPI
- Jupyter Notebook

---

## Estrutura do projeto

```text
.
├── notebook/
│   └── projeto_etl.ipynb
├── README.md
└── LICENSE
```

---

## Como executar

1. Criar uma API utilizando o MockAPI.
2. Inserir os usuários iniciais.
3. Criar um arquivo CSV contendo os IDs dos usuários.
4. Configurar a chave da OpenAI.
5. Executar o notebook do pipeline.
6. Verificar os registros atualizados na API.

---

## Autor

**Paulo Ricardo Costa Mariano de Souza**

- GitHub: https://github.com/PauloData9
- LinkedIn: https://www.linkedin.com/in/paulo-ricardo-costa-mariano-de-souza-834585376
