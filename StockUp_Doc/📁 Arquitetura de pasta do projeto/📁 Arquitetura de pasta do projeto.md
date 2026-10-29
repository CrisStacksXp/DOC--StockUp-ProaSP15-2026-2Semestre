___

|Pasta ou arquivo|Responsabilidade|Exemplo no StockUp|
|---|---|---|
|`public/`|Armazena arquivos públicos servidos diretamente, como ícones estáticos.|Favicon do StockUp.|
|`src/assets/`|Armazena recursos utilizados pela aplicação.|Imagens e ilustrações da interface.|
|`src/components/`|Reúne elementos reutilizáveis da interface.|Botões, campos de formulário, tabelas e cartões de indicadores.|
|`src/pages/`|Contém o código responsável pelas páginas ou telas do sistema.|Produtos, vendas e dashboard.|
|`src/services/`|Concentra operações e regras relacionadas aos dados.|Cadastro de produtos, cálculo de vendas e movimentação de estoque.|
|`src/styles/`|Organiza arquivos CSS adicionais.|Estilos globais ou específicos de componentes.|
|`main.js`|Inicializa a aplicação e conecta os módulos principais.|Carregar a tela inicial e configurar a navegação.|
|`style.css`|Contém a folha de estilos principal.|Importação do Tailwind e estilos globais.|
|`index.html`|É o documento HTML de entrada da aplicação.|Define a estrutura inicial da página.|
|`package.json`|Registra dependências, informações e comandos do projeto.|`npm run dev` e `npm run build`.|
|`package-lock.json`|Registra as versões resolvidas das dependências.|Ajuda os integrantes a instalar um conjunto consistente de pacotes.|
|`vite.config.js`|Configura o Vite e seus plugins.|Integração do Tailwind CSS.|
|`.gitignore`|Define arquivos e pastas que o Git deve ignorar.|`node_modules/` e arquivos locais que não devem ser versionados.|

### Um detalhe importante sobre `components/`, `pages/` e `services/`

Essas três pastas são fundamentais para o funcionamento da arquitetura.

Pense nelas como três responsabilidades diferentes:

**`components/` → Como algo é apresentado.**

Um componente pode representar um botão de cadastro ou uma tabela de produtos. Sua função principal é cuidar de uma parte reutilizável da interface.

**`pages/` → Como uma funcionalidade é apresentada ao usuário.**

A página de produtos pode reunir um formulário, uma tabela e botões para editar ou desativar produtos.

**`services/` → Como os dados são manipulados.**

O serviço de produtos valida as regras pertinentes e executa operações de cadastro, consulta e atualização. A forma de persistência poderá mudar quando o banco de dados for implementado.

Por exemplo, uma página pode chamar `productService.createProduct(dados)`, enquanto o serviço fica responsável pela operação de cadastro.

Essa separação facilita a manutenção e permite que a equipe de UI altere a apresentação sem precisar reescrever as regras de negócio.