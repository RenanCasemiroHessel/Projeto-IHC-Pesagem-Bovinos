# Entrega 4 — Cenários de análise/problema

**Data:** 06/10/2026  
**Status:** 🟩 concluído  
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

## Cenário C01 — Acompanhar o ganho de peso do lote entre uma pesagem e outra

**Autor(a):** Rafael Takahagi Mendes — 22.126.084-7  
**Persona(s) relacionada(s):** P01 — Chico  
**Necessidade relacionada:** R01 — saber quanto cada animal ganhou de peso desde a última pesagem, para decidir entre vender, esperar ou suplementar  
**Situação concreta da Entrega 1 relacionada:** seção 4.5 (o produtor pesa poucas vezes por ano e, entre uma pesagem e outra, avalia os animais "no olho" e compara com anotações incompletas), com a seção 4.4  
**Hipóteses ainda presentes:** H03

## Cenário C02 — Recomendação de venda sem dados de peso
 
**Autor(a):** Gustavo Atui — 24.123.072-1  
**Persona(s) relacionada(s):** P02 — Dinho  
**Necessidade relacionada:** R03 — acompanhar a evolução do peso para orientar o manejo  
**Situação concreta da Entrega 1 relacionada:** seção 4.5 (pesagem trabalhosa e poucas vezes por ano), agora vista pela perspectiva do técnico agropecuário  
**Hipóteses ainda presentes:** H03, H05, H08

## Cenário C03 — Recomendação de venda sem dados de peso
 
**Autor(a):** Renan Casemiro Hessel — 24.123.019-2 
**Persona(s) relacionada(s):** P03 — Agnaldo 
**Necessidade relacionada:**  
**Situação concreta da Entrega 1 relacionada:**
**Hipóteses ainda presentes:** 
### 1. Cenário inicial

#### C01
Chico cria cerca de 30 bovinos jovens no pasto da propriedade. Numa manhã de sábado, na época da seca, ele passa pelo pasto e olha o lote. Pensa em duas coisas ao mesmo tempo: se algum animal já está no ponto de vender e se vale comprar suplemento para segurar os mais magros até a chuva voltar.

Em casa, abre o caderno e procura a última pesagem, de uns cinco meses atrás. Tenta comparar com o que viu no pasto, mas vários pesos estão ligados a brincos que ele não consegue ler direito, e outros só têm uma descrição, como "o pintado". Ele chama o Agnaldo, que cuida do lote todo dia, e pergunta o que ele acha de cada animal. A resposta do Agnaldo nem sempre bate com a impressão do Chico.

Sem saber quanto cada animal ganhou desde a última pesagem, Chico decide comprar suplemento para o lote inteiro e adiar a venda. Na hora de vender, descobre que parte dos animais já estava pronta antes e que gastou com suplemento onde não precisava.

#### C02
Dinho é técnico agropecuário e presta assistência a várias propriedades da região. Na visita mensal à fazenda do Chico, o produtor pergunta se o lote já está no ponto de venda, porque um comprador ofereceu um preço bom pela arroba.
 
Dinho pede os registros de peso do lote. Chico mostra um caderno com anotações de uma única pesagem feita meses atrás, quando alugou uma balança. Sem dados recentes, Dinho observa os animais e estima o peso "no olho". Ele sabe que essa estimativa tem pouca precisão.
 
Dinho recomenda esperar mais algumas semanas. Chico fica em dúvida, porque o vizinho vendeu um lote parecido e disse que estava no ponto. No fim, Chico decide vender, e o frigorífico paga menos do que ele esperava, porque parte dos animais estava abaixo do peso ideal.

#### C03
Agnaldo é peão na fazenda do Chico. Chico pede que ele e outro funcionário levem o lote para pesar na balança do vizinho, a 12 km, porque quer saber se os animais já estão no ponto de venda.
 
Agnaldo passa a manhã juntando o lote e embarcando os animais no caminhão. Na balança, os bois chegam agitados e alguns resistem a entrar no tronco. Ele anota o brinco e o peso de cada animal com as mãos sujas e com pressa, porque o vizinho precisa liberar a balança.
 
Eles voltam no fim da tarde. Ao passar as anotações a limpo, Chico encontra pesos repetidos e brincos que não consegue ler. Agnaldo não lembra qual animal era qual, e parte da pesagem fica sem uso.

