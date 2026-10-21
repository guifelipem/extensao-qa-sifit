## **Análise de requisitos candidatos — Sifit Alfa**

**Origem:** relatório de exploração de 20/10/2026.  
**Status:** requisitos e critérios de aceitação **inferidos dos controles observados**, ainda não validados com especificação formal do produto. Não representam garantias de funcionamento.

---

### **RF01 — Login e proteção de rotas**

**Módulo:** Autenticação  
**Comportamento a verificar:** Login com credenciais válidas, redirecionamento ao login sem sessão e tratamento de senha incorreta.  
**Evidência disponível:** Login e redirecionamento foram observados apenas durante a exploração.  
**Casos planejados:** AUT-01, AUT-02, AUT-03.

---

### **RF02 — Consulta de indicadores por período**

**Módulo:** Página Inicial  
**Comportamento a verificar:** Seleção de datas/período e consulta de cartões e listas correspondentes.  
**Evidência disponível:** Controles de período e indicadores foram visualizados.  
**Casos planejados:** DASH-01.

---

### **RF03 — Listagem, cadastro e vínculo**

**Módulo:** Clientes  
**Comportamento a verificar:** Busca e filtros, cadastro com campos obrigatórios, formatos de dados e perfil relacionado.  
**Evidência disponível:** Formulário, marcações `*`, filtros e perfil observados; persistência não verificada.  
**Casos planejados:** CLI-01 a CLI-05.

---

### **RF04 — Cadastro e dados consistentes**

**Módulo:** Matrículas  
**Comportamento a verificar:** Registrar cliente/plano/período/valores e tratar períodos ou valores inválidos.  
**Evidência disponível:** Formulário e campos visualizados.  
**Casos planejados:** MAT-01, MAT-02.

---

### **RF05 — Agendamento e validações**

**Módulo:** Avaliações  
**Comportamento a verificar:** Cadastrar avaliação por aluno/personal/data/hora e rejeitar entradas inconsistentes.  
**Evidência disponível:** Modal e campos observados.  
**Casos planejados:** AVA-01, AVA-02.

---

### **RF06 — Cadastro e horários**

**Módulo:** Turmas  
**Comportamento a verificar:** Registrar turmas com plano, horário/dias e tratar entradas inválidas.  
**Evidência disponível:** Modal e seletores observados.  
**Casos planejados:** TUR-01, TUR-02.

---

### **RF07 — Registro de entrada**

**Módulo:** Check-in  
**Comportamento a verificar:** Entrada rápida por código e tratamento de tentativas inválidas/duplicadas.  
**Evidência disponível:** Tela e controles de entrada observados; registro não executado.  
**Casos planejados:** CHK-01, CHK-02.

---

### **RF08 — Consultas por período**

**Módulo:** Presenças  
**Comportamento a verificar:** Filtrar presença por cliente e intervalo e consultar indicadores.  
**Evidência disponível:** Filtros e indicadores observados.  
**Casos planejados:** PRE-01.

---

### **RF09 — Contas a receber e relatórios**

**Módulo:** Financeiro  
**Comportamento a verificar:** Cadastro, recebimento, validação de dados financeiros e geração de PDFs.  
**Evidência disponível:** Modal Nova Conta e sete tipos de relatório visualizados; geração não testada.  
**Casos planejados:** FIN-01, FIN-02, FIN-03, FIN-07.

---

### **RF10 — Ficha de treino**

**Módulo:** Treinamento  
**Comportamento a verificar:** Criar ficha associada a cliente/exercícios, consultar status e validade.  
**Evidência disponível:** Busca/cadastro e biblioteca de exercícios observados.  
**Casos planejados:** TRE-01.

---

### **RF11 — Planos e contratos**

**Módulo:** Comercial  
**Comportamento a verificar:** Cadastro de plano mensal e uso de variáveis no modelo de contrato.  
**Evidência disponível:** Modal de plano e editor de contratos observados.  
**Casos planejados:** COM-02, COM-03.

---

### **RF12 — Modelo e aplicação**

**Módulo:** Anamnese  
**Comportamento a verificar:** Montar perguntas e aplicar anamnese vinculada a cliente/modelo.  
**Evidência disponível:** Editor e telas de anamnese observados.  
**Casos planejados:** SAU-01, SAU-02.

---

**Nota:** quando a regra de negócio não está descrita na interface (por exemplo, limites de desconto, unicidade de presença ou valores financeiros), o resultado esperado deve ser confirmado com o responsável pelo sistema antes de classificar um comportamento como defeito.
