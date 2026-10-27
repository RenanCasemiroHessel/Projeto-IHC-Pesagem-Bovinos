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

## Parte B — ferramentas de coleta

> Cada integrante deve preparar uma técnica/instrumento completo. As técnicas devem ser diferentes entre si e **questionário deve estar entre as técnicas escolhidas**, conforme o enunciado da disciplina.

### Instrumento I01 — {{nome da técnica}}

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

## Síntese

Explique quais lacunas de conhecimento sobre usuários o conjunto de técnicas pretende reduzir. Indique explicitamente quais hipóteses da Entrega 1 deverão ficar **sustentadas, refutadas ou refinadas** após a análise dos dados. Quando os dados forem coletados/analisados, atualize o histórico em `RASTREABILIDADE.md`.

**Parte do Gustavo (A01 e I01):** a entrevista com técnicos busca confirmar se eles realmente acompanham a evolução do peso de cada animal (H03), como acessam os dados do produtor (H05), quem opera o celular na fazenda (H01), que vocabulário usam (H08) e como os animais são identificados (H09). Ao fim da análise, cada uma dessas hipóteses deve ficar sustentada, refutada ou refinada na RASTREABILIDADE.md.

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
