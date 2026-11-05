# Entrega 7 — Coleta de dados, necessidades e aspectos éticos

**Data:** 23/20/2026
**Status:** 🟨 em andamento

## Objetivo da atividade

Planejar dados necessários para compreender usuários e requisitos de IHC, escolher técnicas adequadas e documentar instrumentos de modo que a aplicação possa ser reproduzida por pessoas diferentes.

## Para escopos de IHC derivados de TCC técnico

Quando o usuário e a interface foram propostos pela disciplina, uma prioridade da coleta é investigar se esse **cenário de uso realmente faz sentido**. Não trate o exercício de comercialização da Entrega 1 como validação de mercado.

Perguntas úteis incluem:

- esse perfil realmente realiza a atividade imaginada?
- quais ferramentas usa hoje?
- quais informações consulta?
- quais decisões toma?
- que vocabulário utiliza?
- quais parâmetros compreende e quais deveriam ser abstraídos?
- precisa de dashboard, histórico, filtros, relatórios ou comparação? Por quê?
- quais erros são frequentes e quais são críticos?
- existem papéis/permissões diferentes?
- que resultados do algoritmo/modelo seriam úteis ou difíceis de interpretar?

Quando o acesso ao perfil profissional for difícil, discuta com o docente alternativas metodológicas (especialistas próximos, dados secundários, literatura, participantes proxy) e registre as limitações. **Não esconda a limitação da amostra.**

## Hipóteses e lacunas prioritárias herdadas da Entrega 1

Antes de decidir “que dados coletar”, retome os itens `[H]` e `[?]` da Entrega 1 e o registro de hipóteses em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md). A coleta deve responder perguntas reais do projeto, e não apenas produzir um formulário porque a técnica foi solicitada.

| ID | Hipótese/lacuna | Evidência atual | Decisão que depende da resposta | Prioridade |
|---|---|---|---|---|
| H01 | Quem faz a captura (produtor ou peão) consegue usar o app sozinho em campo | PENDENTE | Tamanho dos botões, contraste e modo offline, quem é o usuário principal da captura | alta |
| H02 | A forma de mostrar a incerteza muda a confiança no resultado | PENDENTE | Como exibir a margem de erro e a faixa de peso (Tela 2 da Entrega 6) | alta |
| H03 | O produtor quer acompanhar a evolução do peso, não só o último registro | PENDENTE | Se o histórico por animal (Telas 3 e 4) fica no recorte principal | alta |
| H04 | Uma única foto basta sem frustrar a captura em campo | Parcial: viável tecnicamente (TCC 1), o Beefie orienta o enquadramento (Entrega 2) | Orientação de captura e mensagem de "boi não reconhecido" | média |
| H05 | O técnico usaria o mesmo app que o pecuarista ou precisaria de outro acesso | PENDENTE | Se é preciso ter perfis/permissões ou compartilhamento | média |
| H06 | O modelo treinado com gado de Bangladesh perde precisão em Nelore | Indireta: o Beefie precisou de versão para Nelore (Entrega 2) | Risco técnico do TCC 2 não depende desta coleta | baixa |
| H07 | O público usa arroba, brinco, lote e "ponto de venda" no dia a dia | PENDENTE | Vocabulário das telas (kg e @) | alta |
| H08 | Os animais têm brinco legível ou outra identificação | Indireta: brincos sujos ou caídos no C03 (Entrega 4) | Identificação por brinco ou nome; busca por número ou lote | alta |
## Parte A — necessidades e requisitos de IHC

> **Responsabilidade:** solução individual por integrante.

### A01 — Gustavo 

**Autor(a):** Gustavo Atui — 24.123.072-1

#### Que dados coletar?

| Dado/informação | Hipótese/lacuna relacionada | Por que é necessário | Qual decisão de design pode afetar |
|---|---|---|---|
| Como o técnico descobre hoje o peso dos animais (balança, fita, olho) | H03 | Saber se o app substitui algo que já existe | Fluxo principal e argumento de valor |
| Com que frequência e de que forma acompanha o peso de um mesmo animal | H03 | Confirmar se o histórico por animal é útil | Telas de lote e histórico do animal |
| Como identifica cada animal (brinco, apelido, marca) | H09 | O histórico por animal depende de alguma identificação | Campo de identificação obrigatório ou opcional |
| Como acessa os dados do produtor durante a visita | H05 | O acesso ao histórico depende do produtor | Compartilhamento por link |
| Quem segura o celular e tira a foto na fazenda | H01 | Pode mudar quem é o usuário principal | Personas e fluxo de captura |
| Que termos usa para peso e venda (kg, arroba, "ponto") | H08 | Evitar linguagem técnica ou estranha ao público | Textos das telas |

