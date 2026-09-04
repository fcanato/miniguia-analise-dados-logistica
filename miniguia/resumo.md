 MINIGUIA DE ESTUDOS: ANÁLISE DE DADOS APLICADA À GESTÃO DE ESTOQUES

Este material foi desenvolvido para apoiar profissionais e estudantes da área de logística na compreensão de como a análise quantitativa e o uso estratégico de dados estruturam e otimizam a gestão de estoques [214]. 

---

## 1. Introdução

A **gestão de estoques** consiste no planejamento, controle e supervisão de todos os bens físicos armazenados por uma organização [215]. O seu objetivo primário é equilibrar duas forças opostas: a garantia de disponibilidade de produtos para atender ao mercado no tempo certo e a prevenção contra excessos de mercadorias que imobilizam capital financeiro desnecessariamente [215, 216]. 

Na era digital, a tomada de decisão logística moderna abandonou o empirismo ("achismos") e apoia-se em sistemas informatizados (como o Sistema de Gestão de Estoques - SGE, Enterprise Resource Planning - ERP, e o Warehouse Management System - WMS) [216, 332]. Esses sistemas capturam dados operacionais em tempo real — como histórico de demanda, ordens de compra pendentes e contagens de inventário — permitindo análises estatísticas rigorosas para prever o comportamento do mercado, programar ressuprimentos em tempo hábil e assegurar a saúde financeira da empresa [217, 222].

---

## 2. Previsão de Demanda

### Conceito
É o processo científico de estimar as necessidades de consumo ou vendas de produtos em um determinado horizonte de tempo futuro [216, 264]. Uma previsão precisa serve de base para o dimensionamento de compras, programação da produção e equilíbrio dos níveis de segurança [60, 216].

### Dados Necessários
*   Dados históricos de vendas ou consumo do produto por período [95].
*   Características e sazonalidade do produto [271, 272].
*   Fatores independentes influenciadores (promoções, preços históricos, concorrência, etc.) no caso de modelos de correlação [191, 270].
*   Expectativas não numéricas e opiniões de especialistas (para métodos qualitativos) [95, 268].

### Métodos Encontrados nas Fontes
As fontes dividem os métodos de previsão em duas categorias [95, 219]:
1.  **Métodos Qualitativos**: Baseados em opiniões subjetivas, julgamentos e experiência acumulada. Os principais são:
    *   *Pesquisa de Mercado*: Levantamento direto com consumidores [95].
    *   *Painel de Consenso / Especialistas*: Reunião estruturada de profissionais da área (como gerentes e vendedores) para discutir estimativas [95, 267].
    *   *Método Delphi (Opinião de Especialistas)*: Coleta de estimativas de forma anônima e iterativa através de questionários moderados, até que um consenso estatístico seja alcançado [96, 268].
    *   *Analogia Histórica*: Uso do histórico de itens semelhantes para prever a curva de introdução de um novo produto [95].
2.  **Métodos Quantitativos (Estatísticos)**: Modelos matemáticos que assumem que o comportamento futuro será uma projeção de tendências passadas [95, 188]. Destacam-se:
    *   *Séries Temporais*: Média Móvel Simples, Média Móvel Ponderada e Ajustamento Exponencial [188, 265].
    *   *Modelos de Regressão Linear Simples*: Estabelecem relações matemáticas entre a demanda (variável dependente $Y$) e um fator influenciador (variável independente $X$, como investimentos em publicidade ou tempo de promoção) [191, 270].
    *   *Simulação de Cenários*: Modelagem computacional complexa [95].

### Fórmulas Disponíveis nas Fontes

#### A. Média Móvel Simples (SMA)
Calcula a previsão do próximo período extraindo a média aritmética de $N$ períodos históricos anteriores [188].
$$\text{Média Móvel Simples} = \frac{\sum_{i=1}^{N} D_i}{N}$$
*   **$D_i$**: Demanda real registrada no período anterior $i$ [188].
*   **$N$**: Quantidade total de períodos considerados no cálculo [188].

