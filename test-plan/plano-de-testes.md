# Plano de Testes – Sistema de Login

## 1. Introdução

Este documento descreve o plano de testes para a funcionalidade de login do site **Automation Exercise**,
uma aplicação web pública utilizada para prática e simulação de testes de software.

O objetivo é garantir que o processo de autenticação funcione corretamente, oferecendo segurança,
usabilidade e confiabilidade ao usuário final.

Este plano foi criado simulando um ambiente de desenvolvimento ágil, para fins de estudo e portfólio em QA.
Ele segue boas práticas de teste de software, considerando critérios de qualidade, risco e impacto ao usuário.

---

## 2. Escopo

### 2.1 Funcionalidades que serão testadas

* Login com credenciais válidas
* Login com credenciais inválidas
* Validação de campos obrigatórios (email e senha)
* Exibição de mensagens de erro ao usuário
* Logout do sistema
* Comportamento da sessão após autenticação

### 2.2 Funcionalidades fora do escopo

* Cadastro de novos usuários
* Recuperação de senha
* Funcionalidades de compra e pagamento
* Testes de performance e segurança aprofundados

---

## 3. Tipos de Teste

### 3.1 Testes Funcionais

* Validação do comportamento esperado do sistema
* Verificação das regras de negócio relacionadas ao login

### 3.2 Testes de Regressão

* Garantir que alterações futuras não impactem negativamente a funcionalidade de login

### 3.3 Testes de Usabilidade

* Clareza das mensagens exibidas ao usuário
* Facilidade de uso da tela de login
* Feedback visual adequado em caso de erro

---

## 4. Ambiente de Testes

* Aplicação Web: [Automation Exercise](https://automationexercise.com)
* Tipo de aplicação: Web
* Navegadores testados:

  * Google Chrome
  * Mozilla Firefox
* Sistema Operacional:

  * Windows 10 ou superior
* Ambiente: Produção (site público para prática de testes)

---

## 5. Critérios de Aceite

* O usuário deve conseguir acessar o sistema com credenciais válidas
* O sistema deve impedir acesso com credenciais inválidas
* Mensagens de erro devem ser claras e objetivas
* O sistema não deve permitir login com campos vazios
* A sessão deve ser encerrada corretamente após o logout

---

## 6. Critérios de Entrada

* Funcionalidade de login disponível no ambiente
* Ambiente de testes acessível
* Usuários de teste previamente cadastrados
* Casos de teste documentados

---

## 7. Critérios de Saída

* Todos os casos de teste planejados executados
* Defeitos encontrados devidamente registrados
* Evidências de teste documentadas
* Resultados consolidados e revisados

---

## 8. Riscos

* Ausência de documentação formal de requisitos
* Mudanças frequentes nas regras de negócio
* Instabilidade do ambiente público de testes
* Limitações por se tratar de um ambiente não controlado

---

## 9. Responsáveis

* **QA:** Responsável pelo planejamento, execução e reporte dos testes
* **Desenvolvedor:** Responsável pela análise e correção dos defeitos encontrados
* **Product Owner:** Responsável pela validação dos critérios de aceite e priorização de correções
