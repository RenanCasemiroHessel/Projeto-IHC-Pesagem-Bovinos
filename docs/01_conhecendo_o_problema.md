# Entrega 1 — Conhecendo o projeto, o usuário e o problema

**Data:** 13/08/2026 (revisada em 06/10/2026, após o feedback do professor)  
**Status:** 🟦 revisada  
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

**Nota da equipe sobre esta revisão:**

- Quando algo é uma escolha nossa de escopo ou de projeto, e não uma afirmação sobre os usuários, escrevemos **"Decisão da equipe:"**. Decisão não é fato sobre o mundo.
- Terminologia usada em todo o documento: **peso estimado** é o valor produzido pelo modelo a partir da foto. **Pesagem** é a medição feita com balança.
- Usamos `[?]` só para perguntas que realmente precisam de investigação. As lacunas principais estão reunidas na tabela da seção 4.6 e na lista da seção 10.

---

# 0. Identificação do TCC e da equipe

## 0.1 Membros

| Nome completo | Matrícula | GitHub |
|---|---:|---|
| Renan Casemiro Hessel | 24.123.019-2 | RenanCasemiroHessel |
| Gustavo Mendes Franco Lapin Atui | 24.123.072-1 | GustavoAtui |
| Rafael Takahagi Mendes | 22.126.084-7 | rafamendes04 |

## 0.2 Título atual do TCC

Estimativa não invasiva do peso de bovinos leves utilizando Visão Computacional

## 0.3 Orientador(a)

Profa. Dra. Gabriela Oliveira Biondi

## 0.4 Qual é o resultado principal atualmente previsto no TCC?

Marque e descreva:

- [ X ] sistema/aplicação interativa;
- [ X ] algoritmo;
- [ X ] modelo de IA/ML/LLM;
- [ X ] análise de dataset;
- [ X ] estudo/benchmark/avaliação experimental;
- [ X ] infraestrutura/backend;
- [ ] componente embarcado/IoT;
- [ ] outro.

**Descrição:** Sistema de estimativa de peso bovino por imagem. O pipeline tem três partes: segmentação da imagem (YOLO), extração de medidas morfométricas do animal e regressão com uma CNN ResNet18. A ideia é que esse pipeline seja acessado por um aplicativo móvel.

## 0.5 O TCC já previa desenvolvimento de interface com usuário?

- [ X ] Sim, a interface já faz parte do TCC.
- [ ] Parcialmente; existe alguma interação, mas ainda não está bem definida.
- [ ] Não. O TCC é predominantemente técnico e não previa interface.

**Explique o que está formalmente previsto no TCC:** [F] O TCC prevê um aplicativo móvel como forma de acesso ao pipeline de estimativa de peso. A previsão tem quatro telas: (1) login/cadastro, (2) cadastro do fazendeiro (quantidade de gado e localização), (3) captura de fotos e (4) dashboard/histórico. Fonte: TCC 1.

---

# 1. Entendendo a contribuição do projeto

## 1.1 Explique o TCC em uma frase, sem citar linguagem de programação, framework ou banco de dados.

Desenvolver e validar um sistema capaz de estimar o peso de bovinos a partir de fotos, sem precisar de balança de curral.

## 1.2 Qual situação, atividade ou problema do mundo real motivou o TCC?

[H] A pesagem com balança no curral exige estrutura cara e mão de obra, e a equipe supõe que o animal fica estressado ao ser contido.

## 1.3 Qual é a **capacidade/contribuição central** produzida pelo TCC?

Complete, se ajudar:

> “Nosso TCC produz, melhora, analisa ou permite `{{capacidade}}`.”

Separamos em três níveis, porque são coisas diferentes:

- **Capacidade técnica (contribuição do TCC):** [F] estimar o peso de bovinos leves a partir de uma imagem digital, sem balança. Fonte: resultados do TCC 1.
- **Forma de disponibilizar essa capacidade:** [F] aplicativo móvel, previsto no TCC. Fonte: TCC 1.
- **Valor em uso para a pessoa:** [H] apoiar o acompanhamento do peso e decisões de manejo sem precisar levar o animal até a balança.

## 1.4 O que se espera que esteja diferente **para pessoas, organizações ou processos** se essa contribuição for bem-sucedida?

[H] Pecuaristas conseguiriam acompanhar o peso dos animais com mais frequência, usando só um smartphone.

[H] O custo e o trabalho de pesagens frequentes com balança seriam uma barreira para o produtor hoje.

## 1.5 O que é mérito técnico/científico do TCC e o que seria uma possível aplicação prática?

| Mérito/contribuição técnica | Possível aplicação/valor em uso |
|---|---|
| [F] Estimativa de peso a partir de foto, com os resultados do TCC 1 (MAE ~20,75 kg) | [H] O produtor saberia o peso estimado do animal no campo, sem balança |
| [F] Comparação entre modelos para identificar o melhor (a CNN ResNet18 foi o melhor resultado) | [H] Base para continuar o estudo de estimativa de peso no TCC 2 |
| [H] Modelo de porte pequeno (ResNet18) como candidato a rodar em celular | [F] Ainda não foi testado em celular (TCC 1), então não sabemos se roda no aparelho do produtor sem equipamento extra |

