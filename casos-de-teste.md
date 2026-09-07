# Casos de Teste - SauceDemo

Documentação de casos de teste manuais para o e-commerce SauceDemo (https://www.saucedemo.com/).

---

## CT001 - Login com credenciais válidas

**Pré-condição:** Usuário não está logado no sistema.

**Passos:**
1. Acessar https://www.saucedemo.com/
2. Preencher o campo "Username" com `standard_user`
3. Preencher o campo "Password" com `secret_sauce`
4. Clicar no botão "Login"

**Resultado esperado:** Usuário é redirecionado para a página de produtos (`/inventory.html`).

**Status:** ✅ Passou

---

## CT002 - Login com senha inválida

**Pré-condição:** Usuário não está logado no sistema.

**Passos:**
1. Acessar https://www.saucedemo.com/
2. Preencher o campo "Username" com `standard_user`
3. Preencher o campo "Password" com um valor incorreto, ex: `senha_errada`
4. Clicar no botão "Login"

**Resultado esperado:** Sistema exibe mensagem de erro "Epic sadface: Username and password do not match any user in this service" e usuário permanece na tela de login.

**Status:** ✅ Passou

---

## CT003 - Login com usuário bloqueado

**Pré-condição:** Usuário não está logado no sistema.

**Passos:**
1. Acessar https://www.saucedemo.com/
2. Preencher o campo "Username" com `locked_out_user`
3. Preencher o campo "Password" com `secret_sauce`
4. Clicar no botão "Login"

**Resultado esperado:** Sistema exibe mensagem de erro informando que o usuário foi bloqueado ("Epic sadface: Sorry, this user has been locked out.").

**Status:** ✅ Passou

---

## CT004 - Adicionar produto ao carrinho

**Pré-condição:** Usuário logado com sucesso (`standard_user`), na página de produtos.

**Passos:**
1. Localizar o produto "Sauce Labs Backpack"
2. Clicar no botão "Add to cart"

**Resultado esperado:** O ícone do carrinho no topo da página exibe o número "1", indicando 1 item adicionado.

**Status:** ✅ Passou

---

## CT005 - Ordenar produtos por preço (menor para maior)

**Pré-condição:** Usuário logado com sucesso, na página de produtos.

**Passos:**
1. Clicar no menu de ordenação (dropdown no canto superior direito da lista de produtos)
2. Selecionar a opção "Price (low to high)"

**Resultado esperado:** A lista de produtos é reordenada, exibindo o item mais barato primeiro e o mais caro por último.

**Status:** ✅ Passou
