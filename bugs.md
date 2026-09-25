## Bugs encontrados

Durante a execução dos testes, foram identificados 2 defeitos:

- `SCRUM-5` — Ordenação de produtos A-Z não respeita ordem alfabética
- `SCRUM-6` — Ordenação de produtos Z-A não respeita ordem alfabética decrescente

## BUG 01 - Ordenação de produtos A-Z não respeita ordem alfabética

**Caso de teste no Zephyr:** `SCRUM-T8`  
**Caso relacionado:** `CT-007`  
**Bug no Jira:** `SCRUM-5`

**Descrição:**  
Ao selecionar a opção de ordenação de produtos de A a Z, a listagem não é reorganizada corretamente em ordem alfabética.

**Pré-condição:**  
Usuário autenticado no SauceDemo e na página de produtos.

**Passos para reproduzir:**
1. Acessar o SauceDemo.
2. Realizar login com usuário válido.
3. Acessar a página de produtos.
4. Selecionar a opção `Name (A to Z)`.
5. Observar a ordem dos produtos.

**Resultado esperado:**  
Os produtos devem ser exibidos em ordem alfabética crescente.

**Resultado atual:**  
Os produtos não são exibidos em ordem alfabética crescente após selecionar a opção `Name (A to Z)`.

**Status:** Aberto  
**Prioridade:** Medium

---

## BUG 02 - Ordenação de produtos Z-A não respeita ordem alfabética decrescente

**Caso de teste no Zephyr:** `SCRUM-T9`  
**Caso relacionado:** `CT-008`  
**Bug no Jira:** `SCRUM-6`

**Descrição:**  
Ao selecionar a opção de ordenação de produtos de Z a A, a listagem não é reorganizada corretamente em ordem alfabética decrescente.

**Pré-condição:**  
Usuário autenticado no SauceDemo e na página de produtos.

**Passos para reproduzir:**
1. Acessar o SauceDemo.
2. Realizar login com usuário válido.
3. Acessar a página de produtos.
4. Selecionar a opção `Name (Z to A)`.
5. Observar a ordem dos produtos.

**Resultado esperado:**  
Os produtos devem ser exibidos em ordem alfabética decrescente.

**Resultado atual:**  
Os produtos não são exibidos em ordem alfabética decrescente após selecionar a opção `Name (Z to A)`.

**Status:** Aberto  
**Prioridade:** Medium