---

# 2. Entendendo as pessoas envolvidas

## 2.1 Quem interage diretamente com o produto, se já existe interface prevista?

Decisão da equipe: o usuário direto será o **pecuarista**.

[H] O técnico agropecuário pode ser usuário secundário (H05).

Decisão da equipe: frigorífico/comprador e veterinário não operam a interface, só receberiam informação.

## 2.2 Quem poderia **usar, configurar, administrar, operar, interpretar ou tomar decisões** a partir da contribuição técnica?

Considere perfis profissionais e stakeholders, não apenas consumidores finais.

| Perfil | Relação com a contribuição | O que faria | Status/evidência |
|---|---|---|---|
| Pecuarista | Usuário direto priorizado (decisão da equipe). Pode ser proprietário, gerente ou quem executa o manejo | Fotografaria o animal e usaria o peso estimado em decisões de manejo | [H] |
| Peão/vaqueiro | Possível operador em campo, ainda sem decisão se é um perfil separado do pecuarista | Operaria o celular durante o manejo, enquanto outra pessoa decide | [H] |
| Técnico agropecuário | Usuário secundário possível ou só stakeholder, conforme H05 | Consultaria o histórico de peso estimado por animal para orientar nutrição e tratamento | [H] |

Resumo dos papéis, para não misturar:

| Papel | Quem (hipótese) |
|---|---|
| Opera a interface | [H] pecuarista ou peão/vaqueiro |
| Decide a partir do resultado | [H] produtor ou gerente da fazenda |
| Recebe a informação sem usar a interface | [H] frigorífico/comprador e veterinário |
| Possível usuário secundário em versão futura | [H] técnico agropecuário |

## 2.3 Existem pessoas afetadas que não usariam a interface diretamente?

| Stakeholder | Como é afetado | Usa interface? | Status/evidência |
|---|---|---|---|
| Frigorífico/comprador | Poderia receber o histórico de peso do animal | não | [H] |
| Veterinário | Poderia receber o histórico de peso do animal | não | [H] |

## 2.4 Que características desses perfis podem influenciar a interação?

Considere conhecimento do domínio, experiência tecnológica, frequência de uso, necessidades de acessibilidade, responsabilidade profissional, familiaridade com métricas, linguagem técnica, urgência etc.

[H] O produtor rural pode ter baixa familiaridade com aplicativos técnicos e preferir poucos passos e resultado imediato na tela.

[F] 77,2% da população rural de 10 anos ou mais tinha celular para uso pessoal em 2024. Fonte: PNAD Contínua TIC 2024, IBGE. O dado fala de posse de celular, não de smartphone nem de uso no manejo.

[?] Dentro de "pecuarista" cabem pessoas bem diferentes. Na investigação precisamos descobrir o papel no manejo, a experiência, a frequência da tarefa, a relação com tecnologia, o aparelho disponível, quem decide e como é a propriedade.

---

# 3. Entendendo objetivos e atividades

## 3.1 O que o usuário está tentando conseguir no mundo real?

Não responda “usar o algoritmo”, “clicar no sistema” ou “ver o dashboard”.

[H] O produtor não quer "usar visão computacional". Ele quer saber o peso do animal em quilos e arrobas com pouco esforço, e saber o quanto pode confiar nesse número para decidir.

## 3.2 Quais são as atividades mais importantes?

| ID | Atividade/objetivo | Quem realiza | Frequência/criticidade inicial | Status/evidência |
|---|---|---|---|---|
| A01 | Fotografar o animal e receber o peso estimado | pecuarista (ou peão) | Central no fluxo (decisão da equipe). Se repete a cada animal numa sessão de pesagem. A frequência real ao longo do ano ainda não tem evidência | [H] |
| A02 | Identificar o animal antes de salvar o peso estimado | pecuarista (ou peão) | Acontece junto com A01. Criticidade prevista alta | [H] |
| A03 | Consultar o histórico de peso estimado do bovino | pecuarista (técnico, conforme H05) | Frequência ainda sem evidência. Criticidade prevista média | [H] |

## 3.3 Qual atividade parece mais frequente? Por quê?

- **Atividade central do fluxo:** decisão da equipe: A01, porque as outras atividades dependem dela. Isso mostra importância no sistema, não frequência de uso.
- **Atividade prevista como mais frequente:** [H] A01 e A02, porque se repetem para cada animal durante uma sessão de pesagem.
- **Evidência disponível sobre frequência:** [?] nenhuma. Não sabemos com que frequência o produtor pesa hoje nem com que frequência pesaria se tivesse uma solução por foto.

## 3.4 Qual parece mais crítica? Que consequência existe se for mal executada?

Decisão da equipe: priorizar A02 como a atividade mais crítica. Isso não foi validado com usuários.

[H] Se o bovino for identificado errado, o peso estimado entra no histórico do animal errado e interfere em todos os outros registros de peso dele.

---

# 4. Entendendo o problema ou processo atual

## 4.1 Como essas atividades são realizadas hoje, antes da interface imaginada na disciplina?