#### De quem coletar?

| Perfil/stakeholder | Critério de inclusão | Relação com persona/público |
|---|---|---|
| Técnico agropecuário ou zootecnista de campo | Atende pequenos ou médios produtores de gado de corte há pelo menos 1 ano | É a persona P02 (Dinho) |
| Pecuarista de pequeno ou médio porte | Cria gado de corte e vende animais | Persona P01 |

#### Aspectos éticos

- **Dados sensíveis:** informações sobre o tamanho do rebanho, o peso dos animais e o preço de venda podem expor o patrimônio do produtor. Fotos também podem revelar a localização da fazenda.
- **Minimização:** coletar apenas o necessário, sem pedir nome da fazenda, endereço, CPF, número exato de animais ou fotos. O tamanho do rebanho será informado por faixa.
- **Participação voluntária:** deixar claro que participar é opcional e que o técnico pode desistir a qualquer momento, sem consequências.
- **Consentimento:** explicar a pesquisa antes de começar e pedir autorização para gravar o áudio, registrando o consentimento no início da gravação.
- **Anonimização e armazenamento:** identificar cada participante por um código (E1, E2 etc.), retirar nomes das transcrições e guardar os arquivos em uma pasta acessível apenas aos três integrantes do grupo.
- **Descarte:** apagar os áudios após a transcrição e excluir as transcrições ao final da disciplina.


Analise voluntariedade, consentimento, minimização de dados, privacidade, riscos, gravação, anonimização, armazenamento e descarte. Não responda apenas “sim, por causa da LGPD”: explique **quais dados e riscos existem neste projeto**.

> Repita A02, A03...

### A02 — Rafael

**Autor(a):** Rafael Takahagi Mendes — 22.126.084-7

#### Que dados coletar?

Os dados estão agrupados nas cinco categorias da aula: usuário, relação com tecnologia, conhecimento do domínio, tarefas, e motivações e valores.

| Dado/informação | Hipótese/lacuna relacionada | Por que é necessário | Qual decisão de design pode afetar |
|---|---|---|---|
| **Usuário:** papel na fazenda e quem segura o celular no curral (produtor, peão, familiar, técnico) | H01 | Se quem tira a foto não é o dono, o usuário principal da captura pode ser outro | Persona principal e fluxo de captura |
| **Usuário:** faixa de idade (não a idade exata) | Lacuna nova (sem ID) | Ajuda a decidir o quanto a tela precisa ser grande e contrastada | Tamanho de fonte, contraste e botões |
| **Tecnologia:** tipo de celular e apps que usa toda semana | H01 | Confirmar se o estilo WhatsApp é mesmo familiar e para qual sistema prototipar | Padrões de navegação e plataforma do protótipo |
| **Tecnologia:** sinal de internet no curral e no pasto | H01 | O modo offline depende disso | Modo offline e envio das fotos depois |
| **Tecnologia:** facilidade com apps novos e jeito preferido de aprender (sozinho, vídeo, alguém mostra, passo a passo) | Lacuna nova (sem ID) | Calibrar a complexidade e a ajuda dentro do app | Número de passos, tutorial e textos de ajuda |
| **Domínio:** medida usada para falar de peso e termos do dia a dia (kg, arroba, brinco, lote, ponto de venda) | H07 | Evitar palavra estranha ao produtor | Textos das telas (kg e @) |
| **Domínio:** preferência entre número único e faixa de peso, e quanto erro aceitaria para decidir a venda | H02 | Define como o produtor entende e confia em um peso estimado | Como exibir margem de erro e faixa (Tela 2 da Entrega 6) |
| **Tarefas:** como pesa hoje, quantas vezes por ano e onde anota | H03 | Confirmar que a tarefa existe e o que o app substituiria | Fluxo principal e argumento de valor |
| **Tarefas:** se compara com pesagens anteriores e o que gostaria de ver no histórico | H03 | Confirmar se histórico por animal é útil ou se o último peso basta | Se o histórico (Telas 3 e 4) fica no recorte principal |
| **Tarefas:** como identifica cada animal e se o brinco está legível no dia do manejo | H08 | Identificar o animal antes de salvar é a atividade mais crítica (A02 do projeto) | Identificação por brinco ou por nome; busca por número ou lote |
| **Tarefas:** erros já ocorridos ao anotar peso (animal trocado, anotação perdida) e a consequência | H08 | Mostra a gravidade do erro de identificação | Confirmação antes de salvar |
| **Tarefas:** quantas fotos por animal tolera durante o manejo | H04 | Verificar se uma foto basta sem atrapalhar o serviço | Orientação de captura e número de fotos pedidas |
| **Motivações e valores:** reação à ideia de pesar por foto (fácil, confiável, útil) e o que faria a pessoa não usar | H02 | Testa se o cenário faz sentido para esse público e se existe desconfiança | Mensagens de confiança e forma de apresentar a incerteza |

