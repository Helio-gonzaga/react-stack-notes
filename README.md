# 🚀 TUDO que você deve estudar de JavaScript antes do React ou Next.js

![Banner](./images/cover-note-js-for-react.png)

> 📌 Este documento é um guia completo para quem quer migrar ou se aprofundar na **stack Web moderna**, entendendo **JavaScript de verdade** antes de entrar em React ou Next.js.  
> Ideal para quem vem do **Android (Kotlin/Java)** ou **iOS (Swift)** e quer entender como a Web realmente funciona.

---

## 📚 Índice Principal

- 🌍 [Como a web funciona](#como-a-web-funciona)
- 🌐 [Como funciona o navegador](#como-funciona-o-navegador)
- 🌳 [Document Object Model (DOM)](#document-object-model-dom)
- 🔄 [Babel](#babel)
- 📦 [Webpack](#webpack)
- ⚡ [Vite](#vite)
- 🌳 [Document Object Model (DOM)](#document-object-model-dom)
- 🧩 [Desestruturação](#desestruturacao)
- 🧠 [Rest Operator](#rest-operator)
- 🔁 [Métodos de Array](#metodos-de-array)
- ✨ [Template Literals](#template-literals)
- ❓ [Optional Chaining](#optional-chaining)
- ⏳ [Promises e Async/Await](#promises-e-asyncawait)
- 📥📤 [Importação e Exportação de Módulos](#importacao-e-exportacao-de-modulos)

---

## 🌍 Como a web funciona

A Web funciona por meio da comunicação entre **clientes (navegadores)** e **servidores**, utilizando o protocolo **HTTP/HTTPS**.

Quando você digita um endereço no navegador, acontece o seguinte fluxo:

1. ✍️ Você digita uma URL no navegador
2. 📡 O navegador faz uma requisição HTTP para o servidor
3. 🗄️ O servidor responde com arquivos (HTML, CSS, JS, imagens, etc.)
4. 🖥️ O navegador interpreta esses arquivos e monta a página na tela

🔁 Esse ciclo acontece o tempo todo enquanto navegamos na internet.

---

## 🌐 Como funciona o navegador

**O navegador é o runtime da Web.**  
Ele não apenas exibe HTML, mas também:

- Executa JavaScript
- Aplica estilos CSS
- Gerencia cache, cookies e armazenamento local
- Garante segurança da navegação

### 🧠 Etapas principais do navegador

1. **📡 Requisição:** Envia uma requisição HTTP/HTTPS
2. **📥 Recebimento:** Recebe HTML, CSS, JS, imagens, etc.
3. **🌳 Parsing:** Constrói o DOM (Document Object Model)
4. **🎨 Renderização:** Aplica CSS e monta a árvore de renderização
5. **⚙️ Execução:** Executa JavaScript e atualiza o DOM
6. **🖌️ Pintura:** Desenha tudo na tela

### 🛠️ Navegadores modernos possuem:

- Engine JavaScript (V8, SpiderMonkey, JavaScriptCore)
- DevTools
- Gerenciamento de abas, histórico, cache e storage

🔗 [🎥 Como funciona o navegador (Alura)](https://www.youtube.com/watch?v=kDy62zaCHZE)

---

## 🔄 Babel

### ❓ O que é o Babel?

**Babel é um transpilador de JavaScript.**  
Ele converte código **JavaScript moderno (ES6+)** em versões mais antigas, garantindo compatibilidade com todos os navegadores.

👉 Com Babel, você pode usar:

- arrow functions
- const / let
- optional chaining
- JSX

sem se preocupar com suporte de browser.

🔗 [🎥 Babel explicado (Código Fonte TV)](https://www.youtube.com/watch?v=RZQMAuHE_hw)

### 🧪 Exemplo prático

Código moderno:

```js
const soma = (a, b) => a + b;
```

Código após o Babel:

```js
var soma = function (a, b) {
  return a + b;
};
```

⚛️ Babel no React e Next.js

JSX não existe no navegador:

```html
<button onClick="{handleClick}">Enviar</button>
```

Babel transforma em JavaScript puro:

```js
React.createElement("button", { onClick: handleClick }, "Enviar");
```

✅ React depende do Babel

✅ Next.js já vem com Babel configurado

⚠️ Normalmente você não mexe, mas precisa entender

## 📦 Webpack

### ❓ O que é o Webpack?

Webpack é um empacotador de módulos.
Ele gera bundles otimizados para o navegador.

🔗 [🎥 Webpack explicado (Código Fonte TV)](https://www.youtube.com/watch?v=PcWOAYbTc9Y&t=35s)

🧪 Exemplo prático

```js
// arquivo1.js
export function somar(a, b) {
  return a + b;
}

// arquivo2.js
import { somar } from "./arquivo1";
console.log(somar(2, 3));
```

⚛️ Webpack no React e Next.js

Create React App usava Webpack (descontinuado)

Next.js usa Webpack internamente

Quase nunca precisa configurar

## ⚡ Vite

### ❓ O que é o Vite?

Vite é uma ferramenta de build extremamente rápida.
Usa ES Modules nativos do navegador.

🔗 [🎥 Vite explicado (Hashtag Programação)](https://www.youtube.com/watch?v=iNewmFYHjIw)

🚀 Criando projeto React com Vite

```bash
npx create-vite@latest meu-projeto --template react
cd meu-projeto
npm install
npm run dev
```

## 🌳 Document Object Model

### ❓ O que é o DOM?

**O DOM (Document Object Model) é a representação da página web em forma de árvore.**  
Cada elemento HTML (div, button, input, etc.) vira um **nó** que pode ser acessado e manipulado pelo JavaScript.

Quando você:

- clica em um botão
- digita em um input
- abre um modal
- atualiza um texto na tela

👉 você está interagindo diretamente com o **DOM**.

---

🎥 Vídeo recomendado

🔗 [🎥 DOM e JavaScript na prática (Rocketseat)](https://www.youtube.com/watch?v=UftSB4DaRU4)

Esse vídeo explica:

o que é DOM

como o JS interage com ele

base para entender frameworks como React

### 🧠 Pensando como dev Mobile (Android / iOS)

Se você vem do mobile, pensa assim:

| Mobile                       | Web                 |
| ---------------------------- | ------------------- |
| View / ViewGroup             | DOM                 |
| ConstraintLayout / StackView | Estrutura em árvore |
| setText(), setVisibility()   | Manipulação via JS  |
| Re-render da View            | Atualização do DOM  |

👉 A grande diferença é que na Web o DOM **fica exposto** para o JavaScript.

---

### ⚙️ Como o JavaScript usa o DOM?

O JavaScript pode:

- 🔍 buscar elementos
- ✏️ alterar texto e estilos
- ➕ criar novos elementos
- ❌ remover elementos
- 🎧 escutar eventos (click, input, submit)

Exemplo simples:

```js
const button = document.querySelector("button");

button.addEventListener("click", () => {
  button.textContent = "Clicado!";
});
```

⚛️ DOM e React

React não manipula o DOM diretamente o tempo todo.

React cria um Virtual DOM

Compara mudanças (diff)

Atualiza somente o necessário no DOM real

👉 Entender DOM ajuda MUITO a:

evitar re-render desnecessário

entender performance

debugar problemas estranhos
