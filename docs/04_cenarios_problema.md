# Entrega 4 — Cenários de análise/problema

**Data:** 06/10/2026  
**Status:** 🟨 em andamento  
**Responsabilidade:** 1 solução completa por integrante

## Objetivo da atividade

Descrever situações atuais em que o usuário tenta alcançar um objetivo e encontra dificuldades. O cenário de análise/problema deve tornar visível **o contexto, os atores, as ações e as rupturas**, sem antecipar a interface que será projetada.

> **Regra central:** cenário de problema é a “história do problema”. Se o texto já diz “o sistema mostra”, “o aplicativo resolve” ou descreve botões/telas futuras, provavelmente está misturando problema com solução.

Sempre que possível, o cenário deve aprofundar uma **situação concreta já registrada na Entrega 1**.

### Quando o TCC não possuía interface

O cenário continua sendo uma história de **problema/atividade humana**, não uma história do futuro sistema. Descreva como o profissional realiza hoje uma atividade semelhante ou como lida atualmente com dados, resultados, configurações, logs, decisões e limitações que o tema do TCC pretende apoiar.

Exemplo: em vez de “o DBA abre o novo dashboard e executa o algoritmo”, descreva “o DBA precisa investigar uma consulta lenta, reúne informações em ferramentas distintas, compara planos manualmente e tem dificuldade para estimar o impacto de uma mudança”.

A interface da disciplina aparecerá somente depois, nos cenários de interação.

Se o integrante escolher um novo problema/situação, explique por que ele passou a ser relevante e indique a evidência que motivou sua inclusão.

## Cenário C01 — {{título}}

**Autor(a):** {{nome — matrícula}}  
**Persona(s) relacionada(s):** {{P01}}  
**Necessidade relacionada:** {{R01}}  
**Situação concreta da Entrega 1 relacionada:** {{seção 4.4 / H01 / outra ou “nova situação justificada”}}  
**Hipóteses ainda presentes:** {{H01, H02 ou —}}

## Cenário C02 — Recomendação de venda sem dados de peso
 
**Autor(a):** Gustavo Atui — 24.123.072-1  
**Persona(s) relacionada(s):** P02 — Dinho  
**Necessidade relacionada:** R03 — acompanhar a evolução do peso para orientar o manejo  
**Situação concreta da Entrega 1 relacionada:** seção 4.5 (pesagem trabalhosa e poucas vezes por ano), agora vista pela perspectiva do técnico agropecuário  
**Hipóteses ainda presentes:** H03, H05, H08

### 1. Cenário inicial

#### C02
Dinho é técnico agropecuário e presta assistência a várias propriedades da região. Na visita mensal à fazenda do Chico, o produtor pergunta se o lote já está no ponto de venda, porque um comprador ofereceu um preço bom pela arroba.
 
Dinho pede os registros de peso do lote. Chico mostra um caderno com anotações de uma única pesagem feita meses atrás, quando alugou uma balança. Sem dados recentes, Dinho observa os animais e estima o peso "no olho". Ele sabe que essa estimativa tem pouca precisão.
 
Dinho recomenda esperar mais algumas semanas. Chico fica em dúvida, porque o vizinho vendeu um lote parecido e disse que estava no ponto. No fim, Chico decide vender, e o frigorífico paga menos do que ele esperava, porque parte dos animais estava abaixo do peso ideal.

### 2. Questões de refinamento

Use os tipos de questões/taxonomia definidos na aula. As perguntas devem revelar informações **ainda ausentes** do cenário, não repetir o que já foi respondido.

#### C02
| # | Questão | Por que precisa ser respondida | Fonte/forma de obter resposta |
|---|---|---|---|
| Q1 | Com que frequência o Dinho visita a fazenda do Chico, e quanto tempo dura cada visita? | Define quanto tempo ele tem para analisar o lote e conversar com o produtor | Entrevista com técnicos agropecuários (Entrega 7) |
| Q2 | Que registros de peso o Chico tem hoje, onde ficam guardados e de quando são? | Revela de que dados o técnico realmente dispõe | Entrevista com produtores (Entrega 7) |
| Q3 | Além da estimativa visual, que outros recursos o Dinho usa para estimar o peso sem balança? | Mostra as práticas atuais e quanto elas custam em tempo e esforço | Entrevista com técnicos (Entrega 7); literatura de pecuária |
| Q4 | O que o Chico faz para acompanhar o lote entre uma visita do técnico e outra? | Revela o que acontece com o lote fora das visitas e que informação se perde nesse intervalo | Entrevista com produtores (Entrega 7) |