#### De quem coletar?

| Perfil/stakeholder | Critério de inclusão | Relação com persona/público |
|---|---|---|
| Pecuarista de pequeno ou médio porte | Cria gado de corte (cria, recria ou engorda), vende animais e tem 18 anos ou mais | É a persona P01 (Chico Bento), usuário direto e principal |
| Gerente, familiar ou peão que participa do manejo | Trabalha em fazenda de gado de corte e tem 18 anos ou mais | Possível pessoa que tira a foto no curral (H01). Grupo secundário, identificado pela pergunta P2 |

O técnico agropecuário é coberto pela entrevista do Gustavo (A01 e I01). Frigorífico, comprador e veterinário só recebem o histórico de peso e não usam a interface, por isso ficam fora da coleta.

[?] Ainda não temos pecuaristas confirmados para responder. A amostra será por conveniência, a partir de contatos da equipe e de indicações deles, e não representa o setor. [H] Quem responde formulário online costuma ter mais intimidade com celular do que o produtor médio, então os dados podem subestimar a dificuldade de uso. Por isso o questionário mede celular, sinal e facilidade com apps (P5 a P9), e os resultados serão lidos como indício, cruzados com a entrevista com técnicos.

#### Aspectos éticos

Sim, o projeto precisa considerar aspectos éticos. Mesmo sem pedir nome, o questionário envolve pessoas e o patrimônio delas (rebanho e pesagens), e seguimos os princípios da Resolução 196/96 vistos em aula.

- **Dados sensíveis e privacidade:** tamanho do rebanho e frequência de pesagem dizem muito sobre o patrimônio do produtor. [H] Parte dos produtores pode ter receio de que essas informações cheguem a comprador ou fiscalização. As perguntas abertas também podem trazer, sem querer, nome de pessoa, fazenda ou cidade.
- **Minimização:** não pedimos nome, telefone, e-mail, nome da fazenda, cidade, CPF, preço de venda nem fotos. Rebanho e idade são informados por faixa, com a opção "prefiro não dizer". A coleta automática de e-mail do Google Forms fica desligada.
- **Voluntariedade:** o convite e o termo deixam claro que participar é opcional e que dá para parar a qualquer momento, é só fechar a página. Nada é enviado antes de clicar em Enviar. Como a resposta é anônima, depois de enviada não conseguimos achar a resposta de alguém para apagar, e isso está escrito no termo.
- **Consentimento:** o termo é a primeira seção do formulário, em linguagem simples, com uma opção obrigatória "Tenho 18 anos ou mais e aceito participar". Quem não aceita vai direto para o agradecimento e não vê as perguntas. O aceite no formulário é o registro do consentimento.
- **Grupos vulneráveis:** a aula cita subordinados como grupo que precisa de proteção. [H] Um peão ou funcionário pode se sentir pressionado a responder se o patrão pedir. O convite é enviado individualmente, o termo diz que ninguém da fazenda vê as respostas, e só participam maiores de 18 anos.
- **Riscos e benefícios:** o risco é baixo: cansaço, constrangimento com alguma pergunta ou exposição acidental de dado do rebanho. Não há benefício direto ao participante. O benefício é coletivo, ajudar a projetar um app que pode facilitar a pesagem para quem não tem balança.
- **Gravação:** não há gravação de áudio, imagem ou localização. Só texto digitado ou marcado no formulário.
- **Anonimização e armazenamento:** as respostas ficam no Google Forms e em uma planilha exportada para uma pasta acessível só aos três integrantes do grupo. Antes da análise, as respostas abertas são revisadas e qualquer nome, fazenda ou cidade é apagado. No relatório, as citações aparecem como R1, R2 etc. A lista de quem recebeu o convite não é cruzada com as respostas.
- **Descarte:** ao final da disciplina, o formulário e as planilhas com respostas brutas são apagados. Ficam apenas as tabelas agregadas (percentuais) e as citações anonimizadas do relatório.

