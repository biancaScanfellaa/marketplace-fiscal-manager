## O que é o Marketplace Fiscal Manager:

O Marketplace Fiscal Manager foi desenvolvido com o objetivo de trazer mais controle, automação e eficiência para a gestão de notas fiscais em operações de e-commerce.

A aplicação centraliza dados de pedidos provenientes de marketplaces como Shopee e Mercado Livre, permitindo a análise, validação e correção de inconsistências fiscais. Além disso, oferece rastreabilidade completa por meio do registro de histórico de alterações, garantindo maior segurança e confiabilidade no processo.

---

## O que motivou a desenvolver o Marketplace Fiscal Manager:

A necessidade surgiu a partir das dificuldades enfrentadas por vendedores em marketplaces na gestão manual de notas fiscais, frequentemente sujeita a erros, retrabalho e falta de controle.

Observamos a ausência de soluções simples e eficientes que integrassem diferentes plataformas e automatizassem processos fiscais, o que motivou o desenvolvimento de uma aplicação focada em organização, precisão e produtividade.

---
## 🚧 Status do Projeto

*Status:* Em desenvolvimento

---

## ⚙ Funcionalidades e Demonstração da Aplicação

### Funcionalidades Principais

* Cadastro e autenticação de usuários
* Importação e centralização de pedidos de marketplaces
* Análise e validação de notas fiscais
* Identificação de inconsistências fiscais
* Correção de dados com registro de histórico
* Geração de relatórios e métricas operacionais
* Interface responsiva para diferentes dispositivos

Requisitos funcionais 

Autenticação e Usuário
RF01 – O sistema deve permitir o cadastro de usuários com nome, e-mail e senha.
RF02 – O sistema deve permitir o cadastro de usuários do tipo Pessoa Física ou Empresa.
RF03 – O sistema deve solicitar CNPJ ao selecionar conta do tipo Empresa.
RF04 – O sistema deve permitir login com e-mail e senha.
RF05 – O sistema deve permitir logout do usuário.

Dashboard
RF06 – O sistema deve exibir o total de pedidos.
RF07 – O sistema deve exibir o total de notas fiscais emitidas.
RF08 – O sistema deve exibir o total de notas com erro.
RF09 – O sistema deve exibir divergências de impostos.
RF10 – O sistema deve apresentar gráficos de notas por período.
RF11 – O sistema deve apresentar gráficos de erros por tipo.

Gestão de Notas Fiscais
RF12 – O sistema deve listar notas fiscais importadas.
RF13 – O sistema deve identificar inconsistências nas notas fiscais.
RF14 – O sistema deve destacar erros encontrados.
RF15 – O sistema deve permitir visualizar detalhes da nota fiscal.
Controle de Impostos

RF16 – O sistema deve calcular impostos automaticamente.
RF17 – O sistema deve identificar divergências entre valores esperados e calculados.
RF18 – O sistema deve exibir histórico de validações.
 Relatórios
RF19 – O sistema deve gerar relatório mensal.
RF20 – O sistema deve permitir filtrar por mês.
RF21 – O sistema deve permitir filtrar por marketplace.
RF22 – O sistema deve exibir indicadores (notas, erros, impostos).
RF23 – O sistema deve apresentar gráficos de análise.
RF24 – O sistema deve exibir tabela resumo consolidada.

Integrações
RF25 – O sistema deve permitir integração com APIs externas.
RF26 – O sistema deve permitir inserir credenciais (token, key).
RF27 – O sistema deve importar pedidos automaticamente.
RF28 – O sistema deve sincronizar dados manualmente.
RF29 – O sistema deve analisar dados importados automaticamente.

Mobile (Responsável pelo CNPJ)
RF30 – O sistema deve permitir login restrito ao responsável pelo CNPJ.
RF31 – O sistema deve restringir acesso às funcionalidades.
RF32 – O sistema deve exibir resumo de impostos pagos e pendentes.
RF33 – O sistema deve exibir divergências fiscais.
RF34 – O sistema deve permitir visualizar detalhes das inconsistências.
RF35 – O sistema deve restringir acesso por horário.

Requisitos não funcionais 

Segurança
RNF01 – O sistema deve criptografar senhas dos usuários.
RNF02 – O sistema deve utilizar autenticação segura (ex: JWT).
RNF03 – O sistema deve proteger dados sensíveis (CNPJ, tokens).
RNF04 – O sistema deve controlar acesso por perfil de usuário.

 Desempenho
RNF05 – O sistema deve responder requisições em até 3 segundos.
RNF06 – O sistema deve suportar múltiplos usuários simultâneos.

Usabilidade
RNF07 – O sistema deve possuir interface intuitiva.
RNF08 – O sistema deve ser responsivo (desktop e mobile).
RNF09 – O sistema mobile deve ser simples e objetivo.

Disponibilidade
RNF10 – O sistema deve estar disponível 24/7 (exceto manutenção).
RNF11 – O sistema deve permitir acesso mobile em horários controlados.

Integração
RNF12 – O sistema deve ser compatível com APIs REST.
RNF13 – O sistema deve tratar falhas de integração.

 Banco de Dados
RNF14 – O sistema deve garantir integridade dos dados.
RNF15 – O sistema deve armazenar histórico de alterações.

Escalabilidade
RNF16 – O sistema deve permitir crescimento de dados sem perda de desempenho.
[Usuário]
   |
   |----> Cadastrar conta
   |----> Fazer login
   |----> Conectar APIs (Shopee/Mercado Livre)
   |----> Visualizar dashboard
   |----> Consultar notas fiscais
   |----> Ver erros fiscais
   |----> Corrigir inconsistências
   |----> Gerar relatório mensal

[Responsável CNPJ]
   |
   |----> Fazer login (restrito)
   |----> Consultar impostos
   |----> Ver divergências

[Sistema]
   |
   |----> Importar pedidos (API)
   |----> Analisar notas automaticamente
   |----> Identificar erros
   |----> Gerar relatóriosUsuário]
   |
   |----> Cadastrar conta
   |----> Fazer login
   |----> Conectar APIs (Shopee/Mercado Livre)
   |----> Visualizar dashboard
   |----> Consultar notas fiscais
   |----> Ver erros fiscais
   |----> Corrigir inconsistências
   |----> Gerar relatório mensal

[Responsável CNPJ]
   |
   |----> Fazer login (restrito)
   |----> Consultar impostos
   |----> Ver divergências

[Sistema]
   |
   |----> Importar pedidos (API)
   |----> Analisar notas automaticamente
   |----> Identificar erros
   |----> Gerar relatóriosUsuário]
   |
   |----> Cadastrar conta
   |----> Fazer login
   |----> Conectar APIs (Shopee/Mercado Livre)
   |----> Visualizar dashboard
   |----> Consultar notas fiscais
   |----> Ver erros fiscais
   |----> Corrigir inconsistências
   |----> Gerar relatório mensal


