# TUDO que você deve estudar de JavaScript antes do React ou Next

![Banner](./images/cover-note-js-for-react.png)


## Índice

- [Babel](#babel)
- [Webpack](#webpack)
- [Vite](#vite)
- [Vanilla JS](#vanilla-js)
- [Desestruturação](#desestruturacao)
- [Rest Operator](#rest-operator)
- [Métodos de Array](#metodos-de-array)
- [Template Literals](#template-literals)
- [Optional Chaining](#optional-chaining)
- [Promises e Async/Await](#promises-e-asyncawait)
- [Importação e Exportação de módulos](#importacao-e-exportacao-de-modulos)

# Babel
 ## O que é o Babel?
**Babel é uma ferramenta essencial para desenvolvedores JavaScript.**
Ele funciona como um transpilador, convertendo código JavaScript moderno (ES6+) em versões mais antigas, garantindo compatibilidade com todos os navegadores, mesmo os que não suportam as novas funcionalidades.

Com Babel, você pode usar recursos avançados da linguagem sem se preocupar com o suporte dos navegadores.

🔗 [Veja um vídeo explicativo sobre Babel (Código Fonte TV)](https://www.youtube.com/watch?v=RZQMAuHE_hw)

### Exemplo prático

Suponha que você escreveu o seguinte código moderno:

```js
const soma = (a, b) => a + b;
```

Com Babel, esse código pode ser transformado para uma versão compatível com navegadores antigos:

```js
var soma = function(a, b) {
	return a + b;
};
```

Assim, seu código funciona em mais navegadores!

---

### Babel no React e Next.js

No desenvolvimento com React e Next.js, o Babel é fundamental para transformar JSX (uma sintaxe que não existe nativamente no navegador) em JavaScript puro.

Por exemplo, este código JSX:

```jsx
<button onClick={handleClick}>Enviar</button>
```

👉 O Babel transforma JSX em JavaScript puro:

```js
React.createElement("button", { onClick: handleClick }, "Enviar");
```

Ou seja:

- O React depende do Babel para funcionar corretamente com JSX.
- O Next.js já vem com Babel configurado por padrão.
- Você quase nunca precisa mexer na configuração do Babel nesses frameworks, mas é importante entender o que ele faz nos bastidores.


## Webpack
## O que é o Webpack?
**Webpack é um empacotador de módulos para aplicações JavaScript.**
Ele pega todos os arquivos do seu projeto (JavaScript, CSS, imagens, etc.) e os transforma em um ou mais arquivos finais otimizados para o navegador.

Com o Webpack, você pode usar módulos, importar arquivos e dividir seu código em partes menores (code splitting), facilitando a manutenção e melhorando a performance da aplicação.

🔗 [Veja um vídeo explicativo sobre Webpack (Código Fonte TV)](https://www.youtube.com/watch?v=PcWOAYbTc9Y&t=17s)

### Exemplo prático

Suponha que você tenha vários arquivos JS no seu projeto:

```js
// arquivo1.js
export function somar(a, b) {
	return a + b;
}

// arquivo2.js
import { somar } from './arquivo1';
console.log(somar(2, 3));
```

O Webpack empacota tudo em um único arquivo final (ex: bundle.js), pronto para ser usado no navegador.

---

### Webpack no React e Next.js


No React, o Webpack é usado para empacotar todos os arquivos do projeto, inclusive os arquivos JSX e CSS, em um bundle otimizado.

- O Create React App já trazia o Webpack configurado por padrão, mas esse projeto foi descontinuado e não é mais recomendado para novos projetos.
- O Next.js usa o Webpack internamente, mas você raramente precisa configurar manualmente.

Ou seja:

- O Webpack facilita o desenvolvimento moderno, permitindo importar arquivos, usar módulos e otimizar o carregamento da aplicação.
- No dia a dia, você quase nunca precisa mexer na configuração do Webpack em projetos React/Next.js, mas é importante saber o que ele faz!

## Vite
## O que é o Vite?
**Vite é uma ferramenta de build e desenvolvimento extremamente rápida para projetos web modernos.**
Ele utiliza o poder do ES Modules nativo do navegador para fornecer um ambiente de desenvolvimento instantâneo e builds super otimizados para produção.

O Vite foi criado para ser uma alternativa mais simples e rápida ao Webpack, especialmente para projetos com frameworks como React, Vue e Svelte.

🔗 [Veja um vídeo explicativo sobre Vite (Hashtag Programação)](https://www.youtube.com/watch?v=iNewmFYHjIw)

### Exemplo prático

Com Vite, basta rodar um comando para iniciar o projeto e ver as mudanças em tempo real, sem recarregar toda a página:

```bash
npx create-vite@latest meu-projeto --template react
cd meu-projeto
npm install
npm run dev
```

O Vite serve os arquivos diretamente, aproveitando o cache do navegador e recarregando só o que mudou.

---

### Vite no React e Next.js

O Vite se tornou o padrão para novos projetos React (substituindo o Create React App) por ser muito mais rápido e simples de configurar.

- Para projetos React, basta usar o template oficial do Vite.
- O Next.js ainda não usa Vite, pois tem seu próprio sistema de build, mas o Vite é excelente para projetos React puros e bibliotecas.

Ou seja:

- O Vite facilita o desenvolvimento moderno, com recarregamento instantâneo e builds rápidos.
- É a escolha recomendada para novos projetos React que não precisam de funcionalidades avançadas do Next.js.

## Vanilla JS
Conteúdo em breve.

## Desestruturação
Conteúdo em breve.

## Rest Operator
Conteúdo em breve.

## Métodos de Array
Conteúdo em breve.

## Template Literals
Conteúdo em breve.

## Optional Chaining
Conteúdo em breve.

## Promises e Async/Await
Conteúdo em breve.

## Importação e Exportação de módulos
Conteúdo em breve.


## Webpack