Resumindo nos princípios da Resolução 196/96: não maleficência (minimização, anonimização e descarte), justiça e equidade (convite igual para todos, sem exigir nada de quem não quer participar), autonomia (voluntariedade, consentimento e cuidado com subordinados) e beneficência (risco baixo e benefício coletivo).

## Parte B — ferramentas de coleta

> Cada integrante deve preparar uma técnica/instrumento completo. As técnicas devem ser diferentes entre si e **questionário deve estar entre as técnicas escolhidas**, conforme o enunciado da disciplina.

### Instrumento I01 — Entrevista semiestruturada

**Autor(a):** Gustavo Atui - 24.123.072-1 
**Técnica:** entrevista semiestruturada  
**Objetivo:** entender como o técnico acompanha o peso dos animais e decide a recomendação de venda.  
**Público:** técnicos agropecuários

#### Procedimento padronizado de aplicação

1. **Preparação:** agendar uma reunião 30 minutos,levar roteiro para entrevista. 
2. **Consentimento:** ler o termo e pedir autorização para gravar.
3. **Aplicação:** seguir o roteiro sem sugerir respostas.
4. **Encerramento:** agradecer e perguntar se quer acrescentar algo.
5. **Anonimização:** transcrever com códigos (E1, E2). 

#### Instrumento

Cole aqui o questionário/roteiro completo ou forneça link **mais uma cópia textual no repositório**.

**Termo:** "Sou um aluno de IHC da FEI. Deixei reservado 30 minutos para entrevista, você pode parar quando quiser e não registraremos seu nome. Podemos gravar o a entrevista ?"

 **Roteiro:**
 
1. Há quanto tempo trabalha como técnico de campo?
2. Como você descobre hoje o peso de um animal?
3. Como os animais são identificados na fazenda?
4. Quem segura o celular ou anota durante a visita?
5. Que informações você usa para recomendar a venda?
6. Você compara o peso atual com pesagens anteriores? Como?
7. Onde ficam os registros de peso e como você os acessa?
8. Como você e o produtor falam o peso no dia a dia?

#### Como os dados serão analisados

{{ex.: distribuição de respostas, codificação temática, agrupamento de problemas}}

Respostas agrupadas por hipótese (H01, H03, H05, H08, H09), indicando se cada uma foi sustentada, refutada ou refinada na RASTREABILIDADE.md.

### Instrumento I02 — Questionário online (Google Forms)

**Autor(a):** Rafael Takahagi Mendes — {{RA}}  
**Técnica:** questionário online autoaplicado  
**Objetivo:** verificar com pecuaristas se o cenário de uso faz sentido (se pesam, como pesam, como identificam os animais e quem usa o celular no curral) e levantar vocabulário, condição de internet e reação à ideia de pesar por foto.  
**Público:** pecuaristas de pequeno e médio porte (P01). Gerentes, familiares ou peões que participam do manejo também podem responder.  
**Meta de amostra:** pelo menos 15 respostas válidas, sem pretensão estatística.  
**Link do formulário:** {{link do Google Forms}}

#### Procedimento padronizado de aplicação

1. **Preparação:** criar o formulário com o conteúdo abaixo. Desligar a coleta de e-mail, não exigir login e deixar todas as perguntas obrigatórias, menos as abertas. Se a resposta da P1 for "Não", ir direto para o agradecimento. Testar com 2 pessoas de fora do grupo, corrigir o que estiver confuso e conferir o tempo de resposta. As respostas do teste não entram na análise. Definir a janela de coleta: {{data de início}} a {{data de fim}}.
2. **Divulgação:** enviar o link por mensagem individual, com o mesmo texto de convite para todos.
3. **Consentimento:** o termo é a primeira seção do formulário. Sem marcar o aceite, a pessoa não avança.
4. **Aplicação:** a pessoa responde sozinha no celular. Se tiver dificuldade para ler ou usar o formulário, quem aplica lê as perguntas em voz alta, sem explicar nem sugerir respostas, e marca o que a pessoa disser. O termo também é lido em voz alta nesse caso.
5. **Encerramento:** tela de agradecimento com o contato do grupo.
6. **Anonimização:** ao fim da janela, exportar para planilha na pasta do grupo, apagar nomes, fazenda e cidade das respostas abertas e identificar cada resposta como R1, R2 etc.

