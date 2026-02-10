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

🔗 [Veja um vídeo explicativo sobre Babel (DevPleno)](https://www.youtube.com/watch?v=RZQMAuHE_hw)

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
Conteúdo em breve.

## Vite
Conteúdo em breve.

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