### 3. Cenário refinado

Reescreva o cenário incorporando as respostas. Marque o conteúdo novo de forma consistente (por exemplo, `**[NOVO: ...]**`).

{{narrativa refinada}}

#### C02
Dinho é técnico agropecuário e presta assistência a várias propriedades da região. **[NOVO: Ele visita a fazenda do Chico uma vez por mês, por cerca de duas horas.]** Na visita, Chico pergunta se o lote já está no ponto de venda, porque um comprador ofereceu um bom preço pela arroba.
 
Dinho pede os registros de peso. Chico mostra um caderno com uma única pesagem feita meses atrás, **[NOVO: sem o número do brinco em várias anotações]**. **[NOVO: Desde a última visita, Chico não acompanhou o peso do lote.]**
 
Sem dados recentes, Dinho estima o peso "no olho". **[NOVO: Em alguns animais usa a fita de pesagem, mas medir o lote inteiro não cabe no tempo da visita.]** **[NOVO: Ele sabe que o comprador desconta no preço dos animais abaixo de um peso mínimo, mas não consegue dizer quantos do lote já passaram dele.]**
 
Dinho recomenda esperar mais algumas semanas. Chico fica em dúvida, porque o vizinho vendeu um lote parecido. **[NOVO: Sem números, a recomendação do técnico vale o mesmo que a opinião do vizinho, e a decisão final é do Chico.]** Ele vende, e o frigorífico paga menos, porque parte dos animais estava abaixo do peso mínimo


### 4. Elementos extraídos

| Elemento | Evidência no cenário |
|---|---|
| Ator(es) | {{...}} |
| Objetivo(s) | {{...}} |
| Contexto | {{...}} |
| Recursos/informações | {{...}} |
| Ações | {{...}} |
| Problemas/rupturas | {{...}} |
| Consequências | {{...}} |

#### C02
| Elemento | Evidência no cenário |
|---|---|
| Ator(es) | Dinho (técnico agropecuário); Chico (produtor, quem decide); comprador/frigorífico; vizinho (influência indireta) |
| Objetivo(s) | Dinho: recomendar o momento certo de venda com base em dados. Chico: vender o lote no ponto certo e pelo melhor preço |
| Contexto | Visita técnica mensal de cerca de duas horas; oferta de compra com prazo curto; nenhum acompanhamento do peso entre as visitas |
| Recursos/informações | Caderno com uma pesagem antiga e incompleta; observação visual; fita de pesagem; peso mínimo exigido pelo comprador |
| Ações | Pedir registros; estimar o peso visualmente; medir alguns animais com fita; comparar com o peso mínimo do comprador; recomendar esperar |
| Problemas/rupturas | Registros antigos e sem identificação do animal; nenhuma informação sobre o lote entre as visitas; medir o lote inteiro não cabe no tempo da visita; impossível saber quantos animais passaram do peso mínimo; recomendação sem números perde força na decisão |
| Consequências | Venda com parte do lote abaixo do peso mínimo e preço menor; recomendação técnica desconsiderada |

### 5. Implicações para as próximas entregas

Quais tarefas merecem análise? Quais informações precisam ser coletadas? **Não desenhe a solução ainda.**

> Repita para C02, C03... com autoria individual.

#### C02
- Como o técnico decide se um lote está no ponto de venda.
- Como o produtor acompanha o lote entre as visitas do técnico.
- Como o peso de cada animal é associado ao seu brinco.
- Respostas reais para Q1 a Q4, com técnicos e produtores.
- Se o técnico teria acesso aos dados do produtor antes da visita ou só durante ela (H05).
- Se os termos "ponto de venda" e "arroba" são os que técnicos e produtores realmente usam (H08).

## Checklist

- [ ] Há um cenário completo por integrante.
- [ ] Cada cenário tem título, ator, objetivo, contexto e problema.
- [ ] O cenário possui origem rastreável na Entrega 1 ou justifica claramente a inclusão de uma nova situação.
- [ ] O texto descreve a situação atual, sem antecipar a solução.
- [ ] Para TCC sem interface original, o cenário descreve uma prática humana plausível relacionada à contribuição técnica, e não “a falta de uma tela”.
- [ ] Questões de refinamento acrescentam informação nova.
- [ ] O refinamento mostra claramente o que foi adicionado/alterado.
- [ ] Cenários são diferentes o suficiente para cobrir objetivos/problemas relevantes.
- [ ] Cada cenário está ligado a persona/necessidade na matriz de rastreabilidade.