#### Instrumento

**Mensagem de convite:** "Oi! Sou aluno de Ciência da Computação da FEI e estou fazendo uma pesquisa rápida, de uns 10 minutos, sobre como o pecuarista pesa e acompanha o gado. É anônima e só participa quem quiser. Se puder ajudar, o link é este: {{link}}. Obrigado!"

**Termo (seção 1 do formulário):** "Somos alunos de Ciência da Computação da FEI e estamos estudando como seria um aplicativo que estima o peso do boi por foto, sem balança. Esta pesquisa serve só para entender como o pecuarista trabalha hoje. Leva uns 10 minutos. Não pedimos nome, telefone, e-mail, nome da fazenda nem cidade. Ninguém da sua fazenda vê suas respostas. Elas são anônimas, ficam guardadas só com os três alunos do grupo, são usadas apenas no trabalho da disciplina e serão apagadas no fim do semestre. Participar é voluntário. Você pode parar quando quiser, é só fechar a página, e nada é enviado antes de clicar em Enviar. Como as respostas são anônimas, depois de enviar não conseguimos achar a sua para apagar. Dúvidas: tcc.gado.cc@gmail.com."

- ( ) Sim, tenho 18 anos ou mais e aceito participar
- ( ) Não quero participar *(vai para o agradecimento)*

**Bloco 1 — Sobre você e sua criação**

- **P1.** Você cria gado de corte (cria, recria ou engorda)? *(escolha única)* Sim / Não *(Não: vai para o agradecimento)*
- **P2.** Qual é o seu papel na fazenda? *(escolha única)* Dono ou produtor / Gerente ou administrador / Familiar que ajuda no manejo / Peão ou funcionário / Outro: ___
- **P3.** Mais ou menos quantos animais a fazenda tem hoje? *(faixa de valores)* Até 50 / 51 a 200 / 201 a 500 / Mais de 500 / Prefiro não dizer
- **P4.** Qual é a sua faixa de idade? *(faixa de valores)* 18 a 29 / 30 a 44 / 45 a 59 / 60 ou mais / Prefiro não dizer

**Bloco 2 — Celular e internet**

- **P5.** Que tipo de celular você usa? *(escolha única)* Android / iPhone / Celular que não acessa internet / Outro
- **P6.** Como é o sinal de internet onde você faz o manejo (curral ou pasto)? *(escolha única)* Quase sempre tem sinal / Tem sinal só em alguns pontos / Não tem sinal, só pega na sede / Não sei
- **P7.** Quais destes aplicativos você usa pelo menos uma vez por semana? *(marque todos)* WhatsApp / YouTube / Facebook ou Instagram / App do banco / App de clima / Google Maps / App de gestão da fazenda ou do rebanho / Nenhum desses / Outro: ___
- **P8.** "Quando aparece um aplicativo novo, eu consigo aprender a usar sem ajuda." *(escala de Likert)* 1 = Discordo totalmente, 2, 3, 4, 5 = Concordo totalmente
- **P9.** Como você prefere aprender a usar um aplicativo novo? *(escolha única)* Mexendo sozinho / Vendo um vídeo curto / Alguém me mostra / Lendo um passo a passo / Não costumo usar aplicativo novo

**Bloco 3 — Peso dos animais**