### 2. Questões de refinamento

Use os tipos de questões/taxonomia definidos na aula. As perguntas devem revelar informações **ainda ausentes** do cenário, não repetir o que já foi respondido.

#### C01
| # | Questão | Por que precisa ser respondida | Fonte/forma de obter resposta |
|---|---|---|---|
| Q1 | Que informação o Chico precisa ter de cada animal para decidir entre vender, esperar ou dar suplemento? | Define o que realmente entra na decisão dele (peso atual, ganho desde a última pesagem, peso mínimo do comprador) | Entrevista com produtores (Entrega 7) |
| Q2 | Em que épocas do ano essa dúvida aparece e que pressões pesam na decisão (seca, preço da arroba, custo do suplemento)? | Mostra quanto tempo ele tem para decidir e quanto custa errar | Entrevista com produtores (Entrega 7); literatura de pecuária |
| Q3 | Em quem o Chico confia para opinar sobre o peso do lote e o que ele faz quando as opiniões não batem? | Revela de quem depende a decisão e como o conflito entre opiniões é resolvido | Entrevista com produtores e peões (Entrega 7) |
| Q4 | Além de olhar o lote e perguntar ao peão, que outras formas o Chico usa hoje para acompanhar o peso entre as pesagens? | Mostra as estratégias atuais e por que ele não as usa com mais frequência | Entrevista com produtores (Entrega 7) |
| Q5 | Como o Chico descobre que a decisão foi boa ou ruim, e quanto tempo depois? | Revela se existe algum retorno sobre a decisão ou se o erro passa despercebido | Entrevista com produtores (Entrega 7) |

#### C02
| # | Questão | Por que precisa ser respondida | Fonte/forma de obter resposta |
|---|---|---|---|
| Q1 | Com que frequência o Dinho visita a fazenda do Chico, e quanto tempo dura cada visita? | Define quanto tempo ele tem para analisar o lote e conversar com o produtor | Entrevista com técnicos agropecuários (Entrega 7) |
| Q2 | Que registros de peso o Chico tem hoje, onde ficam guardados e de quando são? | Revela de que dados o técnico realmente dispõe | Entrevista com produtores (Entrega 7) |
| Q3 | Além da estimativa visual, que outros recursos o Dinho usa para estimar o peso sem balança? | Mostra as práticas atuais e quanto elas custam em tempo e esforço | Entrevista com técnicos (Entrega 7); literatura de pecuária |
| Q4 | O que o Chico faz para acompanhar o lote entre uma visita do técnico e outra? | Revela o que acontece com o lote fora das visitas e que informação se perde nesse intervalo | Entrevista com produtores (Entrega 7) |

#### C03
| # | Questão | Por que precisa ser respondida | Fonte/forma de obter resposta |
|---|---|---|---|
| Q1 | Quantos animais são pesados por vez e quanto tempo leva cada um na balança? | Define o ritmo de trabalho e a pressa do peão durante a pesagem | Entrevista com peões e produtores (Entrega 7) |
| Q2 | Como o peão identifica o animal na hora da pesagem e o que faz quando o brinco está ilegível ou faltando? | Revela onde acontece o erro ao ligar o peso ao animal | Entrevista/observação no curral (Entrega 7) |
| Q3 | Quem anota os pesos, onde anota e quando isso é passado a limpo? | Mostra em que ponto a informação se perde | Entrevista com peões e produtores (Entrega 7) |
| Q4 | O que deixa de ser feito na fazenda no dia da pesagem, e quantas pessoas ficam envolvidas? | Mostra o custo real da pesagem em tempo e mão de obra | Entrevista com produtores (Entrega 7) |

### 3. Cenário refinado

Reescreva o cenário incorporando as respostas. Marque o conteúdo novo de forma consistente (por exemplo, `**[NOVO: ...]**`).

#### C01
Chico cria cerca de 30 bovinos jovens no pasto da propriedade. Numa manhã de sábado, **[NOVO – Q2: na época da seca, quando o pasto enfraquece e o suplemento pesa no custo]**, ele passa pelo pasto e olha o lote. Pensa em duas coisas ao mesmo tempo: se algum animal já está no ponto de vender e se vale comprar suplemento para segurar os mais magros até a chuva voltar. **[NOVO – Q1: Para decidir, ele precisa saber quanto cada animal pesa hoje, quanto ganhou desde a última pesagem e se já passou do peso mínimo que o comprador exige.]**

