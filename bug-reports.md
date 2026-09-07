# Bug Reports - SauceDemo

Relatórios de bugs identificados durante os testes manuais no e-commerce SauceDemo.

---

## BUG001 - Preço do produto exibido incorretamente após ordenação

**Severidade:** Baixa
**Prioridade:** Média

**Ambiente:** Chrome 152, Windows 11

**Passos para reproduzir:**
1. Fazer login com o usuário `problem_user` / senha `secret_sauce`
2. Na página de produtos, abrir o menu de ordenação
3. Selecionar a opção "Price (low to high)"

**Resultado esperado:** Os produtos devem ser reordenados corretamente do menor para o maior preço.

**Resultado obtido:** A ordenação não funciona - a lista de produtos permanece na ordem original, independente da opção selecionada.

**Evidência:** (aqui entraria um print da tela)

---

## BUG002 - Imagens dos produtos trocadas para usuário "problem_user"

**Severidade:** Média
**Prioridade:** Alta

**Ambiente:** Chrome 152, Windows 11

**Passos para reproduzir:**
1. Fazer login com o usuário `problem_user` / senha `secret_sauce`
2. Observar as imagens dos produtos na página inicial

**Resultado esperado:** Cada produto deve exibir sua imagem correspondente correta.

**Resultado obtido:** Todos os produtos exibem a mesma imagem (foto de um cachorro), o que não corresponde ao produto real anunciado.

**Evidência:** (aqui entraria um print da tela)

---

## BUG003 - Login não permitido para usuário "locked_out_user" sem mensagem clara

**Severidade:** Baixa
**Prioridade:** Baixa

**Ambiente:** Chrome 152, Windows 11

**Passos para reproduzir:**
1. Acessar https://www.saucedemo.com/
2. Preencher usuário `locked_out_user` e senha `secret_sauce`
3. Clicar em "Login"

**Resultado esperado:** Sistema deveria fornecer mais orientação ao usuário sobre como desbloquear a conta (ex: link "Esqueci minha senha" ou contato de suporte).

**Resultado obtido:** Apenas exibe a mensagem "Epic sadface: Sorry, this user has been locked out.", sem nenhuma orientação de próximo passo para o usuário.

**Evidência:** (aqui entraria um print da tela)

**Observação:** Este é um comportamento intencional do site de demonstração (usado propositalmente para prática de QA), documentado aqui apenas como exercício de identificação e registro de bug.