[H] O produtor leva o animal ao curral, passa pelo brete (tronco de contenção) com balança, lê o peso e anota à mão. A pesquisa informal do TCC 1 aponta que o processo é trabalhoso, mas não temos fonte formal sobre as etapas.

[H] A balança de tronco custa entre R$ 30 mil e R$ 50 mil. A pesquisa informal do TCC 1 encontrou uma faixa maior, de R$ 15 mil a R$ 80 mil, e a faixa usada aqui ainda precisa de fonte.

[H] Muitos produtores pesam os animais só 2 a 4 vezes por ano, por causa da dificuldade do processo.

## 4.2 O que é difícil, demorado, confuso, repetitivo, arriscado ou pouco transparente?

[H] Conduzir o rebanho até a balança exige mão de obra e tempo.

[H] O animal preso no tronco fica estressado.

[H] Como os registros são feitos à mão, muitas vezes se perdem.

## 4.3 Que informações o profissional precisa interpretar para tomar decisão?

[H] Peso atual em kg e arrobas, ganho de peso desde a última medição e se o animal atingiu o peso mínimo de abate.

[H] O modelo só cobre bovinos até 250 kg, então decisões ligadas a abate podem ficar fora do que ele consegue estimar.

## 4.4 O que acontece quando a atividade falha ou quando o resultado é interpretado incorretamente?

São hipóteses da equipe, ainda sem verificação com produtores, técnicos ou veterinários.

- [H] **Peso associado ao animal errado (falha em A02).** O histórico daquele bovino passa a ter um valor que não é dele, e o do outro animal fica com buraco ou dado trocado. Quem consulta depois pode decidir com base num histórico que parece certo e não está.
- [H] **Peso estimado lido como se fosse pesagem de balança.** O produtor pode tratar o número como exato. O erro médio do modelo no TCC 1 é de cerca de 20,75 kg [F], então o animal pode estar bem mais leve ou mais pesado do que o número mostrado. Isso pode levar a vender cedo ou tarde demais.
- [H] **Foto mal feita** (animal se mexendo, luz ruim, ângulo errado) que gera um peso estimado pior sem o usuário perceber. Ele salva e usa o número como se estivesse normal.

## 4.5 Conte uma situação concreta.

Escreva uma pequena narrativa com pessoa, objetivo, atividade, contexto, dificuldade e consequência. **Não descreva ainda a futura solução.**

[H] Situação ilustrativa, construída pela equipe a partir do processo e das dificuldades descritos acima. Não vem de entrevista com produtor. Nome e detalhes são inventados para exemplificar.

João cria gado Nelore numa propriedade no interior de São Paulo e tem cerca de 80 animais jovens no pasto. Ele quer saber quais já ganharam peso suficiente para vender e quais ainda precisam de mais tempo. Para isso, precisa pesar os animais um por um.

Num dia de pesagem, João chama dois funcionários e separa um lote no curral. Os animais passam um de cada vez pelo corredor até o tronco, onde ficam presos para a balança marcar o peso. Um funcionário lê o número, outro anota no caderno e o animal é solto. O processo toma boa parte do dia e para o resto do trabalho da fazenda. Alguns animais ficam agitados no tronco, e João acredita que isso muda o peso na hora.

Como dá muito trabalho, João só faz isso duas ou três vezes por ano. Nos meses entre uma pesagem e outra, ele avalia os animais "no olho" ou pergunta para o peão. No fim, às vezes vende um lote antes ou depois do melhor momento. Na hora de comparar com a pesagem anterior, também acontece de a anotação do caderno estar incompleta ou de não bater com o animal.

## 4.6 Que evidência existe hoje?

| Evidência/fonte | O que sustenta | Limitação |
|---|---|---|
| Resultados experimentais do TCC 1 (dataset BMGF, lotes B2 e B4, 4.818 amostras) | [F] O peso pode ser estimado a partir de imagem estática com MAE ~20,75 kg e acerto dentro de ±10% em ~48% dos casos | Dataset de Bangladesh; bovinos taurino-zebuínos; não testado em Nelore brasileiro |
| Literatura do TCC 1 (Berckmans 2017, Tedeschi 2021, Cominotte 2020) | [F] Pesagem não invasiva é um problema reconhecido em pecuária de precisão | Contexto europeu e americano predominante; raças e condições de campo diferentes |
| Pesquisa de mercado informal feita durante o TCC 1 | Indício de que a balança de contenção custa entre R$ 15 mil e R$ 80 mil e de que o processo é trabalhoso | Informal, sem amostragem sistemática de produtores brasileiros. Por isso custo e processo seguem como [H] |
| PNAD Contínua TIC 2024 (IBGE) | [F] 77,2% da população rural de 10 anos ou mais tinha celular pessoal; em 65,8% dos domicílios rurais o serviço de rede móvel celular funcionava | Mede posse de celular, não uso de smartphone no manejo. Fala de domicílio, não de curral ou pasto |

O que ainda **não** tem evidência e continua em aberto:

| Afirmação | Status | Que tipo de evidência falta |
|---|---|---|
| Custo da balança, estresse na pesagem e trabalho do processo | [H] | Fonte técnica e entrevista com produtores |
| Frequência de pesagem hoje (2 a 4 vezes por ano) | [H] | Entrevistas ou dados de propriedades |
| Perda de registros manuais | [H] | Entrevistas |
| Como o processo de pesagem acontece na prática hoje (etapas, anotação à mão) | [H] | Entrevistas e observação em campo |
| Familiaridade tecnológica e uso do celular no manejo | [H] | Entrevistas e observação em campo |
| Quem opera a captura no manejo | [?] | Entrevistas e observação em campo |
| Vocabulário do público (arroba, brinco, lote) | [H] | Entrevistas e observação |
| Necessidade de histórico de peso | [H] | Entrevistas |
| Papel de frigorífico, veterinário e técnico | [H] | Entrevistas |
| Captura com uma foto viável em campo | [H] | Teste com protótipo e observação |

---

# 5. Entendendo o contexto de uso

## 5.1 Onde e em quais situações a interação poderia ocorrer?

[H] Curral ou pasto, durante o manejo de rotina.

## 5.2 Em quais dispositivos/equipamentos?

[H] Smartphone pessoal do produtor ou do peão. O que sabemos é só a posse de celular.

## 5.3 Existem condições físicas relevantes?

Considere iluminação, ruído, mobilidade, conexão, privacidade, uso compartilhado, interrupções, pressão de tempo etc.

[H] Sol forte reduzindo a legibilidade da tela; poeira, barro e mãos sujas ou com luva; uso com uma das mãos enquanto a outra controla portão ou animal; animal em movimento, o que limita o tempo de enquadramento; conexão de internet instável ou inexistente em parte da propriedade; ruído e pressa durante o manejo, com interrupções constantes.

[F] Em 2024, o serviço de rede móvel celular funcionava em 65,8% dos domicílios rurais (contra 95,3% dos urbanos). Fonte: PNAD Contínua TIC 2024, IBGE. O dado é sobre domicílio, não sobre curral ou pasto, então só indica que a cobertura não é garantida onde o manejo acontece.

## 5.4 Existem fatores sociais ou organizacionais?

Considere papéis, chefias, equipes, permissões, aprovação, responsabilidade profissional, auditoria, turnos e colaboração.

[H] O aparelho pode ser operado pelo vaqueiro, mas a decisão é do produtor ou do gerente da fazenda.

[?] Não sabemos quem faz a captura no manejo do dia a dia: proprietário, gerente, vaqueiro, técnico, ou mais de um perfil dependendo da propriedade. Essa lacuna vai para as próximas investigações e se liga diretamente a H01.

## 5.5 Existe necessidade de histórico, rastreabilidade ou auditoria?

[H] Pode haver necessidade de histórico por animal identificado (brinco) para acompanhar o ganho de peso ao longo do tempo.

[?] Não sabemos se o produtor já acompanha o peso ao longo do tempo hoje, nem se o histórico é uma necessidade real ou só uma possibilidade de solução (H03).

## 5.6 Um erro pode produzir consequência relevante? Qual?

Tudo aqui é hipótese da equipe. A gravidade foi atribuída por nós, não por usuários.

| Erro | Consequência prevista | Quem sente | Gravidade prevista | Status |
|---|---|---|---|---|
| Peso estimado associado ao animal errado | Histórico inconsistente de dois animais. Decisões futuras sobre eles ficam apoiadas em dado errado, e corrigir exige descobrir qual registro está trocado | Produtor; técnico, veterinário e comprador, se receberem o histórico | Alta | [H] |
| Estimativa lida como pesagem exata | Decisão de venda ou de manejo com expectativa errada sobre o peso. Se alguma dose de medicamento for calculada pelo peso, ela também pode sair errada | Produtor e animal | Média a alta, dependendo do uso do número | [H] |
| Captura ruim sem aviso | Um peso estimado menos preciso entra no histórico sem ninguém notar | Produtor | Média | [H] |
| Registro perdido ou duplicado por falha de conexão ou interrupção | Precisar refazer a captura ou ficar sem o dado daquele animal | Produtor ou peão | Baixa a média | [H] |

[?] Não sabemos quais desses erros acontecem de verdade, quais têm impacto relevante e para quem. Isso será investigado nas Entregas 3, 7 e 14.

---

# 6. Entendendo mercado e alternativas existentes

> Nesta entrega faça apenas um **levantamento inicial**. A análise aprofundada ocorre na Entrega 2.

## 6.1 Como pessoas resolvem problemas semelhantes hoje?

| Alternativa atual | Quem usa | Para quê | Status/evidência |
|---|---|---|---|
| Balança de tronco | Fazendas com estrutura para ter ou acessar a balança | Pesagem de todo o lote | [H] Solução padrão, com custo alto |
| Estimativa visual do peão | Produtores e funcionários experientes | Decisão rápida do dia a dia | [H] Sem custo e muito variável |
| Pesagem só na venda | Parte dos produtores | Fechamento comercial | [H] O peso só aparece no fim, então não ajuda a orientar o manejo ao longo do tempo |

