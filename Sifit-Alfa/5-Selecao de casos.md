# Registro de seleção dos casos — Sifit Alfa

**Referência:** planejamento inicial com 53 casos propostos na exploração de 20/10/2026.  
**Seleção:** 27 mantidos e 26 fora da bateria atual.  
**Situação:** seleção concluída; dez casos distintos executados ou tentados em 27/10/2026 (8 passaram, MAT-02 falhou, DASH-01 está bloqueado); demais 17 casos sem execução. CLI-02, MAT-01 e MAT-02 foram repetidos em outra URL, mantendo as primeiras tentativas no histórico.

## 1. Casos mantidos

| ID original | RF | Módulo | Prioridade | Objetivo |
| --- | --- | --- | --- | --- |
| AUT-01 | RF01 | Autenticação | P0 | Login com credenciais válidas |
| AUT-02 | RF01 | Autenticação | P0 | Bloqueio de acesso sem autenticação |
| AUT-03 | RF01 | Autenticação | P1 | Senha incorreta |
| DASH-01 | RF02 | Dashboard | P1 | Consulta por período no painel |
| CLI-01 | RF03 | Clientes | P1 | Pesquisa por nome e código de clientes |
| CLI-02 | RF03 | Clientes | P1 | Cadastro válido de cliente |
| CLI-03 | RF03 | Clientes | P1 | Data de nascimento obrigatória |
| CLI-04 | RF03 | Clientes | P1 | Formatos inválidos de CPF e e-mail |
| CLI-05 | RF03 | Clientes | P1 | Consulta das seções do perfil de cliente |
| MAT-01 | RF04 | Matrículas | P0 | Cadastro válido de matrícula |
| MAT-02 | RF04 | Matrículas | P0 | Período invertido na matrícula |
| AVA-01 | RF05 | Avaliações | P1 | Agendamento válido de avaliação |
| AVA-02 | RF05 | Avaliações | P1 | Avaliação com dados inválidos |
| TUR-01 | RF06 | Turmas | P1 | Cadastro válido de turma |
| TUR-02 | RF06 | Turmas | P1 | Horário inválido em turma |
| CHK-01 | RF07 | Check-in | P0 | Check-in manual válido |
| CHK-02 | RF07 | Check-in | P0 | Check-in com código inválido ou duplicado |
| PRE-01 | RF08 | Presenças | P1 | Consulta de presenças por período |
| FIN-01 | RF09 | Financeiro | P0 | Cadastro de conta a receber |
| FIN-02 | RF09 | Financeiro | P0 | Registro de recebimento |
| FIN-03 | RF09 | Financeiro | P0 | Validação de valores e datas financeiros |
| FIN-07 | RF09 | Financeiro | P1 | Relatório PDF de clientes e contas a receber |
| TRE-01 | RF10 | Treinamento | P1 | Cadastro de ficha de treino |
| COM-02 | RF11 | Comercial | P0 | Cadastro de plano mensal |
| COM-03 | RF11 | Comercial | P1 | Modelo de contrato e variáveis |
| SAU-01 | RF12 | Saúde / Anamnese | P1 | Modelo de anamnese com perguntas |
| SAU-02 | RF12 | Saúde / Anamnese | P1 | Aplicação de anamnese |

## 2. Casos não selecionados e justificativa

| ID original | Caso retirado da execução atual | Justificativa |
| --- | --- | --- |
| NAV-01 | Verificar todos os menus | Rotas já mapeadas na exploração; baixa profundidade funcional para esta bateria. |
| NAV-02 | Diferenciar dashboards | Verificação predominantemente visual; impacto menor no recorte. |
| DASH-02 | Período inválido no painel | Validações negativas de datas já contempladas em módulos principais. |
| MAT-03 | Filtros de matrículas | Consulta de clientes já priorizada nesta bateria; filtros de matrículas fora do recorte. |
| AVA-03 | Alteração de status da avaliação | Exige mudança de estado e preparação adicionais. |
| TUR-03 | Filtro e edição de turma | Cadastro de turma priorizado; edição requer etapa adicional. |
| CHK-03 | Busca, abas e unidade do check-in | Registro válido e inválido recebem prioridade. |
| PRE-02 | Datas inválidas em presenças | Cenário semelhante a outras validações negativas. |
| BOX-01 | Consultar aulas SifitBox | Módulo específico fora do recorte escolhido. |
| BOX-02 | Gerar aulas | Geração pode criar muitos registros e exige controle de duplicidade. |
| BOX-03 | Turmas recorrentes SifitBox | Escopo semelhante ao cadastro básico de turmas; requer preparação. |
| FIN-04 | Contas a pagar | Prioridade ao ciclo de recebimentos ligado à matrícula. |
| FIN-05 | Abrir e fechar caixa | Risco de alterar estado financeiro compartilhado. |
| FIN-06 | Despesas recorrentes | Exige observar regras e lançamentos recorrentes. |
| FIN-08 | Integração Pagar.me | Depende de sandbox e autorização financeira. |
| TRE-02 | Biblioteca de exercícios | Cadastro auxiliar em relação à ficha de treino. |
| TRE-03 | Grupos musculares e categorias | Cadastros auxiliares; recorte prioriza jornada principal. |
| COM-01 | Prospecção de leads | Fluxo comercial não priorizado nesta bateria. |
| COM-04 | Tabelas comerciais auxiliares | Predominância de cadastros auxiliares repetitivos. |
| GES-01 | Colaborador e função | Possível interferência com permissões e contas. |
| GES-02 | Cadastros auxiliares de gestão | Diversas entidades secundárias em um único caso. |
| SAU-03 | Categorias, perguntas e atividades | Cadastro auxiliar; modelo e aplicação de anamnese priorizados. |
| IA-01 | Consulta de resultados de IA | Dependência de resultados e critérios de avaliação não confirmados. |
| IA-02 | Executar automação | Possibilidade de ações e mensagens externas. |
| CFG-01 | Alterar configurações | Risco de modificar opções globais no ambiente compartilhado. |
| APP-01 | Notificação do aplicativo | Possibilidade de envio real e dependência externa. |

> Um caso fora do escopo não é caso aprovado ou reprovado. A retirada limita apenas a bateria da atividade.

## 3. Simplificações já acordadas para execução

- **CLI-04:** somente CPF e e-mail inválidos.
- **PRE-01:** comparar dois períodos conhecidos.
- **FIN-07:** gerar apenas os modelos Clientes e Contas a Receber, entre os sete tipos observados.
- **COM-02:** testar plano mensal, não todas as modalidades de cobrança.
- **SAU-01:** modelo simples com duas ou três perguntas.
- **MAT-02:** recorte executado: período invertido. Valor negativo não foi testado.

## 4. Limite acadêmico

O PDF de instruções do professor orienta replicar a documentação do SIFIT no GitHub conforme o exemplo e usar vídeos como evidência. **Ele não estabelece 27 casos como número obrigatório**; essa quantidade é o recorte escolhido para esta bateria.
