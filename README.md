# 📊 Miniguia de Estudos — Análise de Dados Aplicada à Logística

Projeto desenvolvido para explorar o uso de **Inteligência Artificial aplicada à aprendizagem**, utilizando o **NotebookLM**, técnicas de **Engenharia de Prompts** e curadoria de fontes acadêmicas abertas.

O tema escolhido foi **Análise de Dados Aplicada à Logística e Gestão de Estoques**, com foco na utilização de dados e indicadores para apoiar decisões relacionadas ao planejamento e controle de estoques.

---

## 🎯 Objetivo do Projeto

O objetivo deste projeto é utilizar Inteligência Artificial como ferramenta de apoio ao estudo e à consolidação de conhecimento sobre gestão de estoques.

Durante o desenvolvimento foram utilizadas fontes acadêmicas e técnicas no NotebookLM para:

* estudar conceitos relacionados à gestão de estoques;
* analisar indicadores logísticos;
* compreender métodos de previsão de demanda;
* estudar estoque de segurança e ponto de reposição;
* analisar cobertura e acuracidade de estoque;
* experimentar diferentes estratégias de Engenharia de Prompts;
* documentar erros e melhorias realizadas nos prompts;
* construir um miniguia reutilizável para futuras revisões.

---

## 🧠 Temas Estudados

O estudo foi concentrado principalmente nos seguintes conceitos:

* Previsão de Demanda;
* Média Móvel;
* Média Móvel Ponderada;
* Suavização Exponencial;
* Estoque de Segurança;
* Lead Time;
* Ponto de Reposição;
* Cobertura de Estoque;
* Giro de Estoque;
* Acuracidade;
* Inventário Físico;
* Curva ABC;
* Lote Econômico de Compra.

---

## 📚 Curadoria de Fontes

Foram selecionadas fontes abertas relacionadas à logística, gestão de materiais e análise quantitativa de estoques.

Os documentos foram adicionados ao NotebookLM e utilizados como base documental para os experimentos.

➡️ [Consultar as fontes utilizadas](fontes/fontes.md)

---

## 🤖 Engenharia de Prompts

Um dos principais objetivos do projeto foi compreender como diferentes formas de elaborar uma pergunta podem alterar a qualidade da resposta produzida por uma IA.

O primeiro experimento utilizou um prompt genérico:

> Explique os principais conceitos de gestão de estoques e como a análise de dados pode contribuir para uma operação logística.

Embora a resposta apresentasse informações relevantes, o resultado expandiu o escopo para diversos assuntos da logística que não eram o foco principal do estudo.

O prompt foi então refinado com:

* delimitação do contexto;
* definição do escopo;
* estrutura obrigatória da resposta;
* solicitação de fórmulas;
* exemplos práticos;
* restrição às fontes;
* identificação de limitações.

A mudança produziu respostas mais direcionadas, estruturadas e rastreáveis.

➡️ [Consultar os experimentos e troubleshooting](prompts/troubleshooting.md)

---

## 🩹 Cicatrizes do Projeto

Nem todas as etapas funcionaram corretamente na primeira tentativa.

Entre os problemas encontrados durante o desenvolvimento estão:

### Carregamento das fontes

Alguns links de documentos não foram processados diretamente pelo NotebookLM.

**Solução:** os arquivos foram baixados em PDF e posteriormente enviados manualmente para o notebook.

### Prompt excessivamente genérico

O primeiro prompt produziu uma resposta tecnicamente válida, porém muito ampla.

**Solução:** o prompt foi reformulado definindo explicitamente os conceitos que deveriam ser analisados, o formato esperado e as restrições de utilização das fontes.

Essas dificuldades foram registradas porque representam parte importante do processo de aprendizagem.

---

## 📖 Miniguia Final

Como resultado do estudo foi produzido um miniguia estruturado sobre **Análise de Dados Aplicada à Gestão de Estoques**.

O material aborda:

1. Introdução à gestão de estoques;
2. Previsão de demanda;
3. Estoque de segurança;
4. Ponto de reposição;
5. Cobertura de estoque;
6. Acuracidade;
7. Relação entre os indicadores;
8. Glossário;
9. Resumo para revisão.

➡️ [Acessar o Miniguia de Estudos](miniguia/resumo.md)

---

## 🔄 Prompts Reutilizáveis

Durante o projeto também foi construída uma biblioteca de prompts que pode ser utilizada em futuros estudos.

Entre eles estão prompts para:

* resumir conteúdos;
* aprofundar conceitos;
* identificar fórmulas;
* comparar conceitos;
* criar exemplos práticos;
* gerar simulados;
* testar conhecimento;
* identificar limitações das fontes;
* relacionar indicadores;
* realizar revisões rápidas.

➡️ [Consultar os Prompts Reutilizáveis](prompts/prompts_reutilizaveis.md)

---

## 📁 Estrutura do Repositório

```text
miniguia-analise-dados-logistica/
│
├── README.md
│
├── fontes/
│   └── fontes.md
│
├── miniguia/
│   └── resumo.md
│
└── prompts/
    ├── troubleshooting.md
    └── prompts_reutilizaveis.md
```

---

## 🛠️ Ferramentas Utilizadas

* **NotebookLM** — análise e interação com as fontes;
* **GitHub** — versionamento e documentação do projeto;
* **Markdown** — estruturação da documentação;
* **Inteligência Artificial Generativa** — apoio ao processo de aprendizagem;
* **Engenharia de Prompts** — desenvolvimento e refinamento das consultas.

---

## 📈 Principais Aprendizados

O desenvolvimento deste projeto demonstrou que a qualidade da interação com uma IA depende diretamente da forma como o problema é apresentado.

Um prompt mais eficiente tende a combinar:

**Contexto → Objetivo → Escopo → Tarefa → Formato → Restrições → Evidências**

Também foi possível observar a importância de trabalhar com fontes selecionadas e solicitar que a IA identifique explicitamente quando determinada informação não está disponível no material utilizado.

Dessa forma, a Inteligência Artificial deixa de ser utilizada apenas como ferramenta para gerar respostas e passa a atuar como apoio estruturado ao processo de estudo, análise e revisão do conhecimento.

---

## 👨‍💻 Autor

**Felipe Canato**

Projeto desenvolvido como atividade prática envolvendo **NotebookLM, Engenharia de Prompts, curadoria de fontes e documentação no GitHub**.

