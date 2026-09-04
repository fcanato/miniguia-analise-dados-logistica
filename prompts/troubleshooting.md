# 🩹 Engenharia de Prompts e Cicatrizes do Projeto

Esta seção documenta os testes realizados durante a utilização do NotebookLM, incluindo prompts que produziram respostas excessivamente amplas, problemas identificados e estratégias utilizadas para melhorar os resultados.

O objetivo é registrar não apenas as respostas finais, mas também o processo de refinamento das instruções fornecidas à Inteligência Artificial.

---

## Experimento 01 — Do Prompt Genérico ao Prompt Estruturado

### 🔹 Prompt inicial

> Explique os principais conceitos de gestão de estoques e como a análise de dados pode contribuir para uma operação logística.

### Resultado observado

O NotebookLM apresentou uma resposta abrangente, incluindo conceitos relevantes como:

* Estoque;
* Lead Time;
* Estoque de Segurança;
* Ponto de Reposição;
* Lote Econômico de Compra;
* Curva ABC;
* Giro de Estoque;
* Cobertura;
* Acuracidade.

Entretanto, a resposta também expandiu a análise para assuntos como:

* roteirização;
* localização de instalações;
* sistemas WMS;
* rastreamento de veículos;
* RFID;
* EDI.

Embora esses assuntos estejam relacionados à logística, eles ampliaram excessivamente o escopo original do estudo, cujo foco principal é a utilização de dados na **gestão de estoques**.

---

## 🔍 Problema identificado

O primeiro prompt apresentava três limitações principais:

1. **Escopo muito amplo:** não especificava quais conceitos deveriam ser priorizados.
2. **Formato indefinido:** não determinava como a resposta deveria ser estruturada.
3. **Ausência de critérios de evidência:** não solicitava explicitamente que informações não encontradas nas fontes fossem identificadas como limitações.

Esse teste demonstrou que perguntas genéricas podem produzir respostas corretas, porém menos direcionadas ao objetivo específico do estudo.

---

# 🔧 Refinamento do Prompt

Para melhorar o resultado, o prompt foi reformulado utilizando algumas técnicas de Engenharia de Prompts:

* delimitação do contexto;
* definição clara do objetivo;
* decomposição da tarefa;
* especificação do formato da resposta;
* solicitação de exemplos práticos;
* solicitação de fórmulas;
* restrição às fontes disponibilizadas;
* tratamento explícito de informações ausentes.

### 🔹 Prompt refinado

> Com base exclusivamente nas fontes fornecidas, analise como a utilização de dados pode apoiar a gestão de estoques em uma operação logística.
>
> Concentre a análise em cinco aspectos: previsão de demanda, estoque de segurança, ponto de reposição, cobertura de estoque e acuracidade.
>
> Para cada aspecto, apresente:
>
> 1. definição do conceito;
> 2. quais dados são necessários para analisá-lo;
> 3. como ele pode ser calculado ou avaliado;
> 4. um exemplo prático aplicado a uma operação logística;
> 5. como o resultado pode apoiar a tomada de decisão.
>
> Sempre que houver fórmula nas fontes, apresente-a e explique suas variáveis.
>
> Organize a resposta de forma estruturada e objetiva.
>
> Utilize somente informações sustentadas pelas fontes disponibilizadas e indique as referências utilizadas. Caso alguma informação não esteja disponível nas fontes, informe explicitamente essa limitação em vez de completar a resposta com conhecimento externo.

---

# 📈 Resultado após o refinamento

O segundo prompt produziu uma resposta significativamente mais estruturada.

A análise foi concentrada exatamente nos cinco aspectos solicitados:

| Tema                 | Resultado obtido                                |
| -------------------- | ----------------------------------------------- |
| Previsão de demanda  | Métodos, dados necessários, fórmulas e exemplos |
| Estoque de segurança | Conceito, variáveis e aplicação                 |
| Ponto de reposição   | Fórmula, exemplo e apoio à decisão              |
| Cobertura de estoque | Diferentes formas de cálculo e interpretação    |
| Acuracidade          | Fórmulas, exemplos e aplicação em inventários   |

Outro avanço importante foi a apresentação das **limitações das próprias fontes**.

O NotebookLM informou, por exemplo, que determinados cálculos relacionados a regressão linear múltipla e metas quantitativas de nível de serviço não estavam completamente detalhados no material utilizado.

Isso tornou a resposta mais rastreável e reduziu o risco de incorporar informações externas sem identificação.

---

# 💡 Principal Aprendizado

O experimento demonstrou que um bom prompt não depende apenas de fazer uma pergunta.

É necessário especificar:

**Contexto → Objetivo → Escopo → Dados esperados → Formato → Restrições → Evidências**

A transformação pode ser resumida da seguinte forma:

**Prompt genérico**

`Explique o assunto.`

⬇️

**Prompt estruturado**

`Analise X, concentre-se em A/B/C, apresente dados, cálculo, exemplo e decisão, utilize somente as fontes e informe limitações.`

Essa mudança tornou a resposta mais objetiva, técnica, verificável e adequada ao propósito do estudo.

---

## 🩹 Cicatriz registrada

> **Problema:** resposta tecnicamente relevante, porém excessivamente ampla.
>
> **Causa:** ausência de delimitação de escopo e estrutura no prompt inicial.
>
> **Correção:** definição dos conceitos que deveriam ser analisados, formato obrigatório da resposta e restrição às fontes.
>
> **Resultado:** resposta mais estruturada, quantitativa, rastreável e orientada à tomada de decisão.

---

## 🎯 Conclusão do Experimento 01

A principal conclusão deste teste é que **quanto mais clara for a definição do problema e do formato esperado, maior tende a ser a utilidade da resposta produzida pela IA**.

Além disso, solicitar explicitamente que a IA reconheça limitações das fontes mostrou-se importante para diferenciar informações fundamentadas de conteúdos que não poderiam ser comprovados pelo material utilizado.
