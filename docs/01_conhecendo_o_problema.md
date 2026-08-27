# Entrega 1 — Conhecendo o projeto, o usuário e o problema

**Data:** {{13/08/2026}}  
**Status:** 🟨 em andamento
**Responsabilidade:** 1 solução consolidada por equipe

## Objetivo da atividade

Reinterpretar o tema do TCC sob a perspectiva de Interação Humano-Computador e construir um **entendimento comum entre os integrantes da equipe**.

A disciplina utiliza preferencialmente o tema do TCC para os exercícios de IHC. Isso vale tanto para TCCs que já preveem uma interface quanto para trabalhos cujo resultado principal é algoritmo, modelo, API, biblioteca, análise de dados, infraestrutura, estudo experimental ou outro artefato técnico.

> **Importante:** a interface projetada na disciplina é um artefato de aprendizagem de IHC. Ela **não se torna automaticamente uma obrigação do TCC**. Sua incorporação ao trabalho de conclusão depende de decisão da equipe e do orientador.

Antes de preencher, leia [`../GUIA_ESCOPO_IHC.md`](../GUIA_ESCOPO_IHC.md).

Nesta primeira semana a equipe **não deve começar desenhando telas**. Primeiro deverá compreender:

- o que o TCC realmente produz;
- quem poderia obter valor dessa contribuição;
- quais pessoas interagem, administram, configuram, interpretam ou são afetadas;
- o que essas pessoas precisam alcançar;
- como atividades relacionadas acontecem hoje;
- problemas, limitações e contexto;
- alternativas existentes;
- qual recorte de interação fará sentido para a disciplina.

Ao final desta entrega, a equipe deve diferenciar:

- **tema do TCC** × **escopo formal do TCC** × **escopo de IHC da disciplina**;
- **objetivo do projeto** × **objetivo do usuário**;
- **problema do usuário** × **solução tecnológica**;
- **fato conhecido** × **hipótese** × **lacuna de conhecimento**;
- **capacidade técnica** × **forma de uso dessa capacidade**;
- **funcionalidade** × **atividade/resultado que o usuário precisa alcançar**;
- **usuário direto** × **stakeholders**.

---

## Como classificar as respostas

Sempre que a resposta fizer uma afirmação sobre usuários, problemas, atividades, necessidades, contexto ou mercado, use:

- **[F] Fato conhecido** — existe evidência/fonte.
- **[H] Hipótese** — afirmação plausível que ainda precisa ser investigada.
- **[?] Não sabemos ainda** — lacuna relevante.

Quando usar `[F]`, informe a origem. Hipóteses prioritárias devem receber IDs (`H01`, `H02`...) e também ser registradas em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md).

> **Exemplo:** `[H] H01 — DBAs considerariam útil comparar automaticamente o plano atual de execução com uma recomendação produzida pelo algoritmo.`

Uma hipótese explicitada é melhor do que uma suposição escondida.

---

# 0. Identificação do TCC e da equipe

## 0.1 Membros

| Nome completo | Matrícula | GitHub |
|---|---:|---|
| Renan Casemiro Hessel | 24.123.019-2 | RenanCasemiroHessel |
| Gustavo Mendes Franco Lapin Atui | 24.123.072-1 | GustovoAtui |
| Rafael Takahagi Mendes | 22.126.084-7 | rafamendes04 |

## 0.2 Título atual do TCC

Estimativa não invasiva do peso de bovinos leves utilizando Visão Computacional

## 0.3 Orientador(a)

Profa. Dra. Gabriela Oliveira Biondi

## 0.4 Qual é o resultado principal atualmente previsto no TCC?

Marque e descreva:

- [ X ] sistema/aplicação interativa;
- [ X ] algoritmo;
- [ ] modelo de IA/ML/LLM;
- [ ] biblioteca/API/framework;
- [ X ] análise de dataset;
- [ X ] estudo/benchmark/avaliação experimental;
- [ X ] infraestrutura/backend;
- [ ] componente embarcado/IoT;
- [ ] outro: {{...}}.

**Descrição:** {{...}}

## 0.5 O TCC já previa desenvolvimento de interface com usuário?