Em casa, abre o caderno e procura a última pesagem, de uns cinco meses atrás. Tenta comparar com o que viu no pasto, mas vários pesos estão ligados a brincos que ele não consegue ler direito, e outros só têm uma descrição, como "o pintado". **[NOVO – Q4: Entre uma pesagem e outra, ele só olha o lote no pasto e pergunta ao Agnaldo. Pesar um animal sozinho não compensa, porque teria que levá-lo até a balança do vizinho.]** Ele chama o Agnaldo, **[NOVO – Q3: em quem mais confia, porque está com o lote todo dia]**, e pergunta o que ele acha de cada animal. A resposta do Agnaldo nem sempre bate com a impressão do Chico. **[NOVO – Q3: Quando as opiniões divergem, Chico acaba ficando com a dele ou espera a visita mensal do Dinho, que também estima só no olho.]**

Sem saber quanto cada animal ganhou desde a última pesagem, Chico decide comprar suplemento para o lote inteiro e adiar a venda. **[NOVO – Q5: Só percebe que errou na hora de vender, quando o comprador separa os animais e o valor fecha. Ninguém volta para conferir a decisão depois.]** Na hora de vender, descobre que parte dos animais já estava pronta antes e que gastou com suplemento onde não precisava.


#### C02
Dinho é técnico agropecuário e presta assistência a várias propriedades da região. **[NOVO: Ele visita a fazenda do Chico uma vez por mês, por cerca de duas horas.]** Na visita, Chico pergunta se o lote já está no ponto de venda, porque um comprador ofereceu um bom preço pela arroba.
 
Dinho pede os registros de peso. Chico mostra um caderno com uma única pesagem feita meses atrás, **[NOVO: sem o número do brinco em várias anotações]**. **[NOVO: Desde a última visita, Chico não acompanhou o peso do lote.]**
 
Sem dados recentes, Dinho estima o peso "no olho". **[NOVO: Em alguns animais usa a fita de pesagem, mas medir o lote inteiro não cabe no tempo da visita.]** **[NOVO: Ele sabe que o comprador desconta no preço dos animais abaixo de um peso mínimo, mas não consegue dizer quantos do lote já passaram dele.]**
 
Dinho recomenda esperar mais algumas semanas. Chico fica em dúvida, porque o vizinho vendeu um lote parecido. **[NOVO: Sem números, a recomendação do técnico vale o mesmo que a opinião do vizinho, e a decisão final é do Chico.]** Ele vende, e o frigorífico paga menos, porque parte dos animais estava abaixo do peso mínimo

#### C03
Agnaldo é peão na fazenda do Chico. Chico pede que ele e outro funcionário levem o lote **[NOVO: de cerca de 30 animais]** para pesar na balança do vizinho, a 12 km, porque quer saber se os animais já estão no ponto de venda.
 
Agnaldo passa a manhã juntando o lote e embarcando os animais no caminhão. Na balança, os bois chegam agitados e alguns resistem a entrar no tronco. **[NOVO: Quando o animal entra sem resistência, a pesagem leva poucos minutos; quando não entra, é preciso tocar de novo.]** Ele anota o brinco e o peso de cada animal com as mãos sujas e com pressa, porque o vizinho precisa liberar a balança. **[NOVO: Alguns brincos estão sujos ou caíram; nesses casos ele anota a pelagem, como "o pintado de cara branca".]** **[NOVO: As anotações ficam num papel no bolso, e Chico só passa para o caderno à noite.]**
 
Eles voltam no fim da tarde. **[NOVO: No dia da pesagem, duas pessoas ficam ocupadas o dia inteiro, e o trato e a vacinação de outro lote ficam para o dia seguinte.]** Ao passar as anotações a limpo, Chico encontra pesos repetidos e brincos que não consegue ler. Agnaldo não lembra qual animal era qual, e parte da pesagem fica sem uso. **[NOVO: Por dar tanto trabalho, Chico só repete a pesagem dali a alguns meses.]**


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

