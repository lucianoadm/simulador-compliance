# LexOS — Ecossistema de Governança Preditiva & Jurimetria 4.0

> **Status do Projeto:** Prova de Conceito (PoC) / Protótipo Palpável  
> **Ambiente:** Front-end Independente (Hospedagem via GitHub Pages)  
> **Segurança da API:** Modelo de Chave Volátil (`sessionStorage`) — Sem persistência ou exposição de credenciais no código-fonte.

---

## 📌 Contexto e Propósito Científico

O **LexOS (Cognivus Ecosystem)** é a materialização prática, funcional e visual do arcabouço teórico submetido à **IV Mostra Científica de Direito na Escola** (conforme diretrizes e regulamento oficial do programa). Este simulador serve como a **prova viva e palpável** da aplicação prática de *Data Science*, *Business Intelligence* e *IA Explicável (XAI)* ao Direito Regulatório e à Governança Corporativa.

O ecossistema demonstra como transformar dados brutos de incidentes e procedimentos jurídicos em relatórios técnicos defensáveis, mitigando riscos de sanções através de uma arquitetura ancorada em evidências matemáticas e regras claras de decisão (Árvore J48 do Weka).

---

## 🤖 Pilares Arquiteturais do Sistema

O simulador é dividido de forma linear e modular em 3 pilares estratégicos, espelhando o fluxo de um departamento de governança moderno:

### 📊 Pilar 1: Dashboard Analítico (Motor R)
* **Visibilidade Jurimétrica:** Renderização dinâmica da volumetria estrutural baseada em arquivos `.csv` reais gerados via scripts de ETL em R.
* **Gráficos Interativos:** Distribuição de incidentes online por categoria e canais de origem utilizando a biblioteca `Chart.js`.
* **Amostragem em Tempo Real:** Tabela interativa contendo a listagem completa dos casos para seleção e auditoria pontual.

### 🧠 Pilar 2: Previsibilidade Dinâmica (Weka XAI — IA Explicável)
* **Lógica de Decisão Determinística:** Alimentado pelo mapeamento lógico gerado pelo modelo de árvore de decisão J48 do Weka.
* **Transparência Algorítmica:** O sistema afasta o conceito de "caixa-preta" das IAs tradicionais, aplicando regras claras baseadas na probabilidade de perda para categorizar os riscos:
    * `probabilidade_perda <= 0.49` ➡️ **Baixo_Risco (Zona de Conformidade)**
    * `probabilidade_perda > 0.49` e `<= 0.74` ➡️ **Medio_Risco**
    * `probabilidade_perda > 0.74` ➡️ **Alto_Risco_Sancao (Risco Crítico)**
* **Simulador Cognitivo:** Permite testar cenários modificando variáveis e probabilidades na hora.

### 📜 Pilar 3: Relatório Defensável & Engenharia Reversa (OpenAI API)
* **Auditoria Cognitiva Real:** Integração direta com a API da OpenAI (`gpt-4o-mini`) utilizando o modo `json_object` estrito para erradicar alucinações textuais.
* **Geração Automatizada:** Produz pareceres técnicos contendo diagnóstico estrutural, análise preditiva, teses defensivas personalizadas e planos de contingência em formato pronto para impressão (PDF corporativo).
* **Mecanismo Fallback:** Caso nenhuma chave de API seja inserida, o sistema conta com um motor local de templates estáticos, mantendo o simulador 100% funcional para demonstrações offline.

---

## 🔐 Política de Segurança & Blindagem da API

Como este repositório foi desenhado para fins de **apresentação acadêmica, validação e uso estrito**, adotou-se a estratégia de **Sessão Volátil**:
1.  **Chave Oculta:** Nenhuma chave de API ou credencial privada está salva no código-fonte, histórico do Git ou arquivos de configuração deste repositório.
2.  **Injeção em Tempo de Execução:** Ao iniciar o simulador ou disparar o motor de IA, o sistema solicita a chave do usuário por meio de um fluxo seguro temporário.
3.  **Memória Temporária (`sessionStorage`):** A chave inserida permanece viva apenas no contexto da aba atual do navegador. Assim que a aba ou o navegador é fechado, o dado é permanentemente destruído da memória local, impedindo vazamentos ou uso indevido de terceiros.

---

## 🛠️ Tecnologias Utilizadas

* **HTML5 & CSS3** (Customização Semântica e Design Fluido)
* **Tailwind CSS** (Framework utilitário para a interface executiva)
* **JavaScript (ES6+)** (Manipulação assíncrona, FileReader API e chamadas REST)
* **Chart.js** (Visualização de dados analíticos)
* **OpenAI API** (Engine de processamento de linguagem natural corporativa)

---

## 🚀 Como Executar o Simulador

Por ser um sistema construído sobre uma arquitetura puramente cliente-servidor (Serverless Front-end), a execução é extremamente simples:

1.  Faça o clone do repositório ou baixe o arquivo fonte.
2.  Abra o arquivo `index.html` em qualquer navegador moderno (Chrome, Edge, Firefox).
3.  Carregue o arquivo de dados padronizado (`dados_lexos_piloto.csv`).
4.  Para utilizar as funções avançadas de IA, clique no botão **"Configurar Chave OpenAI"** no painel lateral e insira um token válido. Para demonstrações rápidas, utilize o sistema sem chave para rodar o modo de simulação preditiva local.

---

### 📝 Créditos e Desenvolvimento
* **Projeto:** Ecossistema Cognivus — Subprojeto LexOS
* **Autor/Desenvolvedor:** Luciano P. de Moura  
* **Ancoragem Acadêmica:** IV Mostra Científica de Direito na Escola (2026)

---
*Este software é um protótipo funcional acadêmico de uso restrito, desenvolvido para provar a viabilidade técnica da jurimetria e ciência de dados aplicada aos sistemas de governança corporativa e conformidade legal.*
