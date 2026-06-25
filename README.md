# 📌 **Pipeline ETL com IA Generativa — App de Hábitos**

## 📖 **Visão Geral**
Este projeto implementa um **pipeline ETL** **(Extract, Transform, Load)** completo, simulando o funcionamento de um **aplicativo de hábitos pessoais**.

A solução integra dados provenientes de uma API REST, realiza o **enriquecimento dessas informações com Inteligência Artificial Generativa** e carrega os dados transformados de volta para a API.

O objetivo é demonstrar, de forma prática, como pipelines de dados podem ser estruturados em cenários reais, combinando **engenharia de dados**, **consumo de APIs** e **IA aplicada**.

---

## 🎯 **Contexto do Problema**
Aplicativos de hábitos dependem de dados comportamentais para fornecer recomendações personalizadas aos usuários.

Neste projeto, cada usuário possui informações como:

- hábito principal
- frequência semanal
- objetivo pessoal

A partir desses dados, um modelo de linguagem é utilizado para gerar **insights personalizados**, simulando recomendações inteligentes dentro do aplicativo.

---

## 🏗️ **Arquitetura do Pipeline ETL**
🔹 **Etapa 1 — Extract (CSV)**

- Leitura de um arquivo CSV contendo os IDs dos usuários
- Conversão dos IDs para uma lista Python
- Validação inicial dos dados de entrada

🔹 **Etapa 2 — Extract (API)**

- Consulta dos dados completos de cada usuário via API REST
- Requisições HTTP GET utilizando os IDs do CSV
- Filtragem automática de usuários inválidos

🔹 **Etapa 3 — Transform**

- Enriquecimento dos dados com IA generativa
- Geração de insights personalizados com base:
	- no hábito principal
	- na frequência semanal
- Inserção estruturada dos insights no objeto do usuário

🔹 **Etapa 4 — Load**

- Persistência dos dados enriquecidos na API
- Atualização individual de cada usuário via requisição HTTP PUT
- Validação do sucesso da operação por código de status HTTP

---

## 🔄 **Fluxo do Pipeline**

CSV (IDs)

  ↓

API (GET usuários)

  ↓

IA Generativa (insights personalizados)

  ↓

API (PUT usuários enriquecidos)

---

## 🛠️ **Ferramentas Utilizadas**
- **Python**
- **Pandas** — leitura e manipulação de CSV
- **Requests** — consumo de API REST
- **OpenAI API** — geração de insights com IA
- **JSON** — estrutura de dados
- **MockAPI** — simulação de backend

---

## 🧠 **Decisões Técnicas**
- A separação clara das etapas do ETL melhora a legibilidade e a manutenção do código.
- O uso de funções pequenas e reutilizáveis facilita testes e evolução futura do pipeline.
- A transformação com IA foi mantida independente da etapa de Load, seguindo boas práticas de engenharia de dados.
- O domínio do problema foi adaptado para um contexto não bancário, garantindo originalidade em relação a exemplos acadêmicos.

---

## 📌 **Exemplo de Dado Enriquecido**
{

 "id": "1",

 "name": "Paulo",

 "primary\_habit": "Exercício físico",

 "frequency\_per\_week": 3,

 "goal": "Criar consistência",

 "insights": \[

   {

     "habit": "Exercício físico",

     "message": "Defina dias fixos e trate o treino como compromisso.",

     "frequency\_per\_week": 3

   }

 ]

}

---

## 🚀 **Como Executar o Projeto**
- Criar uma API no MockAPI com o schema de usuários
- Inserir usuários iniciais e obter seus IDs
- Criar um arquivo CSV contendo os IDs
- Executar o pipeline ETL em Python
- Verificar os usuários atualizados na API

---

## 📈 **Possíveis Evoluções**
- Adicionar timestamps aos insights gerados
- Implementar controle de erro e retentativas
- Salvar logs do pipeline
- Expandir para múltiplos hábitos por usuário
- Armazenar histórico de insights

---

## 🧾 **Conclusão**
Este projeto demonstra a construção de um pipeline ETL funcional e realista, integrando dados estruturados, APIs REST e Inteligência Artificial generativa.

A abordagem adotada reflete práticas utilizadas em ambientes profissionais de dados, com foco em clareza, modularização e aplicabilidade prática.