- [ X ] Sim, a interface já faz parte do TCC.
- [ ] Parcialmente; existe alguma interação, mas ainda não está bem definida.
- [ ] Não. O TCC é predominantemente técnico e não previa interface.

**Explique o que está formalmente previsto no TCC:** {{...}}

> Um sistema de estimativa de peso de bovinos.

---

# 1. Entendendo a contribuição do projeto

## 1.1 Explique o TCC em uma frase, sem citar linguagem de programação, framework ou banco de dados.

Desenvolver e validar um sistema capaz de estimar peso de bovinos a partir de fotos sem a necessidade de uma balança de curral.

## 1.2 Qual situação, atividade ou problema do mundo real motivou o TCC?

[F] : Os métodos atuais comumente utilizados no meio da pecuária geram estresse no animal. 

## 1.3 Qual é a **capacidade/contribuição central** produzida pelo TCC?

Complete, se ajudar:

> “Nosso TCC produz, melhora, analisa ou permite `{{capacidade}}.”

Exemplos: otimizar consultas; classificar imagens; detectar anomalias; comparar modelos; identificar padrões; prever demanda; analisar desempenho; gerar resumos; recomendar configurações.

Nosso TCC produz um aplicativo móvel que estima o peso do bovino a partir de uma foto estática.

## 1.4 O que se espera que esteja diferente **para pessoas, organizações ou processos** se essa contribuição for bem-sucedida?

[H] Pecuaristas conseguiriam monitorar o peso do animal com maior frequência, utilizando apenas um smartphone.
[F] O custo operacional de pesagens frequentes utilizando balanças de curral, é uma barreira real atualmente.

## 1.5 O que é mérito técnico/científico do TCC e o que seria uma possível aplicação prática?

| Mérito/contribuição técnica | Possível aplicação/valor em uso |
|---|---|
| Predição de peso bovino a partir de foto | Produtor sabe o peso do animal no campo sem balança |
| Avaliação comparativa entre modelos para identificar o melhor | Base para aprofundamento no estudo da predição de peso de bovinos |
| Modelo leve compativel com smartphone | App funciona no celular do produtor sem equipamento especial |

---

# 2. Entendendo as pessoas envolvidas

## 2.1 Quem interage diretamente com o produto, se já existe interface prevista?

De maneira geral: Pecuarista, Frigorificos.

## 2.2 Quem poderia **usar, configurar, administrar, operar, interpretar ou tomar decisões** a partir da contribuição técnica?

Considere perfis profissionais e stakeholders, não apenas consumidores finais.

| Perfil | Relação com a contribuição | O que faria | Status/evidência |
|---|---|---|---|
| Pecuarista | Usuário Direto  | Fotografa o animal e usa o peso predito para decisões de manejo | H |
| Técnico agropecuário | Consultor de manejo  | Consulta o histórico de peso predito por animal para orientar tratamentos e nutrição | H |


## 2.3 Existem pessoas afetadas que não usariam a interface diretamente?

| Stakeholder | Como é afetado | Usa interface? | Status/evidência |
|---|---|---|---|
| Frigorifero/Comprador | Recebe apenas o histórico de peso do animal | não | H |
| Veterinário | Recebe o historico de peso e de imagem do animal | não | H | 

## 2.4 Que características desses perfis podem influenciar a interação?

Considere conhecimento do domínio, experiência tecnológica, frequência de uso, necessidades de acessibilidade, responsabilidade profissional, familiaridade com métricas, linguagem técnica, urgência etc.

{{[F/H/?] ...}}

[H]  O produtor rural pode ter baixa familiaridade com aplicativos técnicos, preferindo poucos passos e resultado imediato na tela.
[F] Smartphones são amplamente usados no meio rural brasileiro.

---

# 3. Entendendo objetivos e atividades

## 3.1 O que o usuário está tentando conseguir no mundo real?

Não responda “usar o algoritmo”, “clicar no sistema” ou “ver o dashboard”.

[H] O produtor não quer "usar visão computacional" ele quer uma resposta confiável em quilogramas e arrobas com o mínimo de esforço.
## 3.2 Quais são as atividades mais importantes?

| ID | Atividade/objetivo | Quem realiza | Frequência/criticidade inicial | Status/evidência |
|---|---|---|---|---|
| A01 | fotografar o animal e receber o peso predito | pecuarista | alta | [H] |
| A02 | Identificar o animal antes de salvar o peso | pecuarista | alta | [H] |
| A03 | consultar o historico de peso do bovino | pecuarista/comprador/veterinário | média | H |  

## 3.3 Qual atividade parece mais frequente? Por quê?

[F] A01 - fotografar o animal e receber o peso predito, é a principal funcionalidade do aplicativo e as outras atividades dependem dela. 

## 3.4 Qual parece mais crítica? Que consequência existe se for mal executada?

[H] A02 - identificar o animal antes de salvar o peso, caso o bovino identificado seja catalogado de maneira errada irá interferir em todas as outras pesagens do mesmo. 
---

# 4. Entendendo o problema ou processo atual

## 4.1 Como essas atividades são realizadas hoje, antes da interface imaginada na disciplina?

[F] Com balança. Conduzindo o animal ao curral, passá-lo pelo brete (tronco de contenção), registrar o peso e anotar manualmente. O equipamento custa entre R$ 30.000 e R$ 50.000.

[H] Muitos produtores pesam os animais apenas 2 a 4 vezes por ano pela dificuldade.  

## 4.2 O que é difícil, demorado, confuso, repetitivo, arriscado ou pouco transparente?

[F] Conduzir o rebanho até a balança, exige mão de obra e tempo.
[F] O animal ficar preso gera estresse.
[H] Como os registros são feitos manualmente muitas vezes são perdidos.

## 4.3 Que informações o profissional precisa interpretar para tomar decisão?

[H] Peso atual em kg e arrobas, ganho de peso desde a última medição e se o animal atingiu o peso mínimo de abate.

## 4.4 O que acontece quando a atividade falha ou quando o resultado é interpretado incorretamente?

[H] O produto deixa de ser vantajoso para o usuário.

## 4.5 Conte uma situação concreta.

Escreva uma pequena narrativa com pessoa, objetivo, atividade, contexto, dificuldade e consequência. **Não descreva ainda a futura solução.**



{{[F/H/?] narrativa...}}

## 4.6 Que evidência existe hoje?

| Evidência/fonte | O que sustenta | Limitação |
|---|---|---|
| Resultados experimentais do próprio TCC | O peso pode ser estimado através de uma imagem estática | Pouco material para pesquisa em outras raças |
| Resultados experimentais do próprio TCC | O peso pode ser estimado através de uma imagem estática | Pouco material para pesquisa em outras raças |
| Resultados experimentais do próprio TCC | O peso pode ser estimado através de uma imagem estática | Pouco material para pesquisa em outras raças |

---

# 5. Entendendo o contexto de uso

## 5.1 Onde e em quais situações a interação poderia ocorrer?

[H] Curral ou pasto durante o manejo de rotina.

## 5.2 Em quais dispositivos/equipamentos?

[F] Smartphone pessoal do produtor ou peão.

## 5.3 Existem condições físicas relevantes?

Considere iluminação, ruído, mobilidade, conexão, privacidade, uso compartilhado, interrupções, pressão de tempo etc.

[H] Sol forte reduzindo a legibilidade da tela; poeira, barro e mãos sujas ou com luva; uso com uma das mãos enquanto a outra controla portão ou animal; animal em movimento, o que limita o tempo de enquadramento; conexão de internet instável ou inexistente em parte da propriedade; ruído e pressa durante o manejo, com interrupções constantes.

## 5.4 Existem fatores sociais ou organizacionais?

Considere papéis, chefias, equipes, permissões, aprovação, responsabilidade profissional, auditoria, turnos e colaboração.

Sim.
[H] O aparelho pode ser operado pelo vaqueiro, mas a decisão é do produtor ou do gerente da fazenda.

## 5.5 Existe necessidade de histórico, rastreabilidade ou auditoria?

Sim.
[H] Histórico por animal identificado (brinco) para acompanhar ganho de peso ao longo do tempo.

## 5.6 Um erro pode produzir consequência relevante? Qual?

{{[F/H/?] ...}}

---

# 6. Entendendo mercado e alternativas existentes

> Nesta entrega faça apenas um **levantamento inicial**. A análise aprofundada ocorre na Entrega 2.

## 6.1 Como pessoas resolvem problemas semelhantes hoje?

| Alternativa atual | Quem usa | Para quê | Status/evidência |
|---|---|---|---|
| Balança de tronco | Fazenda de médio/grande porte | Pesagem precisa de todo o lote | [F] Solução padrão com alto custo  |
| Estimativa visual do peão | Produtores e funcionários experientes | Decisão rápida do dia a dia | [H] Sem custo e altamente variável  |
| Pesagem apenas na venda | Todos | Fechamento comercial | [F] Não é mais possível orientar o manejo devido  |

## 6.2 Existem produtos que atuam na mesma área, mesmo sem serem equivalentes ao TCC?

Sim
[?] Softwares de gestão de rebanho, sistemas de pesagem eletrônica integrados a leitores de brinco e soluções comerciais de pecuária de precisão.

## 6.3 Quais interfaces profissionais esse público já conhece?

Exemplos possíveis: ferramentas de banco, IDEs, consoles de nuvem, dashboards, plataformas de dados, ferramentas de monitoramento, painéis de IA, sistemas administrativos.

[H] WhatsApp, aplicativos de banco, apps de clima e de cotação da arroba, sistemas de cooperativa e leilão, e softwares de gestão de rebanho em uma parcela do público

## 6.4 O que essas soluções parecem fazer bem?

[H] Registro estruturado por animal e por lote, relatórios de evolução do rebanho e integração com equipamentos de pesagem eletrônica.

## 6.5 O que parecem fazer mal, dificultar ou não atender?

[H] Exigem cadastro longo antes de qualquer uso, pressupõem conexão estável, cobram assinatura e ainda dependem de uma balança para obter o dado de peso.

## 6.6 Que padrões de interface ou vocabulário parecem familiares a esse público?

[H] Arroba (@) como unidade de negociação junto com o quilograma, número do brinco, lote, pasto, "ponto de abate"; listas simples, botão de câmera e navegação rasa no estilo WhatsApp.

---

# 7. Derivando o escopo de IHC da disciplina

## 7.1 Escolha o caminho do projeto

### Caminho A — TCC já possui interface

Explique qual parte da interface será usada como recorte da disciplina e por que esse fluxo é relevante.

[F] O recorte da disciplina será o fluxo de captura de foto -> identificação do animal -> visualização do peso estimado, que corresponde às telas 3 (captura de fotos) e 4 (dashboard/histórico) da interface prevista.
Esse fluxo é relevante porque concentra as duas atividades mais críticas já mapeadas: A01 (fotografar e receber o peso, sendo essa a mais frequente) e A02 (identificar o animal antes de salvar, sendo essa a mais crítica, já que erro aqui compromete o histórico inteiro daquele animal). 
[H] As telas 1 e 2 (login/cadastro e cadastro do fazendeiro) ficam fora do recorte principal por serem telas de configuração única, não de uso recorrente — mas podem aparecer de forma simplificada no protótipo pra dar contexto de navegação.

### Caminho B — TCC não possui interface prevista

Faça o exercício de transferência de uso:

> **Imagine que o TCC foi concluído com sucesso e uma empresa, laboratório ou organização quer transformar a contribuição em algo utilizável. Quem precisaria interagir com ela e para quê?**

Responda:

1. quem poderia contratar/adotar a solução? {{...}}
2. quem seria o usuário direto? {{...}}
3. quem administraria/configuraria? {{...}}
4. quem interpretaria resultados? {{...}}
5. quem tomaria decisões? {{...}}
6. quais dados/entradas seriam necessários? {{...}}
7. quais resultados deveriam ser compreendidos? {{...}}
8. que erros/rupturas seriam possíveis? {{...}}

## 7.2 Qual perfil será priorizado no projeto de IHC?

[F] Pecuarista (usuário direto)

**Por que esse perfil foi escolhido?** 
[F] Porque é quem de fato maneja o app no curral/pasto, no smartphone pessoal, no momento da pesagem. O técnico agropecuário é perfil secundário, pois ele consulta e orienta, mas não é quem fotografa o animal no dia a dia.

## 7.3 Qual objetivo desse usuário será priorizado?

[H] Obter o peso estimado de um bovino específico de forma rápida e confiável, sem precisar de balança, garantindo que o peso seja corretamente associado ao animal certo no histórico.

## 7.4 Que interface será explorada na disciplina?

Complete:

> **Para fins da disciplina de IHC, será projetada uma interface que permita a `{{perfil}}` utilizar `{{capacidade/resultado do TCC}}` para `{{objetivo}}`, no contexto de `{{situação}}`.**

[F] Para fins da disciplina de IHC, será projetada uma interface que permita ao pecuarista utilizar a estimativa de peso do bovino via foto para registrar o peso do animal certo no histórico, sem precisar de balança, no contexto de curral ou pasto, usando o smartphone pessoal, com sol forte, poeira, mãos sujas e conexão instável.

## 7.5 Qual é a relação dessa interface com o TCC?

- [x] Já fazia parte do TCC.
- [ ] É um aprofundamento de algo parcialmente previsto.
- [ ] É uma extensão conceitual criada para a disciplina.
- [ ] É um protótipo demonstrativo de aplicação potencial.
- [ ] Outra: {{...}}.

> **Declaração:** a interface desenvolvida nesta disciplina é um artefato de aprendizagem de IHC baseado no tema do TCC. Sua inclusão ou implementação no TCC somente ocorrerá se isso for posteriormente decidido pela equipe e pelo orientador.

---

# 8. Levantando possibilidades de interação — sem desenhar ainda

A equipe pode registrar possibilidades para investigação. **Não significa que todas serão implementadas.**

Marque apenas as que parecem plausíveis e explique o objetivo correspondente.

| Possibilidade | Pode fazer sentido? | Objetivo/tarefa que justificaria | Evidência atual |
|---|---|---|---|
| Dashboard/visão geral | sim | Reunir os animais/lotes do produtor com peso mais recente de cada um, pra ele ter visão geral do rebanho sem abrir animal por animal | [F] já previsto como tela 4 do projeto (dashboard/histórico) |
| Configuração/parametrização | sim | Cadastro inicial do fazendeiro (quantidade de gado, localização) | [F] já previsto como tela 2 do projeto |
| Entrada/upload/seleção de dados | sim | Capturar foto do bovino pra gerar a estimativa de peso | [F] já previsto como tela 3 do TCC (captura de fotos) |
| Acompanhamento de processamento | talvez | Mostrar status enquanto o modelo processa a foto (segmentação + regressão não é instantâneo) | ?] não sabemos o tempo de inferência do pipeline rodando em campo/mobile, sendo essa uma lacuna a validar |
| Relatório/resultados | sim | Exibir o peso estimado (em kg e/ou @) depois da foto, com clareza de que é uma estimativa e não pesagem exata | [F] é a saída central do TCC, atualmente sendo MAE ~20,75 kg, acerto em ±10% em ~48% dos casos, então a interface precisa comunicar isso de forma honesta |
| Histórico com busca/filtros | sim | Consultar o histórico de peso de um bovino específico (busca por brinco/lote) | [F] já previsto como parte da tela 4; brinco e lote são vocabulário já validado como familiar ao público |
| Comparação de resultados | talvez | 	Visualizar evolução de peso do animal ao longo do tempo (ganho de peso entre pesagens) | H] hipótese de que o produtor quer acompanhar engorda, não só o valor pontual, sendo necessário validar com usuário |
| Explicabilidade/detalhamento | talvez | Não faz sentido explicar a CNN, mas pode fazer sentido comunicar a margem de erro/confiança da estimativa | [H] hipótese de que mostrar incerteza (ex: "peso estimado: 180kg ± 20kg") ajuda o produtor a confiar mais no número do que um valor seco |
| Administração/configurações globais | não | 	Não há indício de necessidade de administração central (múltiplas fazendas, múltiplos operadores por conta) | [?] não foi definido se o app atende 1 produtor = 1 conta ou estrutura multi-usuário |
| Usuários/perfis/permissões | talvez | Diferenciar visualização do pecuarista (seu próprio rebanho) da do técnico agropecuário (pode acompanhar vários produtores) | [H] hipótese, decorre do perfil secundário já definido, mas não há confirmação de que o técnico usa o mesmo app |
| CRUD de entidade do domínio | sim | Cadastrar/editar/excluir bovino (brinco, lote) | [F] decorre diretamente da atividade mais crítica já mapeada |
| Auditoria/logs | não | 	Não há indício de necessidade de rastrear alterações/quem editou o quê | [?] pode ganhar relevância se peso errado gerar disputa com frigorífico, mas não foi validado |
| Alertas/ocorrências | talvez | Avisar quando a foto capturada não está em condições boas pra estimativa (ângulo, distância, animal em movimento) | [H] hipótese ligada às condições reais de uso (sol forte, poeira, animal se mexendo) que podem prejudicar a qualidade da foto |
| Ajuda/documentação | talvez | Orientar o pecuarista sobre como tirar a foto corretamente (distância, ângulo) | [H] hipótese, reforçada pelo contexto de baixa familiaridade digital do público e pela sensibilidade do modelo à imagem de entrada |

> **Atenção:** “login + dashboard + CRUD” não é uma solução universal. Cada padrão deve surgir de uma tarefa real.

---

# 9. Benefícios e ações iniciais

## 9.1 Qual benefício concreto o projeto de IHC pretende oferecer?

| Benefício esperado | Problema/necessidade | Usuário | Status/evidência |
|---|---|---|---|
| Conseguir estimar o peso do rebanho sem precisar comprar/alugar balança de tronco | [F] balança de tronco custa R$ 30-50 mil, por isso muitos produtores pesam só 2-4 vezes por ano | Pecuarista | [F] já validado como motivação central do TCC |
| Reduzir o risco de erro na hora de associar o peso ao animal certo | [F] Identificar o animal foi mapeada como a atividade mais crítica, pois um erro aqui compromete todo o histórico daquele animal | Pecuarista | [F] já decidido nas entregas anteriores |
| Conseguir usar o app mesmo em condições ruins de campo (sol forte, mãos sujas, sinal instável) | [F] Contexto de uso real é curral/pasto | Pecuarista | [H] hipótese de que isso é viável — ainda não testado com interface real |

## 9.2 Que ações o usuário deverá conseguir realizar?

| ID | O usuário precisa conseguir... | Para alcançar... | Prioridade inicial |
|---|---|---|---|
| F01 | Tirar/enviar uma foto do bovino pelo celular | Receber o peso estimado sem balança | alta |
| F02 | Identificar/vincular a foto ao animal certo (por brinco ou lote) | Garantir que o peso seja salvo no histórico correto | alta |
| F03 | Consultar o histórico de peso de um bovino específico | Acompanhar a evolução do animal ao longo do tempo | alta |
| F04 | Ver uma lista/visão geral dos animais do seu rebanho | Ter noção geral do estado do rebanho sem abrir animal por animal | média |
| F05 | Cadastrar novo bovino (brinco, lote) | Ter o animal disponível para registrar pesagens futuras | média |
| F06 | Entender que o peso mostrado é uma estimativa, não uma pesagem exata | Tomar decisões de manejo/venda com expectativa correta em relação à margem de erro do modelo | alta |

## 9.3 Tecnologias/restrições já definidas no TCC

A tecnologia aparece **agora**, depois do entendimento do uso.

| Tecnologia/restrição | Por que existe | Possível impacto na interação |
|---|---|---|
| Pipeline: segmentação (YOLO zero-shot) -> medidas morfométricas -> regressão (CNN ResNet18) | [F] é a arquitetura técnica definida e validada no TCC 1 | [?] não sabemos o tempo de inferência em produção/mobile — impacta se precisa de tela de "processando" |

---

# 10. Hipóteses e dúvidas prioritárias

| ID | Hipótese/dúvida | Por que importa | Como poderá ser investigada |
|---|---|---|---|
| H01 | {{...}} | {{...}} | Entrega 2/3/7/... |
| H02 | {{...}} | {{...}} | {{...}} |
| H03 | {{...}} | {{...}} | {{...}} |

Registre em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md).

---

# 11. Síntese da equipe

| Pergunta | Síntese atual |
|---|---|
| Qual é a contribuição central do TCC? | {{...}} |
| O TCC já previa interface? | {{...}} |
| Quem é o usuário prioritário de IHC? | {{...}} |
| O que ele precisa alcançar? | {{...}} |
| Qual problema/atividade será estudado? | {{...}} |
| Como isso acontece hoje? | {{...}} |
| Qual é o contexto de uso? | {{...}} |
| Que interface/recorte será explorado? | {{...}} |
| Como a interface se relaciona ao TCC? | {{...}} |
| Quais pontos ainda são hipóteses? | {{H01...}} |

### Delimitação

**Dentro do escopo de IHC:** {{...}}  
**Fora do escopo de IHC:** {{...}}  
**Dentro do escopo formal do TCC:** {{...}}  
**Interface da disciplina será implementada no TCC?** não definido / sim / não — {{justificativa, se houver}}

---

# 12. Como esta entrega alimenta as próximas

- **Entrega 2:** verifica mercado, concorrentes e interfaces profissionais representativas.
- **Entrega 3:** detalha perfis e contexto.
- **Entrega 4:** aprofunda situações problemáticas.
- **Entrega 5:** modela tarefas centrais.
- **Entrega 6:** experimenta alternativas em baixa fidelidade.
- **Entrega 7:** investiga hipóteses com dados.
- **Entrega 8:** define restrições e metas de usabilidade.
- **Entregas 9–11:** transformam o recorte em modelo de interação e protótipo.
- **Entregas 12–14:** avaliam a interface construída na disciplina.

A Entrega 1 é uma **fotografia inicial do conhecimento**. Ela pode e deve ser revisada quando surgirem evidências.

---

# 13. Relação com INOVA e comunicação do projeto

Prepare uma explicação de até três frases:

1. **Problema/atividade humana:** {{...}}
2. **Contribuição técnica do TCC:** {{...}}
3. **Como uma pessoa poderia utilizar essa contribuição:** {{...}}

Essa síntese ajuda a apresentar o projeto para público não especializado sem reduzir seu mérito técnico.

---

# Checklist de qualidade

- [ ] Está clara a diferença entre tema do TCC, escopo formal do TCC e escopo de IHC.
- [ ] A equipe declarou se o TCC já previa interface.
- [ ] Se não previa, foi derivado um usuário plausível e um objetivo de uso.
- [ ] A interface de IHC não foi apresentada como obrigação automática do TCC.
- [ ] A contribuição do TCC foi descrita sem começar por tecnologias de implementação.
- [ ] Usuários diretos e stakeholders foram diferenciados.
- [ ] Foram considerados profissionais que configuram, administram, interpretam ou decidem, quando pertinente.
- [ ] Objetivo do usuário não foi confundido com objetivo do projeto.
- [ ] Processo/problema atual foi descrito antes da solução.
- [ ] Existe situação concreta de uso/problema.
- [ ] Contexto físico, social/organizacional, dispositivos e consequências de erro foram considerados.
- [ ] Mercado/alternativas existentes foram levantados inicialmente.
- [ ] Possibilidades como dashboard, relatório, histórico, filtros e CRUD foram tratadas como hipóteses de solução, não como requisitos automáticos.
- [ ] Cada possibilidade de interface tem um objetivo/tarefa que poderia justificá-la.
- [ ] Afirmações relevantes estão marcadas `[F]`, `[H]` ou `[?]`.
- [ ] Hipóteses prioritárias receberam IDs e foram para a rastreabilidade.
- [ ] O recorte de IHC é viável para modelar, prototipar e avaliar no semestre.
- [ ] A equipe consegue explicar problema humano → contribuição computacional → forma de uso.