#### C01
| Elemento | Evidência no cenário |
|---|---|
| Ator(es) | Chico (produtor, quem decide); Agnaldo (peão, dá opinião sobre o lote); Dinho (técnico, visita mensal, estima no olho); comprador (define o peso mínimo) |
| Objetivo(s) | Chico: decidir quais animais vender agora, quais esperar e se vale dar suplemento, sem gastar à toa e sem vender no momento errado |
| Contexto | Pasto com cerca de 30 animais jovens na época da seca; última pesagem há cerca de cinco meses; custo do suplemento; sem balança própria |
| Recursos/informações | Caderno com pesagem antiga e incompleta; observação do lote no pasto; opinião do Agnaldo; visita mensal do Dinho; peso mínimo do comprador |
| Ações | Olhar o lote; procurar a última pesagem no caderno; tentar ligar os pesos aos animais; consultar o Agnaldo; decidir suplementar o lote inteiro e adiar a venda |
| Problemas/rupturas | Nenhum dado de peso entre as pesagens; pesos do caderno sem brinco legível; opiniões diferentes sem número para desempatar; impossível saber qual animal ganhou peso e qual não; decisão tomada para o lote todo, não por animal; erro só aparece na venda |
| Consequências | Gasto com suplemento sem necessidade; parte dos animais fica além do ponto de venda; a mesma decisão se repete no ciclo seguinte sem aprendizado |

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

#### C03
| Elemento | Evidência no cenário |
|---|---|
| Ator(es) | Agnaldo (peão, executa a pesagem); outro funcionário; Chico (produtor, pede a pesagem e usa os dados); vizinho (dono da balança) |
| Objetivo(s) | Agnaldo: pesar o lote inteiro sem errar o animal e voltar a tempo para o resto do serviço. Chico: saber se o lote está no ponto de venda |
| Contexto | Sem balança própria; balança do vizinho a 12 km; lote de cerca de 30 animais; pressa para liberar a balança; trabalho no curral com mãos sujas |
| Recursos/informações | Caminhão; balança e tronco do vizinho; brinco dos animais; papel no bolso; caderno do Chico |
| Ações | Juntar o lote; embarcar no caminhão; conduzir cada animal ao tronco; ler o brinco; anotar brinco e peso; voltar; passar as anotações a limpo |
| Problemas/rupturas | Animais agitados resistem a entrar no tronco; brincos sujos ou caídos; anotação com pressa e mãos sujas; pesos repetidos e brincos ilegíveis; dados só passados a limpo à noite, quando ninguém lembra mais qual animal era qual |
| Consequências | Parte da pesagem perdida; dia inteiro de duas pessoas gasto; outras tarefas adiadas; pesagem repetida só meses depois |

### 5. Implicações para as próximas entregas

Quais tarefas merecem análise? Quais informações precisam ser coletadas? **Não desenhe a solução ainda.**

> Repita para C02, C03... com autoria individual.

#### C01
- Como o produtor decide, animal por animal, entre vender, esperar ou dar suplemento.
- Que informação de peso (kg, arroba, ganho desde a última pesagem) ele realmente usa na decisão.
- Como ele compara hoje o peso atual com o anterior e o que se perde nessa comparação.
- Como se resolve quando produtor, peão e técnico têm opiniões diferentes sobre o mesmo lote.
- Quando e como ele descobre se a decisão foi boa.
- Respostas reais para Q1 a Q5, com produtores.
- Se o produtor quer mesmo acompanhar a evolução do peso ao longo do tempo, e não só o último registro (H03).

#### C02
- Como o técnico decide se um lote está no ponto de venda.
- Como o produtor acompanha o lote entre as visitas do técnico.
- Como o peso de cada animal é associado ao seu brinco.
- Respostas reais para Q1 a Q4, com técnicos e produtores.
- Se o técnico teria acesso aos dados do produtor antes da visita ou só durante ela (H05).
- Se os termos "ponto de venda" e "arroba" são os que técnicos e produtores realmente usam (H08).

#### C03
- Como o peão conduz e identifica cada animal durante a pesagem.
- Como o peso é anotado e em que momento é passado a limpo.
- O que acontece quando o brinco está ilegível ou faltando.
- Respostas reais para Q1 a Q4, com peões e produtores.
- Se é mesmo o peão quem executa a pesagem, ou se o produtor faz isso sozinho.
- Se termos como "brinco", "lote" e "tronco" são os que os peões realmente usam.

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