#### B. Média Móvel Ponderada (MMP)
Atribui relevâncias (pesos) diferentes a cada período anterior, geralmente priorizando os dados mais recentes por representarem melhor a tendência atual do mercado [189, 269].
$$\text{Média Móvel Ponderada} = \frac{\sum_{i=1}^{N} D_i \times P_i}{\sum_{i=1}^{N} P_i}$$
*   **$D_i$**: Demanda real registrada no período $i$ [189].
*   **$P_i$**: Peso individual atribuído ao período $i$ [189].

#### C. Ajustamento Exponencial (Média Exponencial Móvel)
Modelo recursivo que atualiza a previsão do próximo período somando à previsão anterior uma fração do erro de previsão cometido no período anterior [315, 326].
$$P_t = P_{t-1} + \alpha(D_{t-1} - P_{t-1})$$
*   **$P_t$**: Previsão de demanda calculada para o período atual ($t$) [315, 326].
*   **$P_{t-1}$**: Previsão de demanda calculada para o período imediatamente anterior ($t-1$) [315, 326].
*   **$\alpha$ (alfa)**: Fator de suavização exponencial, variando em uma escala estrita de $0$ a $1$ [273, 315, 326].
*   **$D_{t-1}$**: Demanda real verificada no período imediatamente anterior ($t-1$) [315, 326].

### Exemplo Prático
Uma empresa de comércio eletrônico adota para a previsão de vendas de um determinado acessório o método de **Ajustamento Exponencial com constante $\alpha = 0,2$** [318, 326]. 
No mês 4, a previsão estimada pelo analista era de **375 unidades**, mas o fechamento de vendas reais computou uma demanda real de **400 unidades** [318, 325]. 

O cálculo para prever a demanda do mês 5 ($P_5$) é:
$$P_5 = 375 + 0,2 \times (400 - 375)$$
$$P_5 = 375 + 0,2 \times 25 = 375 + 5 = 380 \text{ unidades}$$ [326]

Se no final do mês 5 a demanda real verificada subir para **430 unidades**, a nova projeção para o mês 6 ($P_6$) será:
$$P_6 = 380 + 0,2 \times (430 - 380)$$
$$P_6 = 380 + 0,2 \times 50 = 380 + 10 = 390 \text{ unidades}$$ [326]

---

## 3. Estoque de Segurança

### Conceito e Finalidade
É um volume preventivo extra de mercadorias mantido em estoque com a finalidade de amortecer e salvaguardar a operação contra flutuações e picos imprevistos na demanda de vendas e contra atrasos no tempo de ressuprimento (*lead time*) por parte dos fornecedores ou transportadoras [102, 216]. O estoque de segurança visa mitigar o risco de ruptura de estoque (desabastecimento) [102, 216].

### Variáveis Utilizadas
*   **$ES$**: Volume do Estoque de Segurança em unidades [91].
*   **DemandaMédia (ou $d$)**: Consumo médio diário ou taxa de demanda histórica [91, 102].
*   **IntervaloreabastecimentoMédio (ou $LT$)**: Prazo médio de ressuprimento medido [91, 102].
*   **Dias úteis**: Número de dias úteis contidos no período de tempo analisado [91].
*   **$k$**: Fator de segurança estatístico arbitrado proporcionalmente ao Nível de Serviço desejado para o item [102, 103].

### Fórmulas Disponíveis nas Fontes

1.  **Fórmula prática baseada na variabilidade de consumo e prazo fixo**:
    $$ES = \frac{\text{Intervalo reabastecimento Médio} \times \text{Demanda Média}}{\text{Dias úteis}}$$ [91]
2.  **Fórmula com base no Fator de Serviço estatístico**:
    $$ES = d \times k$$ [102, 103]

### Exemplo Prático
Um analista de controle de estoque avalia um determinado fornecedor de insumos e percebe que ele opera de forma instável, gerando atrasos recorrentes no tempo de entrega [90]. Sob o sistema de transporte atual, a empresa é obrigada a manter um Estoque de Segurança elevado de $100$ unidades para garantir a continuidade da operação sem quebras na produção [90]. 

