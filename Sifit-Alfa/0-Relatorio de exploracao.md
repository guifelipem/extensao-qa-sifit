# Relatório de exploração funcional — Sifit Alfa

**Data da exploração:** 20/10/2026 (America/Sao_Paulo)  
**Sistema:** [Sifit Alfa](https://sifitalfa.centrion.com.br/dashboard)  
**Ambiente:** sessão autenticada com credenciais de demonstração; credenciais não incluídas.  
**Método:** navegação exploratória pela interface.  
**Execução formal de testes:** não iniciada.

## 1. Alcance observado

Conforme o relatório de exploração fornecido, **44 rotas do menu principal** foram abertas, juntamente com telas/formulários adicionais de cadastro e detalhe, e modais. A tabela abaixo apresenta **46 entradas de inventário** (não 46 rotas de menu), pois algumas entradas descrevem formulários e páginas adicionais ou agrupam mais de uma rota. A exploração observou interfaces e controles; não comprovou sua persistência, validações e efeitos.

## 2. Classificação da evidência

- **V — verificado visualmente:** telas, textos e controles exibidos.
- **P — proposto para teste:** comportamento esperado sugerido pela interface, ainda não comprovado.
- **L — limitado:** resultado depende de operação, permissão ou serviço externo não testado.

## 3. Inventário das telas exploradas

| Área | Tela | Rota observada | Elementos observados (V; comportamento P/L) |
| --- | --- | --- | --- |
| Principal | Página Inicial | /dashboard | Resumo, filtros de período, indicadores e atalhos |
| Principal | Dashboard | /dash | Gráficos e botão Ver Inteligência |
| Principal | Check-in | /checkin | Unidade, abas, busca e entrada rápida por código/QR |
| Principal | Presenças | /presencas | Consulta por cliente e período, indicadores e Relatório |
| Principal | SifitBox — Aulas | /sifitbox/aulas | Consulta de período e ação Gerar aulas |
| Operação | Clientes | /clientes | Busca, filtros, paginação, novo, visualizar e excluir |
| Operação | Cadastrar Cliente | /adicionar-cliente | Dados pessoais, contatos, biometria e campos obrigatórios indicados |
| Operação | Detalhe do Cliente | /visualizar-cliente/408 | Perfil, avaliação, pagamentos, matrícula, presenças e financeiro |
| Operação | Matrículas | /matriculas; /adicionar-matricula | Consulta e formulário de matrícula |
| Operação | Avaliações | /avaliacoes | Consulta, cadastro, importação e ações por avaliação |
| Operação | Turmas | /turmas | Listagem e cadastro com plano, horário, personal e dias |
| Financeiro | Contas a Receber | /contas-receber | Consulta e modal Nova Conta |
| Financeiro | Contas a Pagar | /contas-pagar | Consulta e Nova Conta |
| Financeiro | Caixas | /caixas | Consulta de estados e Abrir Caixa |
| Financeiro | Pagar.me | /pagarme | Saldos e atalhos; integração não confirmada |
| Financeiro | Despesas Fixas | /despesas-fixas | Busca, recorrência e Nova Despesa |
| Financeiro | Relatórios | /relatorios | Seleção de sete modelos e saída PDF indicada |
| Treinamento | Fichas de Treino | /fichas-treino | Busca e cadastro de ficha |
| Treinamento | Exercícios | /exercicios | Biblioteca por grupo muscular e Adicionar |
| Treinamento | Grupos Musculares | /grupos-musculares | Busca, tipo e cadastro |
| Treinamento | Objetivos Treino | /objetivos-treino | Busca e Novo Objetivo |
| Treinamento | Categorias Crossfit | /categorias-exercicios-crossfit | Busca e Nova Categoria |
| Treinamento | Box — Turmas | /sifitbox/turmas | Modalidade, turma recorrente e vagas |
| Comercial | Prospecção | /prospeccao | Lead, estágio e Adicionar Lead |
| Comercial | Grupos | /grupos | Busca e Novo Grupo |
| Comercial | Planos | /planos | Busca, ranking e Novo Plano; cobranças e valores |
| Comercial | Modelos Contrato | /modelos-contrato; /adicionar-modelo-contrato | Editor, variáveis e prévia |
| Comercial | Tipos de Pagamento | /tipos-pagamento | Busca e cadastro |
| Comercial | Bandeiras | /bandeiras | Busca e Nova Bandeira |
| Gestão | Colaboradores | /colaboradores; /adicionar-colaborador | Busca, cadastro e função de login |
| Gestão | Funções | /funcoes | Busca, tipo e Nova Função |
| Gestão | Fornecedores | /fornecedores | Busca e Novo Fornecedor |
| Gestão | Tipos de Documentos | /tipos-documento | Busca e Novo Tipo |
| Gestão | Pontuação | /pontuacao | Busca, indicadores e Nova Pontuação |
| Gestão | Produtos | /produtos | Busca e Novo Produto |
| Gestão | Enquetes | /enquetes | Busca, respostas e Nova Enquete |
| Saúde | Fichas de Anamnese | /anamneses | Busca, status e Nova Anamnese |
| Saúde | Modelos de Anamnese | /anamnese/modelos; /anamnese/modelos/novo | Editor com ordem e perguntas obrigatórias |
| Saúde | Categorias Anamnese | /anamnese/categorias | Busca e Nova Categoria |
| Saúde | Perguntas Anamnese | /perguntas-anamnese | Busca e Nova Pergunta |
| Saúde | Atividades | /atividades | Busca e Nova Atividade |
| Inteligência | Inteligência & Automação | /inteligencia-automacao | Ativação, execução e resultados; ações não testadas |
| Inteligência | Resultados IA | /inteligencia/resultados | Filtros temporais e indicadores |
| Configurações | Configurações | /configuracoes | Abas e controles de Cancelar/Salvar |
| Configurações | Modelo Ficha | /fichas-treino-modelo | Busca e Nova Ficha |
| Configurações | Aplicativo | /aplicativo | Notificações, postagens, denúncias e listas |

> A numeração `/visualizar-cliente/408` identifica apenas a rota observada durante a exploração, não um ID obrigatório para os testes. Todos os comportamentos descritos a partir de controles da interface são P até execução.

## 4. Observações verificadas (sem resultado formal de teste)

- Sem sessão, `/dashboard` redirecionou para `/login`; a autenticação com credenciais fornecidas abriu o painel. O caso AUT-01 permanece **não executado formalmente**.
- Os 44 destinos do menu abriram telas na sessão autenticada; existem Página Inicial (`/dashboard`) e Dashboard (`/dash`).
- Existem filtros de clientes, matrículas e outras listas, além de controles de paginação observados.
- No cadastro de cliente, Nome, Status, Sexo e Data de Nascimento aparecem com `*`. Isso não comprova validação de servidor.
- No cadastro de modelo de anamnese, Nome do Modelo aparece com `*`.
- No módulo Contas a Receber, o modal Nova Conta apareceu com status “Recebido” selecionado; isso é **ponto para investigar**, não bug confirmado.
- Algumas páginas exibiam “Carregando...” ou `0` transitório; não usar números intermediários como evidência de valor final.
- O painel Pagar.me exibiu campos com `--` e carregamento; integração financeira não foi verificada.
- Nenhuma ação de criar, atualizar, excluir, cobrar, registrar presença, enviar mensagem, executar automação ou realizar transação foi executada na exploração.

## 5. Limitações

Persistência, permissões por papel, cálculos, importações, PDFs, integrações Pagar.me, QR/biometria, mensagens, notificações e automações ainda dependem de testes futuros. A exploração ocorreu em sessão controlada pelo navegador integrado; a aba Chrome previamente aberta não ficou disponível para controle confiável.

## 6. Próxima etapa

Executar os **27 casos selecionados**, com autorização, massa de teste fictícia, regras de negócio confirmadas e evidências próprias. A exploração não equivale à aprovação de nenhum caso.
