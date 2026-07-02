# AtivAI 📚🤖

O **AtivAI** é um Gerador Inteligente de Atividades Pedagógicas voltado para os anos iniciais do Ensino Fundamental (do 1º ao 5º ano). 

Esta aplicação web foi desenvolvida com o intuito de facilitar a rotina de professores e pedagogos, utilizando Inteligência Artificial para gerar atividades e materiais didáticos completos, estruturados, pedagogicamente adequados e prontos para impressão em formato PDF.

---

## 🎓 Contexto Acadêmico

Este projeto foi desenvolvido como requisito avaliativo para a disciplina de **Inteligência Artificial** no curso de **Tecnologia em Análise e Desenvolvimento de Sistemas (ADS)** do **UniSenac**. 

O objetivo do projeto é demonstrar a viabilidade prática da integração de Large Language Models (LLMs) via API em aplicações web reais, aplicando técnicas de engenharia de prompt para guiar a IA na geração de saídas estruturadas e sem alucinações.

---

## ✨ Funcionalidades

- **Geração Inteligente de Conteúdo:** Produção automatizada de atividades estruturadas e personalizadas baseadas em parâmetros pedagógicos informados pelo usuário.
- **Filtros Personalizados:** Ajuste automático de vocabulário, complexidade e extensão de acordo com o ano escolar (1º ao 5º ano), disciplina e conteúdo específico.
- **Materiais Prontos para Impressão:** Geração de atividades completas (com título, breves explicações conceituais, enunciados claros e exercícios).
- **Exportação em PDF de Alta Qualidade:** Conversão instantânea da atividade gerada em formato PDF formatado e pronto para impressão.
- **Visualização em Tempo Real:** Renderização imediata da resposta da IA em Markdown e tabelas organizadas.
- **Diretrizes Anti-Alucinação:** O sistema é blindado com um prompt robusto para garantir que a IA não invente informações e forneça apenas conteúdos precisos e corretos.

---

## 🖥️ Tecnologias Utilizadas

O projeto adota uma arquitetura simplificada e eficiente, dividida entre Front-end e Back-end:

### Front-end
- **HTML5 & CSS3:** Estruturação da página e design moderno com foco em usabilidade.
- **Vanilla JavaScript:** Lógica da interface, envio de requisições assíncronas e manipulação dinâmica do DOM.
- **Marked.js:** Biblioteca utilizada para renderizar a saída Markdown gerada pela IA de forma visualmente agradável na tela.

### Back-end
- **Node.js & Express.js:** Servidor HTTP ágil para disponibilização das rotas e serviços.
- **Dotenv:** Gerenciamento seguro de variáveis de ambiente (como chaves de API).
- **CORS:** Liberação e controle de acessos entre domínios.
- **Puppeteer:** Ferramenta para automação do navegador Chrome headless, responsável por converter dinamicamente o HTML das atividades em arquivos PDF formatados para impressão.

### Inteligência Artificial
- **OpenRouter API:** Ponte de comunicação com os modelos de linguagem de última geração.
- **Prompt Engineering:** Criação de um prompt de sistema estrito contendo regras pedagógicas, limitações de saída (ex: sem LaTeX, uso de frações em formato amigável, tabelas estruturadas) e restrições de segurança.

---

## 📁 Estrutura do Projeto

A organização dos arquivos segue a seguinte estrutura:

```text
ativai/
├── public/                # Arquivos estáticos servidos pelo Express
│   ├── css/
│   │   └── style.css      # Estilização da interface da aplicação
│   ├── index.html         # Página principal do sistema
│   └── pdf-template.html  # Template base utilizado pelo Puppeteer para gerar o PDF
├── server.js              # Inicialização do servidor Node.js e rotas de API
├── package.json           # Dependências e scripts de execução do projeto
├── package-lock.json      # Registro exato de versões das dependências
├── .env.example           # Modelo para configuração das variáveis de ambiente
└── README.md              # Documentação oficial do projeto
```

---

## ⚙️ Instalação e Configuração

Siga os passos abaixo para clonar e rodar o projeto localmente em sua máquina.

### Pré-requisitos
Certifique-se de ter instalado em sua máquina:
- [Node.js](https://nodejs.org/) (versão 18 ou superior recomendada)
- Git (opcional, para clonagem)

### 1. Clonar o repositório
```bash
git clone https://github.com/rafaelaboldt/ativai.git

cd ativai
```

### 2. Instalar as dependências do projeto
```bash
npm install
```

### 3. Configurar as variáveis de ambiente
Crie um arquivo `.env` na raiz do projeto (use como base o `.env.example`) e adicione a sua chave de API do OpenRouter:
```env
PORT=3000
OPENROUTER_API_KEY=sua_chave_do_openrouter_aqui
```

---

## 🚀 Executando o Projeto

Para iniciar o servidor localmente:

```bash
npm start
```
ou utilizando diretamente o Node:
```bash
node server.js
```

O console deverá exibir uma mensagem confirmando a execução:
```text
Servidor rodando em http://localhost:3000
```

Abra o seu navegador de preferência e acesse o endereço acima para começar a usar a aplicação.

---

## 🧠 Como Utilizar a Aplicação

1. **Defina os Parâmetros:** Na barra lateral, selecione o Ano Escolar (ex: 3º Ano), informe a Disciplina (ex: Ciências) e detalhe o Conteúdo a ser trabalhado (ex: O Ciclo da Água).
2. **Gere a Atividade:** Clique no botão **Gerar Atividade**. A aplicação fará a requisição à API e renderizará o conteúdo gerado na tela.
3. **Visualize e Ajuste:** Verifique se as informações estão organizadas (textos, tabelas ou caça-palavras).
4. **Exporte para Impressão:** Caso o material esteja ideal, clique no botão **Baixar PDF** para fazer o download do documento pronto para impressão.

---

## 🎯 Objetivos de Aprendizado

Com o desenvolvimento deste projeto, foram alcançados e consolidados conhecimentos em:
- Integração dinâmica de APIs com serviços de Inteligência Artificial generativa.
- Formulação e refinamento de prompts para controle rigoroso de qualidade em aplicações de IA (*System Prompts*).
- Geração automatizada de relatórios e documentos PDF no lado do servidor com Puppeteer.
- Arquitetura de aplicações Web Node.js robustas e eficientes.
