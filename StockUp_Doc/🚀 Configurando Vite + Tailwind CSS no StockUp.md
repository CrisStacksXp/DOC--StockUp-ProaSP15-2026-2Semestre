___

Configurando o ambiente do **StockUp** passo a passo, usando **Vite + JavaScript + Tailwind CSS**, sem frameworks como React ou Angular.]
## Etapa 1 — Verificar se o Node.js está instalado

O Vite precisa do Node.js e do npm para funcionar.

Abra o terminal do VS Code e execute:

```shell
node -v
```

Depois:

```shell
npm -v
```

Os dois comandos devem retornar números de versão.

- `node -v`: mostra a versão do Node.js.
- `npm -v`: mostra a versão do gerenciador de pacotes npm.

Se algum comando não funcionar, instale uma versão compatível do Node.js pelo site oficial: [Node.js](https://nodejs.org/?utm_source=chatgpt.com).

> **Importante:** execute esses comandos antes de continuar. Se ambos funcionarem, prossiga para a próxima etapa.
> 
> As versões usadas seção as seguintes:
> 
>  node -v node: v24.14.0
>  npm -v npm: 11.9.0

---

## Etapa 2 — Criar o projeto Vite

No terminal, navegue até a pasta onde deseja armazenar o projeto.

Por exemplo, no Linux:

```shell
cd ~/Projetos
```

Se a pasta não existir, você poderá criá-la com `mkdir`.

Agora execute:

```shell
npm create vite@latest stockup -- --template vanilla
```

### O que esse comando faz?

- `npm create vite@latest`: utiliza o assistente de criação do Vite.
- `stockup`: define o nome da pasta do projeto.
- `--template vanilla`: cria um projeto com JavaScript puro, sem React, Vue ou Angular.

Se o terminal perguntar se deseja instalar um pacote para continuar, confirme.

Em seguida, entre na pasta:

```shell
cd stockup
```

Instale as dependências iniciais:

```shell
npm install
```

### Qual será a estrutura inicial?

O Vite criará arquivos semelhantes a estes:

```shell
stockup/
├── public/
├── src/
│   ├── counter.js
│   ├── javascript.svg
│   ├── main.js
│   └── style.css
├── index.html
├── package.json
└── vite.config.js
```

Essa é uma estrutura inicial de exemplo. Mais adiante, podemos adaptá-la à organização do StockUp.

---

A documentação oficial do [Vite](https://vite.dev/guide/?utm_source=chatgpt.com) confirma esse fluxo de criação de projetos. Agora vamos integrar o Tailwind CSS usando o método atual da versão 4. [vitejs](https://vite.dev/guide/?utm_source=chatgpt.com)

---

## Etapa 3 — Instalar o Tailwind CSS

Certifique-se de estar dentro da pasta `stockup`.

Execute:

```shell
npm install tailwindcss @tailwindcss/vite
```

### O que estamos instalando?

|Pacote|Função|
|---|---|
|`tailwindcss`|Disponibiliza as classes utilitárias do Tailwind CSS.|
|`@tailwindcss/vite`|Integra o Tailwind CSS ao Vite.|

**Atenção:** estamos usando o Tailwind CSS 4. Nesse método, não precisamos executar `npx tailwindcss init -p` nem criar manualmente os arquivos `tailwind.config.js` e `postcss.config.js`. A integração é feita pelo plugin do Vite. [Tailwind CSS](https://tailwindcss.com/docs/installation/using-vite?utm_source=chatgpt.com)

---

## Etapa 4 — Configurar o Vite

Na raiz do projeto, abra o arquivo:

```shell
vite.config.js
```

Substitua o conteúdo pelo seguinte:

```javascript
import { defineConfig } from 'vite';
import tailwindcss from '@tailwindcss/vite';

export default defineConfig({
  plugins: [
    tailwindcss(),
  ],
});
```

### Entendendo o código

- `defineConfig`: ajuda a definir as configurações do Vite.
- `tailwindcss`: importa o plugin do Tailwind CSS.
- `plugins`: registra os plugins que o Vite deve utilizar.
- `tailwindcss()`: ativa a integração.

**Resultado:** o Vite passa a processar o Tailwind CSS durante o desenvolvimento e a compilação do projeto.

---

## Etapa 5 — Configurar o CSS

Abra o arquivo:

```shell
src/style.css
```

Apague o conteúdo padrão e adicione:

```javascript
@import "tailwindcss";

body {
  margin: 0;
  min-height: 100vh;
  font-family: Arial, sans-serif;
}
```

A linha abaixo é a principal configuração do Tailwind CSS 4:

```javascript
@import "tailwindcss";
```

Ela importa o Tailwind para que suas classes utilitárias possam ser geradas e utilizadas no projeto. [Tailwind CSS](https://tailwindcss.com/docs/installation/using-vite?utm_source=chatgpt.com)

**Importante:** não misture essa configuração com as antigas diretivas do Tailwind 3, como `@tailwind base`, `@tailwind components` e `@tailwind utilities`.

---

## Etapa 6 — Verificar a importação do CSS

Abra:

```shell
src/main.js
```

Certifique-se de que ele importa o arquivo CSS:

```javascript
import './style.css';
```

O arquivo `main.js` também deve conter o código JavaScript responsável por exibir o conteúdo da página.

Por exemplo, você pode substituir temporariamente seu conteúdo pelo seguinte:

```javascript
import './style.css';

document.querySelector('#app').innerHTML = `
  <main class="flex min-h-screen items-center justify-center bg-slate-900 p-6">
    <section class="rounded-2xl bg-white p-8 text-center shadow-xl">
      <h1 class="text-3xl font-bold text-emerald-600">
        StockUp
      </h1>

      <p class="mt-3 text-slate-600">
        Gerenciamento de estoque simplificado.
      </p>

      <button class="mt-6 rounded-lg bg-emerald-600 px-5 py-3 font-semibold text-white hover:bg-emerald-700">
        Começar
      </button>
    </section>
  </main>
`;
```

Esse código cria uma tela simples para verificar se o Tailwind está funcionando.

### Por que esse teste é importante?

As classes abaixo são fornecidas pelo Tailwind CSS:

- `flex`: ativa o Flexbox.
- `min-h-screen`: define uma altura mínima de uma tela.
- `items-center` e `justify-center`: centralizam o conteúdo.
- `bg-slate-900`: define a cor de fundo.
- `rounded-2xl`: arredonda as bordas.
- `text-emerald-600`: define a cor do texto.
- `hover:bg-emerald-700`: altera o fundo do botão quando o cursor passa sobre ele.

Se as classes forem aplicadas, a configuração está funcionando.

---

## Etapa 7 — Verificar o arquivo HTML

Abra o arquivo `index.html`, localizado na raiz do projeto.

O template do Vite já deve ter criado uma estrutura semelhante a esta:

```html
<!doctype html>
<html lang="pt-BR">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>StockUp</title>
  </head>

  <body>
    <div id="app"></div>

    <script type="module" src="/src/main.js"></script>
  </body>
</html>
```

O elemento:

```html
<div id="app"></div>
```

é onde o JavaScript do exemplo anterior insere o conteúdo da página.

E esta linha:

```html
<script type="module" src="/src/main.js"></script>
```

carrega o JavaScript como um módulo, permitindo utilizar `import` e `export`.

---

## Etapa 8 — Executar o projeto

No terminal, execute:

```shell
npm run dev
```

O Vite deverá exibir uma mensagem semelhante a esta:

```shell
VITE ready

Local: http://localhost:5173/
```

Abra o endereço indicado no navegador.

Você deverá visualizar uma página com fundo escuro, um cartão branco centralizado e o nome StockUp em verde.

O Vite também atualiza a página automaticamente quando você salva alterações nos arquivos durante o desenvolvimento. [vitejs](https://vite.dev/guide/?utm_source=chatgpt.com)

Para interromper o servidor, volte ao terminal e pressione `Ctrl + C`.

---

## Etapa 9 — Verificar se o projeto pode ser compilado

Quando a página estiver funcionando, pare o servidor ou abra outro terminal na pasta do projeto e execute:

```shell
npm run build
```

Esse comando verifica se o projeto pode ser compilado para produção.

Se funcionar, o Vite gerará uma pasta chamada `dist`, que conterá os arquivos preparados para publicação.

**Não edite manualmente os arquivos de `dist`.** Continue trabalhando nos arquivos de `src` e gere novamente a compilação quando necessário.

---

## Etapa 10 — Estruturar o projeto StockUp

Depois de concluir o teste, podemos começar a organizar o código do sistema.

Uma estrutura inicial simples seria:

```shell
stockup/
├── public/
├── src/
│   ├── assets/
│   ├── config/
│   ├── pages/
│   │   ├── dashboard.js
│   │   ├── products.js
│   │   ├── sales.js
│   │   └── login.js
│   ├── services/
│   │   ├── products.js
│   │   ├── sales.js
│   │   └── auth.js
│   ├── styles/
│   │   └── main.css
│   ├── main.js
│   └── style.css
├── index.html
├── package.json
├── package-lock.json
└── vite.config.js
```

Por enquanto, **não é necessário criar todos esses arquivos**. Primeiro, confirme que Vite e Tailwind CSS estão funcionando.

Depois, podemos mover o CSS para `src/styles/main.css`, ajustar a importação e começar a organizar as páginas.

### Como dividir o trabalho com a equipe

Para evitar conflitos, recomendo que todos utilizem a mesma estrutura e as mesmas dependências. Quando o projeto estiver no GitHub, os colegas poderão clonar o repositório e executar:

```shell
npm install
npm run dev
```

O `package.json` e o `package-lock.json` devem ser versionados no Git. Já a pasta `node_modules` não deve ser enviada ao repositório.