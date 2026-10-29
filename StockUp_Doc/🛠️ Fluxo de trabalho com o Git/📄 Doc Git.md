___ 


🌐 **main**
 │
 └── **🧑🏻‍💻 develop**
      │
      ├── 🛠️ **feature**/product-management
      │         │
      │         └── Pull Request → develop
      │
      ├── 🛠️  **feature**/sales
      │         │
      │         └── Pull Request → develop
      │
      ├── 🎨  **style**/product-page
      │         │
      │         └── Pull Request → develop
      │
      └── ✅️ **fix**/stock-calculation
                │
                └── Pull Request → develop

Depois que as funcionalidades integradas em `develop` forem testadas e estiverem prontas para publicação:

```
develop → Pull Request → main
```

Esse é o fluxo que eu usaria no **StockUp**.
### O que cada branch significa?

| Branch        | Finalidade                                           | Exemplo                                                             |
| ------------- | ---------------------------------------------------- | ------------------------------------------------------------------- |
| `main`        | Versão estável do projeto, pronta para publicação.   | Sistema que está no ar ou versão aprovada para entrega.             |
| `develop`     | Integração das funcionalidades antes de publicá-las. | Cadastro e listagem de produtos já integrados, mas ainda em testes. |
| `feature/...` | Desenvolvimento de uma funcionalidade nova.          | `feature/product-management`.                                       |
| `style/...`   | Alterações visuais e de apresentação.                | `style/product-page`.                                               |
| `fix/...`     | Correção de um problema identificado.                | `fix/stock-calculation`.                                            |
