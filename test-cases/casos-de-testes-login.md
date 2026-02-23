# 🧪 Casos de Teste — Módulo de Login

**Aplicação:** Automation Exercise  
**Módulo:** Login  
**Total de casos:** 15  
**Status geral:** Não executado

---

## Legenda

| Tipo | Descrição |
|------|-----------|
| Funcional | Valida comportamento esperado do sistema |
| Negativo | Valida rejeição de entradas inválidas |
| Limite | Valida comportamento nos limites de entrada |

---

## Casos de Teste

| ID | Tipo | Severidade | Título | Pré-condição | Passos | Resultado Esperado | Status |
|----|------|------------|--------|--------------|--------|--------------------|--------|
| CT-LOGIN-001 | Funcional | Alta | Realizar login com credenciais válidas | Usuário cadastrado; Não autenticado | 1. Acessar o site Automation Exercise 2. Clicar em Signup / Login 3. Informar e-mail válido 4. Informar senha válida 5. Clicar em Login | Sistema autentica o usuário. Redireciona para home. Exibe: `Logged in as [username]` | Não executado |
| CT-LOGIN-002 | Negativo | Alta | Tentar login com senha inválida | Usuário cadastrado; Não autenticado | 1. Acessar o site 2. Clicar em Signup / Login 3. Informar e-mail válido 4. Informar senha inválida 5. Clicar em Login | Login bloqueado. Mensagem de erro exibida. | Não executado |
| CT-LOGIN-003 | Negativo | Alta | Tentar login sem preencher e-mail e senha | Usuário cadastrado; Não autenticado | 1. Acessar o site 2. Clicar em Signup / Login 3. Não preencher campos 4. Clicar em Login | Login bloqueado. Mensagem de campos obrigatórios exibida. | Não executado |
| CT-LOGIN-004 | Funcional | Alta | Realizar login após logout | Usuário cadastrado; Autenticado | 1. Estar logado 2. Clicar em Logout 3. Confirmar deslogamento 4. Acessar Signup / Login 5. Informar e-mail e senha válidos 6. Clicar em Login | Sistema autentica com sucesso. Exibe: `Logged in as [username]` | Não executado |
| CT-LOGIN-005 | Negativo | Alta | Tentar login com e-mail não cadastrado | Não autenticado | 1. Acessar o site 2. Clicar em Signup / Login 3. Informar e-mail não cadastrado 4. Informar senha válida 5. Clicar em Login | Login bloqueado. Exibe: `Email ou senha inválidos` | Não executado |
| CT-LOGIN-006 | Limite | Média | Login com e-mail contendo espaços antes/depois | Usuário cadastrado; Não autenticado | 1. Acessar o site 2. Clicar em Signup / Login 3. Preencher e-mail com espaço no início ou fim 4. Preencher senha válida 5. Clicar em Login | Sistema realiza trim no e-mail. Login bem-sucedido se credenciais válidas. | Não executado |
| CT-LOGIN-007 | Funcional | Alta | Realizar logout após login com sucesso | Usuário cadastrado; Autenticado | 1. Estar logado 2. Clicar em Logout | Usuário deslogado. Opção Signup/Login exibida. Mensagem `Logged in as` removida. | Não executado |
| CT-LOGIN-008 | Negativo | Alta | Tentar login com e-mail e senha inválidos | Não autenticado | 1. Acessar o site 2. Clicar em Signup / Login 3. Preencher e-mail inválido 4. Preencher senha inválida 5. Clicar em Login | Login bloqueado. Exibe: `Email ou senha inválidos` | Não executado |
| CT-LOGIN-009 | Funcional | Média | Login com senha contendo caracteres especiais | Usuário cadastrado com senha especial; Não autenticado | 1. Acessar o site 2. Clicar em Signup / Login 3. Informar e-mail válido 4. Informar senha com especiais (ex: `Senha@123`) 5. Clicar em Login | Sistema autentica com sucesso. Exibe: `Logged in as [username]` | Não executado |
| CT-LOGIN-010 | Negativo | Média | Login com senha contendo apenas caracteres especiais | Não autenticado | 1. Acessar o site 2. Clicar em Signup / Login 3. Informar e-mail válido 4. Informar senha só com especiais (ex: `@#$%`) 5. Clicar em Login | Login bloqueado. Mensagem de erro exibida. | Não executado |
| CT-LOGIN-011 | Funcional | Baixa | Login após atualizar a página (F5) | Usuário cadastrado; Não autenticado | 1. Acessar o site 2. Clicar em Signup / Login 3. Atualizar a página (F5) 4. Informar e-mail válido 5. Informar senha válida 6. Clicar em Login | Sistema autentica com sucesso após refresh. Exibe: `Logged in as [username]` | Não executado |
| CT-LOGIN-012 | Negativo | Alta | Login com e-mail preenchido e senha vazia | Não autenticado | 1. Acessar o site 2. Clicar em Signup / Login 3. Informar e-mail válido 4. Deixar senha vazia 5. Clicar em Login | Login bloqueado. Mensagem de senha obrigatória exibida. | Não executado |
| CT-LOGIN-013 | Limite | Média | Login com e-mail no limite máximo de caracteres | Não autenticado | 1. Acessar o site 2. Clicar em Signup / Login 3. Informar e-mail com máx. de caracteres 4. Informar senha válida 5. Clicar em Login | Mensagem de erro de limite. Usuário permanece na página de login. Sem erros técnicos. | Não executado |
| CT-LOGIN-014 | Negativo | Alta | Login com e-mail sem @ (formato inválido) | Não autenticado | 1. Acessar o site 2. Clicar em Signup / Login 3. Informar e-mail sem @ 4. Informar senha válida 5. Clicar em Login | Login bloqueado. Campo indica formato inválido. Usuário permanece na página. | Não executado |
| CT-LOGIN-015 | Limite | Média | Login com e-mail em letras maiúsculas | Usuário cadastrado; Não autenticado | 1. Acessar o site 2. Clicar em Signup / Login 3. Informar e-mail em maiúsculas 4. Informar senha válida 5. Clicar em Login | Sistema trata e-mail como case-insensitive. Login bem-sucedido. Exibe: `Logged in as [username]` | Não executado |