Com base na análise quantitativa de custos de estoques, o gestor logístico decide comparar o custo financeiro de carregar esse excesso de inventário (capital imobilizado) contra a opção de contratar um transportador mais confiável [90, 92]. Se um fornecedor de transportes alternativo cobra uma tarifa mais cara, mas garante pontualidade e reduz o lead time, o novo Estoque de Segurança poderá ser reduzido significativamente, justificando economicamente a substituição operacional [90].

---

## 4. Ponto de Reposição (Ponto de Pedido)

### Conceito
O **Ponto de Reposição (PR)** ou Ponto de Pedido é o nível físico de estoque que, uma vez atingido no almoxarifado, atua como um gatilho de decisão que sinaliza a necessidade de emitir e colocar imediatamente uma nova ordem de compra de reposição de materiais ao fornecedor [102, 104, 216]. Ele garante que o novo lote seja recebido e disponibilizado exatamente no momento em que o estoque regular se esgota, evitando o consumo do estoque de segurança [102, 216].

### Fórmula Encontrada nas Fontes
$$\text{PR} = d \times LT + ES$$ [102, 103]
$$\text{Ponto de Pedido} = (\text{Consumo Médio Diário} \times \text{Prazo de Entrega}) + \text{Estoque de Segurança}$$ [340]

*   **$\text{PR}$ (ou Ponto de Pedido)**: Nível de estoque que dispara o reabastecimento em unidades [102, 340].
*   **$d$ (ou Consumo Médio Diário)**: Taxa de consumo diário médio de estoque. É calculada dividindo-se a demanda ou consumo mensal pelo número de dias úteis trabalhados no mês [102, 340].
*   **$LT$ (ou Prazo de Entrega / Lead time)**: Tempo total de ressuprimento em dias úteis, correspondente ao intervalo entre a emissão do pedido e a efetiva entrega física do produto disponível para uso [102, 104, 340].
*   **$ES$**: Estoque de Segurança estabelecido [102].

### Exemplo Prático
Um almoxarifado opera sob modelo de reposição contínua para um componente industrial. Registra-se um consumo médio mensal de **1.000 unidades** do componente e a empresa mantém um estoque de segurança estipulado de **100 unidades** [329, 339]. O prazo de entrega garantido pelo fornecedor contratado é de **10 dias úteis** após a confirmação do pedido, e a empresa opera com **20 dias úteis** por mês [330].

1.  **Cálculo do Consumo Médio Diário ($d$)**:
    $$d = \frac{\text{Consumo Médio Mensal}}{\text{Dias Úteis por Mês}} = \frac{1.000}{20} = 50 \text{ unidades/dia}$$ [340]
2.  **Cálculo do Ponto de Reposição (PR)**:
    $$\text{PR} = (50 \text{ unidades/dia} \times 10 \text{ dias}) + 100$$
    $$\text{PR} = 500 + 100 = 600 \text{ unidades}$$ [340]

*Decisão Logística*: No momento em que o sistema registrar que o saldo físico desse componente caiu para 600 unidades, uma nova ordem de compra no volume do lote de reposição deve ser disparada de forma imediata [102, 340].

---

## 5. Cobertura de Estoque (Prazo de Cobertura)

### Como o Indicador Funciona
O indicador de **Prazo de Cobertura** mede a autonomia temporal de estoque físico de uma organização [229]. Ele indica por quanto tempo (geralmente expresso em dias ou meses) o estoque disponível atual conseguirá satisfazer plenamente a demanda projetada de vendas sem que haja qualquer necessidade de realizar novos pedidos de compra para reposição [223, 229, 261].

### Como Pode Ser Calculado

#### A. Abordagem Financeira (Valor de Estoque)
Calculada pela divisão do valor monetário do estoque pelo custo operacional diário de vendas [229].
$$\text{Prazo de Cobertura} = \frac{\text{Valor Médio do Estoque}}{\text{Custo Diário de Vendas}}$$ [230]