- **P10.** Hoje, como você fica sabendo o peso dos seus animais? *(marque todos)* Balança de tronco própria / Balança de outra pessoa ou empresa (emprestada ou alugada) / Fita de pesagem / Estimo no olho / Só sei o peso na venda (frigorífico ou comprador) / Não costumo pesar / Outro: ___
- **P11.** Quantas vezes por ano você pesa os animais? *(faixa de valores)* Nenhuma / 1 vez / 2 a 4 vezes / 5 a 11 vezes / 1 vez por mês ou mais
- **P12.** Onde você anota o peso? *(marque todos)* Caderno ou agenda / Planilha / Aplicativo / WhatsApp / Só guardo de cabeça / Não anoto / Outro: ___
- **P13.** Com que frequência você compara o peso atual de um animal com pesagens anteriores dele? *(escolha única)* Nunca / Raramente / Às vezes / Quase sempre / Sempre / Não tenho pesagens anteriores
- **P14.** Se você tivesse esse registro no celular, o que mais gostaria de ver? *(escolha única)* O peso de cada animal ao longo dos meses / A média do lote / Só o último peso de cada animal / Não preciso ver isso / Outro: ___

**Bloco 4 — Como você fala de peso**

- **P15.** Quando você fala do peso de um boi com alguém (vizinho, comprador, técnico), qual medida usa? *(escolha única)* Quilo (kg) / Arroba (@) / Depende de com quem estou falando / Outro: ___
- **P16.** Quais destes termos você usa no dia a dia? *(marque todos)* Arroba / Brinco / Lote / Ponto de venda (ou "ponto") / Ganho de peso / Rendimento de carcaça / Nenhum desses

**Bloco 5 — Identificação dos animais**

- **P17.** Como você identifica cada animal? *(marque todos)* Brinco numerado / Nome ou apelido / Marca a fogo ou tatuagem / Pelo aspecto (cor, chifre, tamanho) / Só por lote, não individualmente / Outro: ___
- **P18.** No dia do manejo, quantos animais estão com o brinco legível? *(escolha única)* Todos / A maioria / Cerca de metade / Poucos / Nenhum / Não uso brinco
- **P19.** Já aconteceu de anotar o peso no animal errado ou de perder a anotação? *(escolha única)* Nunca / Uma vez / Algumas vezes / Com frequência
- **P20.** *(só aparece para quem respondeu "Uma vez", "Algumas vezes" ou "Com frequência" na P19; opcional)* O que aconteceu e qual foi a consequência? *(pergunta aberta)* Aviso na pergunta: "Não escreva nomes de pessoas, fazenda ou cidade."

**Bloco 6 — Manejo no curral**

- **P21.** Quem normalmente segura o celular ou faz as anotações durante o manejo? *(marque todos)* Eu mesmo / Peão ou funcionário / Familiar / Técnico ou veterinário / Ninguém usa celular no curral / Outro: ___
- **P22.** Se um aplicativo pedisse fotos do animal para estimar o peso, quantas fotos por animal você acharia aceitável durante o manejo? *(escolha única)* 1 foto / 2 fotos / 3 ou mais fotos / Nenhuma, prefiro outro jeito de pesar

**Bloco 7 — Peso estimado por foto**

Texto de abertura: "As próximas perguntas são sobre uma ideia: um aplicativo que estima o peso do boi a partir de fotos tiradas com o celular, sem balança. O peso estimado pode errar um pouco, para mais ou para menos."

- **P23.** Como você preferiria ver o peso estimado? *(escolha única)* Só um número (ex.: 420 kg) / Uma faixa (ex.: 400 a 440 kg) / Número e faixa juntos / Tanto faz
- **P24.** Para decidir a hora de vender, até quanto de erro por animal você aceitaria? *(faixa de valores)* Até 5 kg / Até 10 kg / Até 20 kg / Mais de 20 kg / Nenhum, só confio em balança / Não sei
- **P25.** Pesar o gado por foto no celular me parece: *(escala de diferenciais semânticos, de 1 a 5 em cada linha)* Difícil (1) a Fácil (5) / Pouco confiável (1) a Muito confiável (5) / Pouco útil (1) a Muito útil (5)
- **P26.** Tem algo que faria você não usar um aplicativo assim? *(pergunta aberta, opcional)* Aviso na pergunta: "Não escreva nomes de pessoas, fazenda ou cidade."

#### Como os dados serão analisados

- **Tabulação:** contagem e percentual por alternativa em cada pergunta. Nas de "marque todos", percentual de pessoas que marcou cada item.
- **Cruzamentos simples:** papel × quem segura o celular (P2 × P21), sinal × tipo de celular (P6 × P5) e tamanho do rebanho × frequência de pesagem (P3 × P11).
- **Perguntas abertas (P20 e P26):** leitura de todas as respostas, criação de rótulos por tema, agrupamento e contagem de quantas respostas caem em cada tema.
- **Uso nas hipóteses:** respostas agrupadas por hipótese, com o critério abaixo. Definimos que a hipótese fica **sustentada** quando mais da metade das respostas válidas vai na direção dela, **refutada** quando menos de um quarto vai, e **refinada** quando fica no meio ou muda conforme o subgrupo.