## 6.2 Existem produtos que atuam na mesma área, mesmo sem serem equivalentes ao TCC?

[H] Provavelmente existem: softwares de gestão de rebanho, sistemas de pesagem eletrônica integrados a leitores de brinco e soluções comerciais de pecuária de precisão. Ainda não levantamos nomes, e o levantamento detalhado é da Entrega 2.

## 6.3 Quais interfaces profissionais esse público já conhece?

[H] WhatsApp, aplicativos de banco, apps de clima e de cotação da arroba, sistemas de cooperativa e leilão e, em parte do público, softwares de gestão de rebanho.

## 6.4 O que essas soluções parecem fazer bem?

[H] Registro estruturado por animal e por lote, relatórios de evolução do rebanho e integração com equipamentos de pesagem eletrônica.

## 6.5 O que parecem fazer mal, dificultar ou não atender?

[H] Exigem cadastro longo antes de qualquer uso, pressupõem conexão estável, cobram assinatura e ainda dependem de uma balança para obter o peso.

## 6.6 Que padrões de interface ou vocabulário parecem familiares a esse público?

[H] Arroba (@) como unidade de negociação junto com o quilograma, número do brinco, lote, pasto, "ponto de abate", listas simples, botão de câmera e navegação rasa no estilo WhatsApp.

---

# 7. Derivando o escopo de IHC da disciplina

## 7.1 Escolha o caminho do projeto

### Caminho A — TCC já possui interface

Explique qual parte da interface será usada como recorte da disciplina e por que esse fluxo é relevante.

Decisão da equipe: o recorte será o fluxo de captura de foto, identificação do animal e visualização do peso estimado. Ele corresponde principalmente às telas 3 (captura de fotos) e 4 (dashboard/histórico) da interface prevista.

[F] Entre as quatro telas previstas no TCC, nenhuma é dedicada à identificação do animal. Fonte: TCC 1.

Esse fluxo foi escolhido porque junta A01, que é central no fluxo, e A02, que a equipe prevê como a mais crítica.

Decisão da equipe: as telas 1 e 2 (login/cadastro e cadastro do fazendeiro) ficam fora do recorte principal. [H] Elas parecem ser de configuração única e não de uso recorrente, mas podem aparecer simplificadas no protótipo para dar contexto de navegação.

### Caminho B — TCC não possui interface prevista

Não se aplica. O TCC já prevê interface, então seguimos o Caminho A.

## 7.2 Qual perfil será priorizado no projeto de IHC?

Decisão da equipe: priorizar o **pecuarista** (usuário direto).

**Por que esse perfil foi escolhido?**

[H] A equipe supõe que o pecuarista, ou alguém da equipe dele, é quem faz o manejo e carrega o celular no curral ou pasto. O técnico agropecuário seria perfil secundário, porque consulta e orienta, mas provavelmente não é quem fotografa o animal no dia a dia.

Decisão da equipe: tratar "pecuarista" como um papel provisório, que pode juntar proprietário, gerente e vaqueiro, até as próximas entregas descobrirem quem faz a captura em campo.

## 7.3 Qual objetivo desse usuário será priorizado?

Decisão da equipe: priorizar como objetivo obter o peso estimado de um bovino específico de forma rápida, sem balança, com o resultado associado ao animal certo no histórico e com clareza de que é uma estimativa.

[H] A equipe supõe que esse seja um objetivo real do produtor.

[H] Para o usuário, "confiar no resultado" provavelmente envolve entender que é uma estimativa, saber qual a incerteza, saber quando confiar ou não, saber o que fazer se a captura ficou ruim e saber que decisões o número pode ou não apoiar. Isso precisa ser definido com usuários.

## 7.4 Que interface será explorada na disciplina?

Complete:

> **Para fins da disciplina de IHC, será projetada uma interface que permita a `{{perfil}}` utilizar `{{capacidade/resultado do TCC}}` para `{{objetivo}}`, no contexto de `{{situação}}`.**

Decisão da equipe: para fins da disciplina de IHC, será projetada uma interface que permita ao pecuarista utilizar a estimativa de peso do bovino por foto para registrar o peso no animal certo, sem precisar de balança, no contexto de curral ou pasto, usando o smartphone pessoal.

[H] Condições de campo esperadas: sol forte, poeira, mãos sujas e conexão instável.

## 7.5 Qual é a relação dessa interface com o TCC?

- [x] Já fazia parte do TCC.
- [x] É um aprofundamento de algo parcialmente previsto.
- [ ] É uma extensão conceitual criada para a disciplina.
- [ ] É um protótipo demonstrativo de aplicação potencial.
- [ ] Outra.

> **Declaração:** a interface desenvolvida nesta disciplina é um artefato de aprendizagem de IHC baseado no tema do TCC. Sua inclusão ou implementação no TCC somente ocorrerá se isso for posteriormente decidido pela equipe e pelo orientador.

---

# 8. Levantando possibilidades de interação — sem desenhar ainda

A equipe pode registrar possibilidades para investigação. **Não significa que todas serão implementadas.**

Marque apenas as que parecem plausíveis e explique o objetivo correspondente.