#### B. Abordagem Física (Unidades de Itens)
Mapeada diretamente pela razão entre as quantidades físicas em saldo e a projeção de demanda diária [251].
$$\text{Cobertura de Estoque} = \frac{\text{Estoque Inicial}}{\text{Demanda Diária}}$$ [251]
*   A **Demanda Diária** é obtida dividindo a demanda mensal pelos dias considerados do mês (por exemplo, 30 dias) [251].

#### C. Abordagem Baseada no Giro de Estoque
$$\text{Cobertura} = \frac{\text{Período de Tempo}}{\text{Giro de Estoque}}$$ [223, 314]

### Exemplo de Cálculo
Uma loja varejista possui uma demanda estável de **800 unidades** de discos rígidos SATA por mês (mês de 30 dias) [241, 251]. O saldo médio desse item armazenado fisicamente no estoque inicial é de **300 unidades** [241, 248].

1.  **Cálculo da Demanda Diária**:
    $$\text{Demanda Diária} = \frac{800 \text{ unidades}}{30 \text{ dias}} \approx 26,67 \text{ unidades/dia}$$ [251]
2.  **Cálculo da Cobertura de Estoque**:
    $$\text{Cobertura} = \frac{300 \text{ unidades}}{26,67 \text{ unidades/dia}} \approx 11,25 \text{ dias}$$ [252]

### Auxílio em Decisões de Reposição
A monitoria sistemática deste indicador norteia decisões vitais de suprimentos e fluxo de caixa [233]:
*   *Prevenção de Ruptura*: Se o lead time de entrega do fornecedor for de **15 dias** e a cobertura atual for de **11,25 dias**, o gestor decide por uma compra em caráter emergencial ou antecipação de pedidos, pois o estoque atual acabará antes da chegada regular de um novo lote [232].
*   *Otimização de Capital de Giro*: Coberturas excessivamente longas revelam capital ocioso e despesas de armazenamento abusivas [223, 226]. O resultado apoia decisões de redução de investimentos em estoque (como implantação de entregas parciais ou descontinuação de itens sem giro) [233, 250].

---

## 6. Acuracidade de Estoque (Índice de Acurácia)

### Conceito
O **Índice de Acurácia** mede o grau de exatidão e fidedignidade dos controles operacionais da empresa [224, 234]. Ele confronta os registros formais contidos nos sistemas de controle de inventário com as quantidades de itens físicos reais contados e auditados fisicamente dentro dos almoxarifados [224, 234]. 

### Fórmulas Disponíveis nas Fontes

#### A. Acurácia Simples (Física) por Unidades
Calculada dividindo a quantidade física contada corretamente no armazém pelo saldo que o sistema indicava [234, 302].
$$\text{Acurácia} = \frac{\text{Total de itens contados corretamente no inventário físico}}{\text{Total de itens registrados no sistema}}$$ [234, 302]

#### B. Acurácia Baseada em Divergências (Índice de Divergência)
$$\text{Índice de Acurácia (\%)} = \left(1 - \frac{\text{Total de itens com Divergências}}{\text{Total de Itens Inventariados}}\right) \times 100$$ [336]

#### C. Acurácia Ponderada por Valor Monetário (Classes ABC)
Para uma análise mais realista sobre o valor financeiro do estoque, pondera-se o percentual de acurácia de cada classe ABC pelo valor correspondente que ela representa no patrimônio total da empresa [338].
$$\text{Acurácia Ponderada} = \frac{\sum (\text{Valor de estoque da classe } i \times \text{Acurácia de itens da classe } i)}{\text{Valor total de estoque}}$$ [338]

### Demonstração de Aplicação em Inventários Físicos

**Aplicação 1: Acurácia por Divergência de Itens**
Uma auditoria interna realizou um inventário de contagem física geral em **10.000 itens** cadastrados no sistema [328, 335]. Ao cruzar as contagens, os auditores detectaram divergências (erros quantitativos em excesso ou falta) em **1.200 itens** [328, 335].
$$\text{Índice de Acurácia (\%)} = \left(1 - \frac{1.200}{10.000}\right) \times 100 = (1 - 0,12) \times 100 = 88\%$$ [336]

