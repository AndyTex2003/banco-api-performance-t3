# Banco API Performance - Testes de Performance com k6

![k6](https://img.shields.io/badge/k6-7D64FF?style=flat-square&logo=k6&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Performance](https://img.shields.io/badge/Testes-Performance-2DA44E?style=flat-square)
![API REST](https://img.shields.io/badge/API-REST-0A7EA4?style=flat-square)

Projeto de **testes de performance de API REST** desenvolvido com **k6** e **JavaScript**, utilizando uma API bancária como sistema sob teste.

O projeto foi criado para avaliar o comportamento da API sob diferentes condições de carga, utilizando cenários de execução, checks e thresholds para validar as respostas, acompanhar os tempos de resposta e analisar o comportamento da aplicação durante os testes.

---

## Tecnologias Utilizadas

![k6](https://img.shields.io/badge/k6-7D64FF?style=flat-square&logo=k6&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)

---

## Estrutura do Projeto

```text
banco-api-performance-t3/
│
├── config/
│   └── config.local.json
│
├── fixtures/
│   └── postLogin.json
│
├── helpers/
│   └── autenticacao.js
│
├── tests/
│   ├── login.test.js
│   └── transferencias.test.js
│
├── utils/
│   └── variaveis.js
│
├── .gitignore
└── README.md
```

---

## Organização dos Arquivos

### `tests/`

Contém os scripts de teste de performance executados com k6.

- `login.test.js`: testes relacionados ao fluxo de autenticação.
- `transferencias.test.js`: testes relacionados ao fluxo de transferências entre contas.

### `helpers/`

Reúne funções auxiliares reutilizadas durante a execução dos testes.

- `autenticacao.js`: centraliza o fluxo de autenticação e a obtenção do token utilizado pelos testes.

### `fixtures/`

Contém dados estáticos utilizados durante as execuções.

- `postLogin.json`: massa de dados utilizada no fluxo de autenticação.

### `config/`

Armazena configurações e parâmetros utilizados pelo projeto.

- `config.local.json`: configurações locais utilizadas durante a execução dos testes.

### `utils/`

Reúne valores e recursos auxiliares compartilhados pelos testes.

- `variaveis.js`: centraliza variáveis utilizadas pela automação.

---

## Objetivo dos Testes

- Avaliar os **tempos de resposta** da API.
- Analisar o comportamento da aplicação **sob carga**.
- Verificar o comportamento de **endpoints críticos** durante as execuções.
- Identificar possíveis **gargalos, degradações de desempenho e falhas**.

---

## Instalação

### Clonar o repositório

```bash
git clone https://github.com/AndyTex2003/banco-api-performance-t3.git
```

### Acessar o diretório

```bash
cd banco-api-performance-t3
```

### Instalar o k6

Para executar os testes, é necessário ter o **k6** instalado no ambiente.

As instruções oficiais de instalação estão disponíveis na documentação do k6:

[Documentação de instalação do k6](MANTENHA_AQUI_O_LINK_ATUAL)

---

## Execução dos Testes

### Teste de Login

Executa o teste de performance do fluxo de autenticação.

```bash
k6 run tests/login.test.js
```

### Teste de Transferências

Executa o teste de performance do fluxo de transferências entre contas.

```bash
k6 run tests/transferencias.test.js
```
---

## Variável de Ambiente (Opcional)

A URL base da API pode ser sobrescrita por meio da variável de ambiente `BASE_URL`.

Caso a variável não seja informada, será utilizada a URL definida no arquivo `config/config.local.json`.

### Linux, macOS ou Git Bash

```bash
BASE_URL=http://localhost:3000 k6 run tests/transferencias.test.js
```

### Windows PowerShell

```powershell
$env:BASE_URL="http://localhost:3000"
k6 run tests/transferencias.test.js
```

Essa configuração permite executar os mesmos testes contra diferentes ambientes sem alterar o código-fonte.

---

## Observações Técnicas

Durante a execução dos testes, foi possível avaliar o comportamento da API nos fluxos de **autenticação** e **transferências** sob as condições de carga definidas nos cenários.

Os **checks** e **thresholds** foram utilizados para validar as respostas e acompanhar métricas de desempenho, como **tempos de resposta** e comportamento da aplicação durante as execuções.

---

## Aprendizados

Durante o desenvolvimento deste projeto, foi possível aplicar e aprofundar conceitos relacionados a:

- Testes de performance com **k6**
- Criação de **cenários de carga**
- Uso de **checks** e **thresholds**
- Organização de código com `helpers`, `fixtures` e `utils`
- Uso de **variáveis de ambiente** com fallback para configuração local
- Análise de **tempos de resposta** e comportamento da API sob carga

---

## Autor

**Anderson Batista dos Santos**

QA | Testes de Software | Qualidade de Software

- LinkedIn: [linkedin.com/in/anderson-santos-qa](https://www.linkedin.com/in/anderson-santos-qa/)
- GitHub: [github.com/AndyTex2003](https://github.com/AndyTex2003)