| Hipótese | Perguntas | Sustentada se... |
|---|---|---|
| H01 | P2, P5, P6, P8, P21 | a maioria usa smartphone, dá nota 4 ou 5 na P8 e alguém usa celular no curral. Sinal ruim na P6 refina a hipótese (modo offline). |
| H02 | P23, P24, P25 | a maioria prefere uma forma de ver o peso e não responde "tanto faz". O questionário só mostra preferência declarada. O efeito real na confiança fica para a avaliação com protótipo. |
| H03 | P10 a P14 | mais da metade compara com pesagens anteriores "às vezes" ou mais e escolhe o histórico por animal na P14. |
| H04 | P22 | a maioria aceita pelo menos 1 foto por animal e não escolhe "nenhuma". A frustração real em campo fica para a avaliação por observação. |
| H07 | P15, P16 | a maioria usa arroba e termos como brinco e lote. Muita resposta "depende" na P15 refina a hipótese (mostrar kg e @). |
| H08 | P17 a P20 | a maioria tem brinco legível. Se a maioria responde "poucos", "nenhum" ou "não uso brinco", a hipótese é refutada e a identificação precisa de alternativa (nome ou lote). |

As hipóteses H05 e H06 não são cobertas por este instrumento. A H05 (técnico) fica com a entrevista do Gustavo, e a H06 é risco técnico do TCC 2. Quando os dados forem analisados, atualizar o histórico no `RASTREABILIDADE.md`.

## Síntese

Explique quais lacunas de conhecimento sobre usuários o conjunto de técnicas pretende reduzir. Indique explicitamente quais hipóteses da Entrega 1 deverão ficar **sustentadas, refutadas ou refinadas** após a análise dos dados. Quando os dados forem coletados/analisados, atualize o histórico em `RASTREABILIDADE.md`.

**Parte do Gustavo (A01 e I01):** a entrevista com técnicos busca confirmar se eles realmente acompanham a evolução do peso de cada animal (H03), como acessam os dados do produtor (H05), quem opera o celular na fazenda (H01), que vocabulário usam (H08) e como os animais são identificados (H09). Ao fim da análise, cada uma dessas hipóteses deve ficar sustentada, refutada ou refinada na RASTREABILIDADE.md.

**Parte do Rafael (A02 e I02):** o questionário com pecuaristas olha as mesmas lacunas do lado de quem vai usar o app e complementa a entrevista com técnicos. Ele busca confirmar se o produtor realmente pesa e acompanha o peso de cada animal (H03), quem segura o celular e se tem sinal e facilidade para usar sozinho (H01), se uma foto por animal é tolerável no manejo (H04), como prefere ver a incerteza do peso (H02, apenas como preferência declarada), que vocabulário usa (H07) e como identifica os animais (H08). Ao fim da análise, cada uma dessas hipóteses deve ficar sustentada, refutada ou refinada na RASTREABILIDADE.md. A amostra é pequena, por conveniência e com viés para quem responde online, então os resultados são indícios e não um retrato do setor.

## Checklist

- [ ] Hipóteses/lacunas prioritárias da Entrega 1 foram revisitadas.
- [ ] Se o escopo de IHC foi derivado de TCC técnico, a coleta investiga a plausibilidade do usuário, tarefa e contexto adotados.
- [ ] Perguntas não pressupõem que dashboard, CRUD, filtros ou relatórios sejam necessários; investigam a necessidade.
- [ ] Cada dado a coletar responde uma dúvida concreta do projeto ou justifica outra necessidade de informação.
- [ ] Parte A identifica dados e perfis de coleta de forma específica.
- [ ] Aspectos éticos são contextualizados para o projeto.
- [ ] Há uma técnica completa por integrante e técnicas distintas.
- [ ] Questionário está incluído entre as técnicas.
- [ ] Cada instrumento possui objetivo, público, procedimento e conteúdo integral.
- [ ] Perguntas evitam indução e coletam apenas dados necessários.
- [ ] Está claro como os dados serão analisados e usados no design.