*Significado*: Apenas 88% dos registros eletrônicos correspondem de forma exata à realidade física estocada [337].

**Aplicabilidade Prática**: Um índice de 88% é um sinal de alerta vermelho para o gestor. Baixos níveis de acurácia causam perda de vendas (rupturas ocultas) e paradas inesperadas de linha de produção [298]. O resultado apoia a decisão de investir em processos de inventário rotativo (contagens periódicas e frequentes), contratação de sistemas WMS de coleta automatizada por códigos de barra ou RFID e melhor treinamento dos operadores para eliminação do erro humano [132, 298].

---

## 7. Relação entre os Indicadores

Os cinco indicadores não devem ser avaliados de forma isolada, pois são elos interdependentes de um mesmo fluxo operacional quantitativo [102, 216]. A análise de dados atinge sua potencialidade máxima ao cruzar essas métricas para blindar o planejamento logístico contra falhas [222, 224].

```
       [Acuracidade de Estoque] (Garante a fidedignidade dos registros)
                  │
                  ▼
         [Previsão de Demanda]  (Projeta o consumo futuro 'd')
                  │
                  ▼
        ┌─────────┴─────────┐
        ▼                   ▼
 [Estoque de Segurança]  [Ponto de Reposição]  <───►  [Cobertura de Estoque]
(Protege contra desvios) (Indica QUANDO comprar)     (Mede a autonomia operacional)
```

1.  **Acuracidade como Fundação**: A acuracidade de estoque é o ponto inicial de partida [224, 234]. Se a acuracidade for baixa, as informações do sistema sobre o saldo atual estão incorretas [298]. Consequentemente, o cálculo do Ponto de Reposição e o cálculo do Prazo de Cobertura serão calculados sobre saldos fictícios, gerando falsos gatilhos de compra e rupturas graves no atendimento [298].
2.  **Previsão Alimentando os Modelos**: A Previsão de Demanda quantifica a taxa futura esperada de consumo ($d$) [93, 216]. Este parâmetro $d$ determina diretamente a velocidade de esgotamento do estoque, ditando o Ponto de Reposição ($PR = d \times LT + ES$) e a quantidade de proteção contra desvios no Estoque de Segurança ($ES = d \times k$) [102, 103, 216].
3.  **Sincronização entre Ponto de Reposição e Cobertura**: Enquanto o Ponto de Reposição responde à pergunta de *quando* comprar, a Cobertura de Estoque monitora em tempo real a autonomia operacional remanescente do saldo físico [101, 102, 230]. Se o analista perceber que o prazo de cobertura é menor do que o lead time de entrega, e o ponto de reposição ainda não foi acionado eletronicamente (por distorção cadastral ou falha de sistema), o gestor deve antecipar o pedido preventivamente [230, 232].
4.  **Estoque de Segurança como Proteção**: Diante de imprecisões inevitáveis de previsão ou atrasos no tempo de transporte que afetam o lead time do fornecedor, o Estoque de Segurança atua como a última barreira de defesa [102, 216]. O seu dimensionamento depende de dados acurados de variabilidade de consumo e pontualidade física [102].

A análise conjunta permite à organização estruturar políticas inteligentes de reposição automática de estoques, diminuindo o custo total imobilizado sem colocar em risco o Nível de Serviço acordado com o cliente [215, 216].

---

## 8. Glossário