| Possibilidade | Pode fazer sentido? | Objetivo/tarefa que justificaria | Evidência atual |
|---|---|---|---|
| Dashboard/visão geral | talvez | Ver os animais ou lotes com o peso estimado mais recente, sem abrir animal por animal | [F] Está previsto como tela 4 no TCC, o que diz o que foi planejado e não que o usuário precisa. [H] A necessidade da visão geral não foi investigada |
| Configuração/parametrização | não, no recorte principal | Cadastro inicial do fazendeiro (quantidade de gado, localização) | [F] Prevista como tela 2 no TCC. Decisão da equipe: fica fora do recorte de IHC |
| Entrada/upload/seleção de dados | sim | Capturar a foto do bovino para gerar o peso estimado | [F] Prevista como tela 3 no TCC (captura de fotos) |
| Acompanhamento de processamento | talvez | Mostrar o status enquanto o modelo processa a foto | [F] Ainda não medimos o tempo de inferência do pipeline, nem no celular nem em servidor (TCC 1) |
| Relatório/resultados | sim | Mostrar o peso estimado (em kg e/ou @) depois da foto, deixando claro que é estimativa e não pesagem | [F] É a saída central do TCC (MAE ~20,75 kg; ~48% dos casos dentro de ±10%). A forma de mostrar a incerteza ainda precisa ser desenhada e avaliada (H02) |
| Histórico com busca/filtros | talvez | Consultar o histórico de peso de um bovino específico, buscando pelo identificador do animal | [F] Previsto como parte da tela 4. [H] Depende de H03 e do vocabulário do público (brinco, lote) |
| Comparação de resultados | talvez | Ver a evolução de peso do animal ao longo do tempo | [H] Supomos que o produtor queira acompanhar a engorda e não só o valor pontual (H03) |
| Explicabilidade/detalhamento | talvez | Não faz sentido explicar a CNN. Pode fazer sentido comunicar a incerteza da estimativa | [H] Supomos que comunicar a incerteza ajude o produtor a entender o resultado. Como fazer isso é questão de design em aberto (H02) |
| Administração/configurações globais | não | Não há indício de necessidade de administração central (várias fazendas, vários operadores por conta) | Decisão da equipe: fora do escopo. Também não foi definido se o app seria 1 produtor = 1 conta |
| Usuários/perfis/permissões | talvez | Diferenciar o acesso do pecuarista (seu rebanho) do acesso do técnico (que poderia acompanhar vários produtores) | [H] Depende de H05, porque não sabemos se o técnico usaria o mesmo app |
| CRUD de entidade do domínio | talvez | Garantir que o peso estimado seja associado ao animal correto | [H] Existem outras formas de associar o peso ao animal, como cadastro prévio, importação, leitura de brinco ou integração com outro sistema. Ainda não comparamos |
| Auditoria/logs | não | Não há indício de necessidade de rastrear quem editou o quê | [H] Pode ganhar relevância se um peso errado gerar disputa com comprador, mas isso não foi investigado |
| Alertas/ocorrências | talvez | Avisar ou orientar quando a captura pode não estar adequada para a estimativa (ângulo, distância, animal em movimento) | [H] Ligado às condições de campo (sol forte, poeira, animal se mexendo) |
| Ajuda/documentação | talvez | Orientar o usuário sobre como tirar a foto (distância, ângulo) | [H] Pode ser útil se a familiaridade digital do público for baixa. Falta confirmar o quanto o modelo depende da qualidade da foto |

> **Atenção:** “login + dashboard + CRUD” não é uma solução universal. Cada padrão deve surgir de uma tarefa real. Nenhuma das possibilidades acima é requisito validado. Cada uma só existe por uma necessidade que ainda é hipótese.

---

# 9. Benefícios e ações iniciais

## 9.1 Qual benefício concreto o projeto de IHC pretende oferecer?

| Benefício esperado | Problema/necessidade | Usuário | Status/evidência |
|---|---|---|---|
| Conseguir estimar o peso dos animais sem comprar ou alugar balança de tronco | [H] A balança é cara e por isso muitos produtores pesam só 2 a 4 vezes por ano | Pecuarista | [F] É a motivação declarada do TCC. [H] Que isso seja um problema relevante para o produtor ainda não foi verificado com produtores |
| Reduzir o risco de associar o peso estimado ao animal errado | [H] Um erro na identificação compromete o histórico daquele animal | Pecuarista | Decisão da equipe: priorizar esse risco. [H] A hipótese de que ele é o mais crítico não foi validada |
| Conseguir usar o app mesmo em condições ruins de campo (sol forte, mãos sujas, sinal instável) | [H] O contexto de uso previsto é curral ou pasto | Pecuarista | [H] Ainda não foi testado com interface real |

## 9.2 Que ações o usuário deverá conseguir realizar?

As prioridades abaixo são decisão inicial da equipe, ainda sem validação.

