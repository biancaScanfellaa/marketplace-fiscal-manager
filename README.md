## O que é o Marketplace Fiscal Manager:

O Marketplace Fiscal Manager foi desenvolvido com o objetivo de trazer mais controle, automação e eficiência para a gestão de notas fiscais em operações de e-commerce.

A aplicação centraliza dados de pedidos provenientes de marketplaces como Shopee e Mercado Livre, permitindo a análise, validação e correção de inconsistências fiscais. Além disso, oferece rastreabilidade completa por meio do registro de histórico de alterações, garantindo maior segurança e confiabilidade no processo.

---

## O que motivou a desenvolver o Marketplace Fiscal Manager:

A necessidade surgiu a partir das dificuldades enfrentadas por vendedores em marketplaces na gestão manual de notas fiscais, frequentemente sujeita a erros, retrabalho e falta de controle.

Observamos a ausência de soluções simples e eficientes que integrassem diferentes plataformas e automatizassem processos fiscais, o que motivou o desenvolvimento de uma aplicação focada em organização, precisão e produtividade.

---
## Status do Projeto

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
------------------------------------------------------------------------------------------------
sequenceDiagram
    autonumber
    actor Resp as Responsável CNPJ
    participant Mobile as App Mobile
    participant API as Backend (Manager API)
    participant DB as Banco de Dados

    Resp->>Mobile: Insere credenciais e faz Login
    Mobile->>API: POST /api/auth/login-mobile (Email, Senha)
    
    API->>API: Verifica restrição de horário de acesso
    alt Horário Não Permitido
        API-->>Mobile: Retorna Erro 403 (Acesso bloqueado por horário)
        Mobile-->>Resp: Exibe mensagem de bloqueio temporário
    else Horário Permitido
        API->>DB: Valida credenciais e perfil de usuário
        DB-->>API: Usuário válido (Perfil: Responsável)
        API-->>Mobile: Retorna JWT Token + Permissões de escopo
        Mobile-->>Resp: Redireciona para o Dashboard Mobile
    end

    Resp->>Mobile: Solicita resumo de divergências
    Mobile->>API: GET /api/dashboards/resumo-fiscal (Headers: Bearer JWT)
    API->>DB: Consolida métricas de impostos e divergências
    DB-->>API: Retorna dados agregados
    API-->>Mobile: Envia payload JSON consolidado
    Mobile-->>Resp: Renderiza gráficos de análise fiscal
    -----------------------------------------------------------------------------------
    Cards do Dashboard
    📦 Total de Pedidos📄 Notas Emitidas> ### 1,250RF06 
    • Total de pedidos importados integrados com Shopee e Mercado Livre.> ### 1,180RF07 
    • Notas fiscais geradas e validadas com sucesso no período.Status: 🟢 Atualizado em tempo realStatus: 🟢 Sincronizado
    ⚠️ Notas com Erro⚖️ Divergência de Impostos> ### 42RF08
    • Notas retidas ou com inconsistências de dados cadastrais.> ### R$ 1.450,20RF09 
    • Diferença identificada entre o imposto calculado vs. esperado.Status: 🔴 Requer AtençãoStatus: 🟡 Em Análise
    -----------------------------------------------------------------------------------------------------------------------
    Histórias de Usuário
    
US01 — Sincronização Automática de Vendas
Como Vendedor de Marketplace (Shopee/Mercado Livre);
Eu quero que o sistema importe meus pedidos automaticamente através de API,
Para que eu não precise consolidar os dados manualmente e evite erros de digitação.

Critérios de Aceite:

[ ] O sistema deve permitir salvar os tokens/keys de integração de forma segura.
[ ] A sincronização automática deve rodar em segundo plano periodicamente.
[ ] Caso a API do marketplace falhe, o sistema deve registrar o erro e tentar novamente mais tarde (RNF13).
[ ] Os pedidos importados devem aparecer imediatamente na listagem do Dashboard.

US02 — Identificação e Correção de Divergências Fiscais
Como Analista Fiscal/Vendedor;
Eu quero que o sistema destaque as notas fiscais que possuem erros de impostos ou dados incorretos,
Para que eu possa corrigi-las rapidamente antes de gerar prejuízos ou multas.

Critérios de Aceite:

[ ] O sistema deve calcular automaticamente o imposto esperado com base nas regras cadastradas.
[ ] Notas com divergência entre o valor calculado e o importado devem receber o status "Erro Fiscal" e uma cor de destaque (ex: vermelho).
[ ] Ao corrigir a nota, o sistema deve recalcular os valores em tempo real.
[ ] Toda alteração manual deve salvar um registro com o usuário, data, hora e dado antigo na tabela de Histórico (RNF15).

US03 — Acesso Gerencial Restrito (Mobile)
Como Responsável Legal pelo CNPJ;
Eu quero acessar um resumo de impostos e divergências pelo meu celular em horários controlados,
Para que eu possa acompanhar a saúde fiscal da empresa com segurança e privacidade.

Critérios de Aceite:

[ ] O aplicativo mobile deve restringir o login apenas para usuários com perfil de "Responsável CNPJ".
[ ] A tela mobile deve ser simplificada, exibindo apenas os cards de totalizador de impostos (pagos/pendentes) e gráficos de divergências.
[ ] Se o usuário tentar acessar o aplicativo fora do horário configurado, o sistema deve bloquear o acesso com uma mensagem amigável (RNF11).

US04 — Autenticação e Segurança de Dados
Como Administrador do Sistema / Empresa;
Eu quero que minhas credenciais de marketplace e senhas sejam criptografadas,
Para que dados sensíveis do meu faturamento não fiquem expostos a acessos não autorizados.

Critérios de Aceite:
[ ] As senhas dos usuários devem usar criptografia forte (ex: Bcrypt) antes de irem para o banco de dados.
[ ] Tokens e chaves de API dos marketplaces devem ser armazenados criptografados.
[ ] Toda requisição entre Frontend e Backend deve exigir um token JWT válido no cabeçalho (RNF02).
---------------------------------------------------------------------------------------------------------------------------------------
Protótipos das Telas

<img width="1408" height="768" alt="telas_projeto" src="https://github.com/user-attachments/assets/c3110e01-2679-40a8-bf30-0071137bc15e" />