1.  **Administração de Materiais**: Conjunto de atividades integradas que visa planejar, executar e controlar os recursos materiais adquiridos e usados pela empresa, garantindo o abastecimento contínuo à operação ao menor custo global possível [47].
2.  **Acuracidade de Estoque**: Indicador que avalia a precisão e conformidade entre os registros quantitativos inseridos no sistema informatizado e o inventário físico real do armazém [224, 234].
3.  **Almoxarifado**: Espaço físico, coberto ou descoberto, estruturado especificamente para a guarda, conservação e controle exato de movimentação de materiais [136, 142].
4.  **Cobertura de Estoque (Prazo de Cobertura)**: Métrica temporal que avalia a autonomia operacional, determinando por quantos dias ou meses o inventário atual conseguirá atender a demanda prevista de vendas sem precisar de reabastecimento [223, 229].
5.  **Curva ABC**: Método clássico de controle de estoque que classifica as matérias-primas ou produtos armazenados em três categorias de importância (A, B e C) de acordo com o valor financeiro anual consumido e quantidade de itens [108, 110].
6.  **Estoque**: Quantidade acumulada de matérias-primas, materiais semiacabados (*work in progress*) ou produtos finais acabados mantidos temporariamente pela organização para amortecer o desequilíbrio entre a oferta e a demanda de consumo [79, 87].
7.  **Estoque de Segurança**: Volume extra de reserva de materiais mantido para mitigar rupturas operacionais decorrentes de oscilações na demanda ou atrasos na entrega dos fornecedores [102, 216].
8.  **Giro de Estoque**: Métrica de eficiência que indica a frequência de rotação de estoque, ou seja, quantas vezes o inventário médio foi totalmente vendido e reposto ao longo de um determinado período [119, 223, 226].
9.  **Inventário Físico**: Procedimento de contagem manual e direta de todos os materiais físicos em estoque para reconciliação periódica, contábil, fiscal e operacional com os saldos sistêmicos [137, 296].
10. **Just-in-Time (JIT)**: Filosofia japonesa de gestão operacional e programação de materiais que visa entregar as quantidades estritamente necessárias, no tempo e lugar exatos, reduzindo estoques imobilizados ao mínimo possível [308, 313].
11. **Kanban**: Ferramenta de gestão visual (comumente representada por cartões ou quadros de sinalização) que controla e operacionaliza a produção "puxada" Just-in-Time, evidenciando o ritmo de reabastecimento e excessos de fabricação [330].
12. **Lote Econômico de Compra (LEC/EOQ)**: Modelo clássico proposto por Ford Harris em 1913 que calcula matematicamente a quantidade ideal de compra que minimiza a soma total dos custos anuais de colocação de pedidos e custos de armazenagem [105, 106, 275, 276].
13. **Ponto de Reposição / Pedido**: Saldo quantitativo mínimo físico que, assim que alcançado no controle de saldos, deve disparar eletrônica ou manualmente uma ordem de reabastecimento junto ao compras [102, 104, 216].
14. **Tempo de Reposição (*Lead Time*)**: Tempo total decorrido entre a colocação de um pedido de compras no fornecedor e a efetiva entrega do lote físico disponível para uso na empresa [102, 104, 216].

---

## 9. Resumo para Revisão

*   **Objetivo de Otimização**: A gestão moderna de estoques foca em maximizar o nível de serviço prestado ao cliente minimizando o Custo Global operacional (soma dos custos de transporte, armazenagem e processamento de pedidos) [54, 215, 216].
*   **Decisões Embasadas**: A análise de dados de séries temporais históricas (médias móveis e suavização exponencial) elimina estimativas intuitivas, gerando previsões de demanda robustas [95, 185].
*   **Prevenção Contra Rupturas**: A determinação correta do Ponto de Reposição e do Estoque de Segurança responde com critério matemático exato a duas perguntas críticas: *quando comprar* e *quanto comprar* [101, 102, 216].
*   **Controle de Autonomia**: O prazo de cobertura de estoque alerta antecipadamente os analistas de compras se o saldo atual do almoxarifado sobreviverá ao tempo de reposição dos parceiros de fornecimento [230, 261].
*   **Acurácia como Regra**: Sem um rígido controle e índice elevado de acuracidade física de estoques, todo o planejamento de dados logísticos falha por operar sobre registros de sistema irreais e desajustados [298].
*   **Investimento Tecnológico**: Tecnologias modernas como coletores por radiofrequência (RFID), códigos de barra e sistemas automatizados WMS reduzem erros operacionais e são os maiores aliados da acurácia de estoques [132, 298].

---
*Referências bibliográficas base: Rosa, R. A., 2014; Amorim, V. S. e Rocha, W. F., 2023.*