| ID | O usuário precisa conseguir... | Para alcançar... | Prioridade inicial |
|---|---|---|---|
| F01 | Tirar/enviar uma foto do bovino pelo celular | Receber o peso estimado sem balança | alta |
| F02 | Associar o peso estimado ao animal certo (por brinco, lote ou outra forma a definir) | Garantir que o peso fique no histórico certo | alta |
| F03 | Consultar o histórico de peso de um bovino específico | Acompanhar a evolução do animal ao longo do tempo (depende de H03) | média |
| F04 | Ver uma lista/visão geral dos animais do seu rebanho | Ter noção geral do rebanho sem abrir animal por animal | média |
| F05 | Ter o animal disponível no sistema para receber pesos (por cadastro, importação ou outra forma) | Registrar pesos estimados futuros | média |
| F06 | Entender que o peso mostrado é uma estimativa, não uma pesagem com balança | Decidir com a expectativa certa sobre a margem de erro do modelo | alta |

## 9.3 Tecnologias/restrições já definidas no TCC

A tecnologia aparece **agora**, depois do entendimento do uso.

| Tecnologia/restrição | Por que existe | Possível impacto na interação |
|---|---|---|
| Pipeline: segmentação (YOLO zero-shot), medidas morfométricas e regressão (CNN ResNet18) | [F] É a arquitetura técnica definida e avaliada no TCC 1 | [F] O tempo de inferência em produção ainda não foi medido (TCC 1). Isso define se é preciso uma tela de "processando" |
| Uma foto (single-view) é quase tão boa quanto duas (multi-view) | [F] A diferença é de só 0,04 kg de MAE entre os dois modos | [H] Pode simplificar a captura, pedindo só uma foto. Mas isso não prova que a captura é fácil em campo (H04) |
| Dataset de treino é de bovinos de Bangladesh, ainda não testado em gado brasileiro (Nelore) | [F] Limitação conhecida do TCC 1 | [F] O desempenho em raças brasileiras ainda não foi medido (TCC 1). Ainda não está definido se a interface precisa avisar isso |
| Overfitting identificado na versão multi-view | [F] Resultado técnico do TCC | [H] Reforça a escolha de single-view como fluxo principal |
| MAE ~20,75 kg e acerto dentro de ±10% em ~48% dos casos | [F] Resultado atual do modelo | [H] A interface não deve sugerir que o valor é exato. Como comunicar a incerteza é questão de design em aberto (H02) |

---

# 10. Hipóteses e dúvidas prioritárias

| ID | Hipótese/dúvida | Por que importa | Como poderá ser investigada |
|---|---|---|---|
| H01 | Quem faz a captura em campo (produtor ou peão) consegue usar o app sozinho nas condições de campo (sol forte, poeira, mãos sujas, sinal instável) | Se a interação não funcionar nessas condições, o app não resolve o problema real, mesmo com um modelo preciso | Entrega 3 (persona/contexto), Entrega 7 (coleta de dados) e Entrega 14 (avaliação com usuários) |
| H02 | A forma de mostrar a incerteza da estimativa muda a confiança do produtor no resultado. Mostrar a margem de erro pode aumentar ou diminuir essa confiança, dependendo de como for mostrada | O TCC tem MAE de ~20,75 kg. Se a interface esconder isso, o produtor pode decidir errado. Se comunicar mal, pode desconfiar do app inteiro | Entrega 7 (coleta de dados) e Entrega 13 (avaliação heurística) |
| H03 | O produtor quer acompanhar a evolução do peso do animal ao longo do tempo e não só o último registro de peso | Define se histórico e comparação de evolução continuam no recorte principal | Entregas 2 e 3 (entrevistas com público-alvo/persona) |
| H04 | Uma única foto (single-view) é suficiente para a captura em campo sem gerar frustração por foto rejeitada ou mal enquadrada | O TCC valida single-view tecnicamente (MAE quase igual ao multi-view), mas não valida a facilidade de capturar essa foto em condições reais de curral | Entrega 6 (prototipação em papel) e Entrega 14 (observação de usuários) |
| H05 | O técnico agropecuário usaria o mesmo app que o pecuarista ou precisaria de uma visão/acesso diferente. Também falta saber se ele é usuário secundário ou só stakeholder | Afeta se a seção 8 precisa de "perfis/permissões" no escopo | Entrega 2 (público-alvo) |

Registre em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md).

Lacunas que surgiram na revisão e ainda não têm ID:

- [?] Quem realmente opera o app em campo (proprietário, gerente, vaqueiro, técnico).
- [?] Com que frequência o produtor pesa hoje e com que frequência pesaria com uma solução por foto.
- [?] Como o animal é identificado na prática hoje (brinco, lote, leitura eletrônica, anotação, reconhecimento visual).
- [?] Quais as consequências reais de associar um peso ao animal errado.
- [?] Quais informações o produtor realmente usa para decidir (kg, arroba, ganho desde a última medição, peso de venda ou abate).

---

# 11. Síntese da equipe

