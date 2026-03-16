# 🐛 Relatório de Bugs — Módulo de Login

**Aplicação:** Automation Exercise  
**Módulo:** Login  
**Total de bugs:** 3  
**Status geral:** Aberto

---

## Legenda

| Severidade | Descrição |
|------------|-----------|
| Crítica | Bloqueia completamente o fluxo principal. Impede uso do sistema. |
| Alta | Impacta funcionalidade principal. Workaround difícil ou inexistente. |
| Média | Afeta funcionalidade secundária. Workaround possível. |
| Baixa | Impacto mínimo. Problema cosmético ou de usabilidade. |

| Status | Descrição |
|--------|-----------|
| Aberto | Bug identificado e registrado, aguardando análise. |
| Em correção | Bug em processo de correção pelo time de desenvolvimento. |
| Resolvido | Correção implementada, aguardando validação do QA. |
| Fechado | Bug validado e confirmado como resolvido. |

---

## Resumo

| ID | Título | CT Relacionado | Severidade | Prioridade | Status |
|----|--------|----------------|------------|------------|--------|
| BUG-LOGIN-001 | Mensagem de confirmação de login não exibida após autenticação bem-sucedida | CT-LOGIN-001 | Baixa | Baixa | Aberto |
| BUG-LOGIN-002 | Campos de e-mail, senha e mensagem de erro persistem após atualizar a página | CT-LOGIN-016 | Alta | Alta | Aberto |
| BUG-LOGIN-003 | Sistema não realiza login com e-mail em letras maiúsculas (case-sensitive) | CT-LOGIN-015 | Média | Média | Aberto |

---

## BUG-LOGIN-001 — Mensagem de confirmação de login não exibida após autenticação bem-sucedida

| Campo | Detalhe |
|-------|---------|
| **CT Relacionado** | CT-LOGIN-001 |
| **Tipo** | Usabilidade / Interface |
| **Severidade** | Baixa |
| **Prioridade** | Baixa |
| **Status** | Aberto |
| **Ambiente** | Chrome 144 / Windows 11 |
| **Evidência** | [Anexar screenshot] |

**Descrição**  
Ao realizar login com credenciais válidas, o sistema autentica o usuário com sucesso e redireciona para a página inicial, porém a mensagem "Logged in as [username]" não é exibida, contrariando o critério de aceite definido no CT-LOGIN-001.

**Passos para Reproduzir**  
1. Acessar o site Automation Exercise
2. Clicar na opção Signup / Login
3. Informar um e-mail válido
4. Informar uma senha válida
5. Clicar no botão Login

**Resultado Obtido**  
Login realizado com sucesso, porém a mensagem "Logged in as [username]" não é exibida ao usuário.

**Resultado Esperado**  
Após autenticação bem-sucedida, o sistema deve exibir a mensagem "Logged in as [username]", conforme critério de aceite definido no CT-LOGIN-001.

---

## BUG-LOGIN-002 — Campos de e-mail, senha e mensagem de erro persistem após atualizar a página de login

| Campo | Detalhe |
|-------|---------|
| **CT Relacionado** | CT-LOGIN-016 |
| **Tipo** | Segurança / Funcional |
| **Severidade** | Alta |
| **Prioridade** | Alta |
| **Status** | Aberto |
| **Ambiente** | Google Chrome e Microsoft Edge (versões mais recentes) / Windows |
| **Evidência** | [Anexar screenshot] |

**Descrição**  
Ao preencher os campos de e-mail e senha na página de login e atualizar a página (F5), os dados inseridos e a mensagem de erro anterior não são limpos. O comportamento ocorre nos navegadores Chrome e Microsoft Edge.

**Passos para Reproduzir**  
1. Acessar a página de login do Automation Exercise
2. Preencher o campo e-mail com qualquer valor
3. Preencher o campo senha com qualquer valor
4. Clicar em Login (gera a mensagem de erro)
5. Pressionar F5 para atualizar a página
6. Confirmar o reenvio do formulário no pop-up do navegador

**Resultado Obtido**  
Os campos de e-mail, senha e a mensagem de erro "Your email or password is incorrect!" permanecem visíveis após o refresh. O navegador exibe um pop-up perguntando se deseja reenviar o formulário.

**Resultado Esperado**  
Após atualizar a página, todos os campos devem ser limpos e nenhuma mensagem de erro deve ser exibida. O navegador não deve perguntar sobre reenvio de formulário.

---

## BUG-LOGIN-003 — Sistema não realiza login com e-mail em letras maiúsculas (case-sensitive)

| Campo | Detalhe |
|-------|---------|
| **CT Relacionado** | CT-LOGIN-015 |
| **Tipo** | Funcional |
| **Severidade** | Média |
| **Prioridade** | Média |
| **Status** | Aberto |
| **Ambiente** | Chrome 144 / Windows 11 |
| **Evidência** | [Anexar screenshot] |

**Descrição**  
Ao tentar realizar login com o e-mail cadastrado em letras maiúsculas, o sistema rejeita a autenticação e exibe a mensagem "Your email or password is incorrect!". O sistema está tratando o e-mail como case-sensitive, quando o comportamento esperado é que e-mails sejam aceitos independente de maiúsculas ou minúsculas.

**Passos para Reproduzir**  
1. Acessar o site Automation Exercise
2. Clicar em Signup / Login
3. Informar o e-mail válido com letras maiúsculas
4. Informar a senha válida
5. Clicar no botão Login

**Resultado Obtido**  
Ao inserir o e-mail em letras maiúsculas e clicar em Login, o sistema exibe a mensagem "Your email or password is incorrect!" e bloqueia a autenticação.

**Resultado Esperado**  
O sistema deve autenticar o usuário com sucesso independente de o e-mail estar em maiúsculas ou minúsculas, pois e-mails são case-insensitive por padrão.
