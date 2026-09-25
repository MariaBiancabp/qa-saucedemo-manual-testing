# Casos de Teste

## Login

### CT-001 - Login com usuário e senha válidos
**Objetivo:** Validar que um usuário com credenciais válidas consegue acessar a aplicação.

**Pré-condição:** Estar na tela de login do SauceDemo.

**Dados de teste:**
- Username: `standard_user`
- Password: `secret_sauce`

**Resultado esperado:** Usuário autenticado e direcionado para a página de produtos.

---

### CT-002 - Login com usuário inválido
**Objetivo:** Validar que o sistema bloqueia o acesso com usuário inválido.

**Dados de teste:**
- Username: `usuario_invalido`
- Password: `secret_sauce`

**Resultado esperado:** O sistema deve impedir o acesso e exibir mensagem de erro.

---

### CT-003 - Login com campos vazios
**Objetivo:** Validar que o sistema impede o acesso quando os campos de usuário e senha não são preenchidos.

**Pré-condição:** Estar na tela de login do SauceDemo.

**Dados de teste:**
- Username: vazio
- Password: vazio

**Resultado esperado:** O sistema deve impedir o acesso e exibir mensagem informando que o campo de usuário é obrigatório.

---

### CT-004 - Login sem senha
**Objetivo:** Validar que o sistema impede o acesso quando a senha não é informada.

**Pré-condição:** Estar na tela de login do SauceDemo.

**Dados de teste:**
- Username: `standard_user`
- Password: vazio

**Resultado esperado:** O sistema deve impedir o acesso e exibir mensagem informando que a senha é obrigatória.

---

## Produtos

### CT-005 - Visualizar lista de produtos
**Objetivo:** Validar que a lista de produtos é exibida corretamente após o login.

**Pré-condição:** Usuário autenticado no SauceDemo.

**Dados de teste:**
- Username: `standard_user`
- Password: `secret_sauce`

**Resultado esperado:** Os produtos devem ser exibidos com imagem, nome, descrição, preço e botão para adicionar ao carrinho.

---

### CT-006 - Visualizar detalhes de um produto
**Objetivo:** Validar a exibição das informações detalhadas de um produto.

**Pré-condição:** Usuário autenticado e na página de produtos.

**Dados de teste:**
- Produto: `Sauce Labs Backpack`

**Resultado esperado:** A página deve exibir corretamente nome, imagem, descrição, preço e opção para adicionar o produto ao carrinho.

---

## Ordenação

### CT-007 - Ordenar produtos de A a Z
**Objetivo:** Validar a ordenação alfabética crescente dos produtos.

**Pré-condição:** Usuário autenticado e na página de produtos.

**Dados de teste:**
- Filtro: `Name (A to Z)`

**Resultado esperado:** Os produtos devem ser exibidos em ordem alfabética crescente.

**Resultado da execução:** Reprovado.

---

### CT-008 - Ordenar produtos de Z a A
**Objetivo:** Validar a ordenação alfabética decrescente dos produtos.

**Pré-condição:** Usuário autenticado e na página de produtos.

**Dados de teste:**
- Filtro: `Name (Z to A)`

**Resultado esperado:** Os produtos devem ser exibidos em ordem alfabética decrescente.

**Resultado da execução:** Reprovado.

---

### CT-009 - Ordenar produtos do menor para o maior preço
**Objetivo:** Validar a ordenação crescente dos produtos por preço.

**Pré-condição:** Usuário autenticado e na página de produtos.

**Dados de teste:**
- Filtro: `Price (low to high)`

**Resultado esperado:** Os produtos devem ser exibidos em ordem crescente de preço, do menor para o maior.

---

### CT-010 - Ordenar produtos do maior para o menor preço
**Objetivo:** Validar a ordenação decrescente dos produtos por preço.

**Pré-condição:** Usuário autenticado e na página de produtos.

**Dados de teste:**
- Filtro: `Price (high to low)`

**Resultado esperado:** Os produtos devem ser exibidos em ordem decrescente de preço, do maior para o menor.

---

## Carrinho

### CT-011 - Adicionar produto ao carrinho
**Objetivo:** Validar a adição de um produto ao carrinho.

**Pré-condição:** Usuário autenticado e na página de produtos.

**Dados de teste:**
- Produto: `Sauce Labs Backpack`

**Resultado esperado:** O produto deve ser adicionado ao carrinho e o contador deve ser atualizado para 1.

---

### CT-012 - Adicionar mais de um produto ao carrinho
**Objetivo:** Validar a inclusão de múltiplos produtos no carrinho.

**Pré-condição:** Usuário autenticado e na página de produtos.

**Dados de teste:**
- Produto 1: `Sauce Labs Backpack`
- Produto 2: `Sauce Labs Bike Light`

**Resultado esperado:** Os dois produtos devem ser adicionados ao carrinho e o contador deve ser atualizado para 2.

---

### CT-013 - Remover produto do carrinho
**Objetivo:** Validar a remoção de um produto do carrinho.

**Pré-condição:** Carrinho contendo pelo menos um produto.

**Dados de teste:**
- Produto: `Sauce Labs Backpack`

**Resultado esperado:** O produto deve ser removido do carrinho e o contador de itens deve ser atualizado.

---

### CT-014 - Validar contador de itens do carrinho
**Objetivo:** Validar se o contador do carrinho representa corretamente a quantidade de itens adicionados.

**Pré-condição:** Usuário autenticado e na página de produtos.

**Dados de teste:**
- Produto 1: `Sauce Labs Backpack`
- Produto 2: `Sauce Labs Bike Light`

**Resultado esperado:**
- Ao adicionar 1 produto, o contador deve exibir `1`.
- Ao adicionar o segundo produto, o contador deve exibir `2`.
- Ao remover um produto, o contador deve voltar para `1`.
- Ao remover o último produto, o contador não deve mais ser exibido.