| Pergunta | Síntese atual |
|---|---|
| Qual é a contribuição central do TCC? | [F] A capacidade técnica de estimar o peso de bovinos leves (até 250 kg) a partir de fotos, sem balança, com um pipeline de segmentação (YOLO), extração morfométrica e regressão (CNN ResNet18). O aplicativo móvel é a forma prevista de acesso a essa capacidade. Fonte: TCC 1. [H] O valor em uso seria apoiar o acompanhamento e as decisões sobre o peso |
| O TCC já previa interface? | [F] Sim, o app com 4 telas: login/cadastro, cadastro do fazendeiro, captura de fotos e dashboard/histórico. Fonte: TCC 1 |
| Quem é o usuário prioritário de IHC? | Decisão da equipe: o pecuarista. Quem de fato faz a captura em campo continua em aberto |
| O que ele precisa alcançar? | [H] Obter o peso estimado de um bovino específico de forma rápida, sem balança, associado ao animal certo no histórico e entendendo que é uma estimativa |
| Qual problema/atividade será estudado? | Decisão da equipe: o fluxo de fotografar, receber o peso estimado e identificar o animal antes de salvar |
| Como isso acontece hoje? | [H] Com balança de tronco (R$ 30 a 50 mil), e muitos produtores pesariam só 2 a 4 vezes por ano. A frequência real não é conhecida |
| Qual é o contexto de uso? | [H] Curral ou pasto, no smartphone pessoal do produtor ou peão, com sol forte, poeira, mãos sujas, conexão instável e animal em movimento |
| Que interface/recorte será explorado? | Decisão da equipe: as telas 3 (captura de fotos) e 4 (dashboard/histórico) do app previsto, incluindo a identificação do animal |
| Como a interface se relaciona ao TCC? | [F] Já fazia parte do TCC, mas as telas foram definidas de forma superficial, sem trabalho de UX. Por isso a disciplina funciona como aprofundamento. Fonte: TCC 1 |
| Quais pontos ainda são hipóteses? | H01, H02, H03, H04, H05, mais as lacunas listadas na seção 10 |

### Delimitação

**Dentro do escopo de IHC:** decisão da equipe: captura de foto, identificação do animal, exibição do peso estimado deixando claro que é estimativa (forma de mostrar a incerteza a definir) e, sujeitos a confirmação, histórico por animal e visão geral do rebanho.  
**Fora do escopo de IHC:** decisão da equipe: administração multiusuário/permissões, auditoria/logs, cadastro completo do fazendeiro (tela 2) e qualquer detalhamento técnico do modelo (explicabilidade da CNN).  
**Dentro do escopo formal do TCC:** [F] o pipeline de visão computacional e ML (segmentação, extração de medidas, regressão). O app com 4 telas está previsto, mas o foco técnico e científico do TCC é o pipeline. Fonte: TCC 1.  
**Interface da disciplina será implementada no TCC?** Ainda não foi decidido. Depende da equipe e da orientadora.

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

1. **Problema/atividade humana:** [H] Pecuaristas sem balança de tronco (equipamento que custa algo entre R$ 30 mil e R$ 50 mil) tendem a pesar o gado poucas vezes por ano, o que dificulta acompanhar o desenvolvimento dos animais e decidir sobre venda e manejo.
2. **Contribuição técnica do TCC:** [F] O projeto usa visão computacional e aprendizado de máquina (segmentação de imagem, medidas morfométricas e uma rede neural convolucional) para estimar o peso de bovinos leves a partir de uma foto, sem balança, com erro médio de cerca de 20,75 kg nos testes do TCC 1.
3. **Como uma pessoa poderia utilizar essa contribuição:** [H] O produtor poderia fotografar o animal com o próprio celular, no curral ou no pasto, e receber um peso estimado já ligado ao histórico daquele bovino.

Essa síntese ajuda a apresentar o projeto para público não especializado sem reduzir seu mérito técnico.

---

# Checklist de qualidade

- [x] Está clara a diferença entre tema do TCC, escopo formal do TCC e escopo de IHC.
- [x] A equipe declarou se o TCC já previa interface.
- [x] Se não previa, foi derivado um usuário plausível e um objetivo de uso. (Não se aplica: o TCC já previa interface.)
- [x] A interface de IHC não foi apresentada como obrigação automática do TCC.
- [x] A contribuição do TCC foi descrita sem começar por tecnologias de implementação.
- [x] Usuários diretos e stakeholders foram diferenciados.
- [x] Foram considerados profissionais que configuram, administram, interpretam ou decidem, quando pertinente.
- [x] Objetivo do usuário não foi confundido com objetivo do projeto.
- [x] Processo/problema atual foi descrito antes da solução.
- [x] Existe situação concreta de uso/problema.
- [x] Contexto físico, social/organizacional, dispositivos e consequências de erro foram considerados.
- [x] Mercado/alternativas existentes foram levantados inicialmente.
- [x] Possibilidades como dashboard, relatório, histórico, filtros e CRUD foram tratadas como hipóteses de solução, não como requisitos automáticos.
- [x] Cada possibilidade de interface tem um objetivo/tarefa que poderia justificá-la.
- [x] Afirmações relevantes estão marcadas `[F]`, `[H]` ou `[?]`, e os `[F]` têm origem.
- [x] Hipóteses prioritárias receberam IDs e foram para a rastreabilidade.
- [x] O recorte de IHC é viável para modelar, prototipar e avaliar no semestre.
- [x] A equipe consegue explicar problema humano → contribuição computacional → forma de uso.
