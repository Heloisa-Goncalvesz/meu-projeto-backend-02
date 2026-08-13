## 🚀 Teste 2 de memorização de comandos "Configuração de Servidor Back-End com Express e TypeScript"

Este projeto possui a estrutura inicial de uma aplicação back-end construída com **Node.js**, **Express** e **TypeScript**. O objetivo é demonstrar a preparação do ambiente de desenvolvimento do zero, a configuração das ferramentas e a criação de um servidor HTTP funcional.

---

## 💡 Explicação Geral das Tecnologias

* **Node.js:** É o ambiente de execução que nos permite rodar JavaScript no lado do servidor (fora do navegador).
* **TypeScript:** É um superset do JavaScript que adiciona **tipagem estática** ao código. Isso ajuda a capturar erros ainda em tempo de desenvolvimento e melhora o autocompletar da IDE.
* **Express:** É um framework web minimalista para Node.js que facilita o gerenciamento de rotas, requisições e respostas HTTP.
* **TSX:** Uma ferramenta moderna que executa arquivos TypeScript diretamente e possui a flag `--watch`, que reinicia o servidor automaticamente sempre que um arquivo é alterado.

## Comandos em Ordem 
npm init -y
npm i -D typescript @types/node tsx
npx tsc --init
Rode estes comandos para preparar o framework Express:
npm install express
npm install -D @types/express
crie uma pasta e o arquivo .ts: src/app.ts

A estrutura ficará assim:
meu-projeto-backend
´´´
│
├── node_modules
├── src
│   └── app.ts
├── package.json
└── tsconfig.json
´´´

Criar o servidor com Express
No arquivo app.ts, adicione o seguinte código:
// Importa a biblioteca Express e também o tipo Express
// O Express será utilizado para criar o servidor web
import express from "express";
import type { Express } from "express";

// Cria uma aplicação Express
// A função express() devolve um objeto que representa o servidor da aplicação
const app: Express = express();

// Define a porta onde o servidor ficará disponível
// Neste caso, o servidor poderá ser acessado pela porta 8081
const PORT: number = 8081;

// Inicializa o servidor utilizando a porta definida
// O método listen() faz o servidor começar a "escutar" requisições HTTP
app.listen(PORT, () => {
  console.log(`Servidor rodando em http://localhost:${PORT}`);
});
Configurar o script de execução
Abra o arquivo package.json e altere a seção "scripts" para:
"scripts": {
  "dev": "tsx watch src/app.ts"
},
Executar o servidor
No terminal, execute:
npm run dev
Se tudo estiver correto, o terminal exibirá:
Servidor rodando em http://localhost:8081
