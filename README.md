# 🧪 Testes de Performance - API Banco

## 📌 Introdução

Este repositório contém testes de performance desenvolvidos em JavaScript utilizando o **k6**, com o objetivo de avaliar o comportamento de uma API bancária sob diferentes condições de carga.

Os testes foram implementados utilizando a **API do Banco do Júlio de Lima**, amplamente utilizada para fins educacionais e prática de testes de software.

Os cenários cobrem fluxos essenciais da aplicação, como autenticação e transferências entre contas, garantindo que a API responda de forma eficiente, estável e confiável.

---

## 🚀 Tecnologias Utilizadas

- JavaScript
- k6 (ferramenta de testes de performance)
- Node.js

---

## 📂 Estrutura do Repositório

```
├── tests/
│   ├── login.test.js
│   └── transferencias.test.js
├── helpers/
│   └── autenticacao.js
├── fixtures/
├── config/
├── utils/
└── README.md
```

---

## 🧩 Objetivo de cada grupo de arquivos

### 📁 tests/
Contém os scripts de testes de performance executados pelo k6.

- `login.test.js`: valida o endpoint de autenticação  
- `transferencias.test.js`: testa o fluxo de transferências entre contas  

---

### 📁 helpers/
Responsável por funções auxiliares reutilizáveis.

- `autenticacao.js`: realiza autenticação e retorna o token para os testes  

---

### 📁 fixtures/
Contém dados estáticos utilizados nos testes.
 

---

### 📁 config/
Arquivos de configuração do projeto, como definição de cenários de teste e parâmetros.

---

### 📁 utils/
Funções utilitárias para apoio aos testes.

Exemplo:
- geração de dados dinâmicos  
- formatação de informações  

---

## 🎯 Objetivo dos Testes

- Avaliar o tempo de resposta da API  
- Validar a estabilidade sob carga  
- Garantir o funcionamento correto de endpoints críticos  
- Identificar possíveis gargalos e falhas  

---

## ⚙️ Instalação

1. Clone o repositório:

```bash
git clone https://github.com/AndyTex2003/banco-api-performance-t3.git
```

2. Acesse a pasta do projeto:

```bash
cd banco-api-performance-t3
```

3. Instale o k6 (caso ainda não tenha):

https://k6.io/docs/get-started/installation/

---

## ▶️ Execução dos testes

Execute os testes com:

```bash
k6 run tests/login.test.js
k6 run tests/transferencias.test.js
```

---

### 🔧 Variável de ambiente (opcional)

É possível sobrescrever a URL base da API utilizando a variável de ambiente `BASE_URL`.

Exemplo:

```bash
BASE_URL=http://localhost:3000 k6 run tests/transferencias.test.js
```

Caso a variável não seja informada, será utilizada a URL definida no arquivo de configuração local (`config.local.json`).

---

## 📊 Observações técnicas

Durante a execução dos testes, foi possível validar o comportamento da API em cenários de autenticação e transferência, garantindo consistência nas respostas e estabilidade nos endpoints testados.

---

## 🧠 Aprendizados

Durante o desenvolvimento deste projeto, foram aplicados conceitos como:

- Testes de performance com k6  
- Organização de código com helpers, fixtures e utils  
- Uso de variáveis de ambiente com fallback para configuração local  
- Validação de comportamento de APIs sob carga  

---

## 👨‍💻 Autor

Desenvolvido por Anderson Batista dos Santos 🚀
