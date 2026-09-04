# 🤖 Prompts Reutilizáveis para Estudos

Esta seção reúne prompts desenvolvidos durante o projeto para apoiar futuras revisões e estudos utilizando ferramentas de Inteligência Artificial, especialmente o NotebookLM.

Os prompts foram estruturados para priorizar **clareza, contexto, rastreabilidade das fontes e aplicação prática**.

---

## 📚 1. Gerar Resumo Estruturado

> Com base exclusivamente nas fontes disponibilizadas, produza um resumo estruturado dos principais conceitos relacionados ao tema estudado.
>
> Para cada conceito, apresente:
>
> * definição;
> * finalidade;
> * aplicação prática;
> * principais variáveis ou indicadores relacionados.
>
> Utilize linguagem técnica e didática. Indique as referências utilizadas e informe explicitamente quando determinada informação não estiver disponível nas fontes.

### Quando utilizar

Ideal para realizar o primeiro levantamento de um novo assunto.

---

## 🔍 2. Aprofundar um Conceito

> Com base exclusivamente nas fontes fornecidas, explique detalhadamente o conceito de **[INSERIR CONCEITO]**.
>
> Apresente:
>
> 1. definição;
> 2. finalidade;
> 3. dados necessários;
> 4. método de cálculo, quando disponível;
> 5. fórmula e explicação das variáveis;
> 6. exemplo prático;
> 7. como o resultado pode apoiar uma decisão.
>
> Não utilize conhecimento externo para preencher informações ausentes nas fontes.

### Quando utilizar

Para aprofundar assuntos como estoque de segurança, cobertura, acuracidade ou previsão de demanda.

---

## 📊 3. Transformar Teoria em Aplicação Prática

> Utilizando exclusivamente as fontes disponibilizadas, transforme os conceitos estudados em um exemplo aplicado a uma operação logística.
>
> Apresente a situação inicial, os dados disponíveis, o indicador ou método utilizado, o cálculo quando aplicável, a interpretação do resultado e a decisão que poderia ser tomada.
>
> Diferencie claramente informações provenientes das fontes de hipóteses utilizadas apenas para construção do exemplo.

### Quando utilizar

Ideal para compreender como determinado conceito pode ser aplicado no ambiente profissional.

---

## 🧮 4. Identificar Fórmulas e Indicadores

> Analise as fontes e identifique todas as fórmulas e indicadores relacionados a **[INSERIR TEMA]**.
>
> Para cada fórmula ou indicador, apresente:
>
> * nome;
> * fórmula;
> * significado das variáveis;
> * finalidade;
> * interpretação;
> * exemplo disponível nas fontes.
>
> Não crie fórmulas que não estejam presentes no material analisado.

### Quando utilizar

Útil para revisão quantitativa e construção de material de consulta rápida.

---

## ⚖️ 5. Comparar Conceitos

> Compare **[CONCEITO A]** e **[CONCEITO B]** utilizando exclusivamente as fontes disponibilizadas.
>
> Organize a resposta apresentando:
>
> * definição de cada conceito;
> * diferenças;
> * semelhanças;
> * aplicações;
> * dados necessários;
> * relação entre os conceitos.
>
> Finalize explicando em quais situações cada conceito é mais relevante.

### Quando utilizar

Exemplo:

`Compare Giro de Estoque e Cobertura de Estoque.`

---

## 🧠 6. Criar Simulado

> Com base exclusivamente nas fontes disponibilizadas, crie um simulado com 10 questões sobre os principais conceitos estudados.
>
> Utilize diferentes níveis de dificuldade e inclua questões conceituais e práticas.
>
> Não apresente inicialmente as respostas.
>
> Aguarde minhas respostas e somente depois apresente o gabarito comentado, indicando quais conceitos das fontes justificam cada resposta.

### Quando utilizar

Para testar retenção do conteúdo antes de finalizar uma etapa de estudo.

---

## 🔎 7. Revisar Meu Conhecimento

> Vou explicar com minhas próprias palavras o que compreendi sobre **[INSERIR TEMA]**.
>
> Compare minha explicação exclusivamente com as fontes disponibilizadas.
>
> Classifique os pontos apresentados em:
>
> * correto;
> * parcialmente correto;
> * incorreto;
> * informação não encontrada nas fontes.
>
> Depois explique o que devo revisar.

### Quando utilizar

Para verificar se o conteúdo foi realmente compreendido e não apenas memorizado.

---

## 🚨 8. Identificar Limitações das Fontes

> Analise as fontes disponibilizadas e identifique quais informações importantes sobre **[INSERIR TEMA]** não estão suficientemente detalhadas.
>
> Não complete essas lacunas utilizando conhecimento externo.
>
> Apresente:
>
> * informação ausente ou incompleta;
> * por que ela seria importante;
> * qual tipo de fonte adicional poderia complementar o estudo.

### Quando utilizar

Este prompt ajuda a identificar limitações da própria curadoria de fontes.

---

## 🔗 9. Relacionar Indicadores

> Analise como **[INDICADOR A]**, **[INDICADOR B]** e **[INDICADOR C]** se relacionam.
>
> Explique como alterações em um indicador podem influenciar os demais e como a análise conjunta pode apoiar a tomada de decisão.
>
> Utilize exclusivamente relações sustentadas pelas fontes e indique quando uma relação não puder ser comprovada pelo material disponível.

### Exemplo

`Analise como previsão de demanda, estoque de segurança, cobertura e ponto de reposição se relacionam.`

---

## ⚡ 10. Revisão Rápida

> Com base exclusivamente nas fontes, crie uma revisão rápida sobre **[INSERIR TEMA]**.
>
> Apresente somente:
>
> * 5 conceitos fundamentais;
> * 3 fórmulas ou indicadores importantes;
> * 3 erros de interpretação que devo evitar;
> * 5 perguntas para testar meu conhecimento.
>
> Priorize informações essenciais para uma revisão de aproximadamente 10 minutos.

---

# 🧩 Estrutura de Prompt Aprendida

Durante os experimentos deste projeto, uma estrutura mostrou-se especialmente útil:

```text
CONTEXTO
↓
OBJETIVO
↓
ESCOPO
↓
TAREFAS
↓
FORMATO DA RESPOSTA
↓
RESTRIÇÕES
↓
FONTES/EVIDÊNCIAS
```

## Template Geral

> Você deverá analisar **[CONTEXTO]**.
>
> Seu objetivo é **[OBJETIVO]**.
>
> Concentre a análise em **[ESCOPO]**.
>
> Para cada elemento, realize **[TAREFAS]**.
>
> Organize a resposta no formato **[FORMATO]**.
>
> Utilize exclusivamente **[FONTES]**.
>
> Não utilize informações externas para preencher lacunas. Quando uma informação não puder ser encontrada, informe explicitamente essa limitação.

---

# 🎯 Principal Aprendizado

Um prompt eficiente não precisa ser simplesmente longo.

Ele precisa deixar claro:

**o que analisar + por que analisar + como analisar + como responder + quais fontes utilizar + quais limites respeitar.**

Essa estrutura permite produzir respostas mais consistentes, verificáveis e reutilizáveis em diferentes contextos de estudo.
