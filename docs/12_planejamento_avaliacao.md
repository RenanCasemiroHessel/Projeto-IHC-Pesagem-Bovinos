# Entrega 12 — Planejamento da avaliação de usabilidade (DECIDE)

**Data:** 14/11/2026  
**Status:** 🟨 em andamento
**Responsabilidade:** 1 solução por equipe

## Objetivo da atividade

Planejar a avaliação antes de executá-la, ligando perguntas de avaliação a métodos, participantes, tarefas, métricas, aspectos práticos, ética e forma de análise.

## O que está sendo avaliado

[F] A avaliação investiga **a qualidade da interação com o protótipo do Figma** (Entrega 11). Ela **não** avalia se o peso estimado está certo. O desempenho do modelo é avaliado no TCC (erro médio de ~20,75 kg e ~48% das estimativas dentro de ±10%, TCC 1).

**Versão avaliada:** protótipo do Figma da Entrega 11, com 19 telas e 4 fluxos de partida (https://www.figma.com/proto/vvwn3MeDQGGoP3d3y5GCwB). Registrar a data da versão no dia do piloto.

**O que é simulado no protótipo e precisa ser declarado ao participante:**

| Simulado | Como aparece | Consequência para a avaliação |
|---|---|---|
| Estimativa do peso | O peso é sempre o mesmo (o exemplo da Entrega 11: 214 kg), com a margem de ± 20 kg. "Calculando o peso…" (F01L) só simula a espera | Não se mede se o peso está certo, só se a pessoa entende e usa o resultado |
| Foto | A foto já vem escolhida (F01B) ou é uma foto sem bovino (F01C) | A captura real no curral não é testada (limitação de MQ05) |
| Animais, lotes e histórico | Dados fictícios: boi 117, lote Pasto 2, lista do lote com "Pintado", "Malhado" e "Mocho", pesagens anteriores | As tarefas usam esses dados, para todos os participantes iguais |
| Digitação do brinco | [?] No Figma, tocar no campo pode preencher o número sozinho (F02 → F02P). Confirmar no piloto | Se não dá para digitar, um erro de digitação não acontece naturalmente. A identificação errada é observada na tela de conferência (F02C) |

**O que fica fora da avaliação com usuários:** fechar a pesagem do lote (T03), envio sem sinal (offline) e cadastro de animal novo (F02X, provisória desde a Entrega 10). Nenhum deles está prototipado de forma completa. A F02X e as demais telas entram só na inspeção heurística (Entrega 13).

## A. Método DECIDE

| Etapa | Aplicação no projeto |
|---|---|
| **D — Determine the goals** | Verificar se o protótipo atinge as metas da Entrega 8 nos dois fluxos principais. No fluxo **estimar e salvar** (T02, M01, F01–F02S): eficácia MU01, erro de identificação MU02, recuperação MU04, compreensão da margem de erro MU05 e MQ01, e tempo MU06. No fluxo **consultar o histórico** (T01,M02, F03–F04): MU03 e MU07. Em todas as tarefas: satisfação MU08. Também encontrar problemas que impeçam ou atrasem as tarefas antes do TCC 2. |
| **E — Explore the questions** | O produtor consegue pesar um boi e guardar o peso no animal certo sem ajuda? Percebe em qual animal o peso vai ficar antes de salvar? Entende que o peso é aproximado? Sabe o que fazer quando o boi não é reconhecido ou o brinco está ilegível? Acha quanto um animal engordou sem fazer contas? As perguntas detalhadas estão na seção B. |
| **C — Choose the evaluation paradigm and techniques** | Duas técnicas que se completam. **(1) Inspeção heurística** com as 10 heurísticas de Nielsen (Entrega 13), feita pelos 3 integrantes sobre as 19 telas. É barata, cobre todas as telas, inclusive as que não entram nas tarefas (F02X, F03V, F05D), e não depende de recrutamento. **(2) Teste de usabilidade com observação** (Entrega 14), com 3 participantes representativos e *think aloud*, para medir sucesso, tempo, erros e compreensão, o que a inspeção não mede. Paradigma: avaliação formativa (achar problemas para corrigir), não somativa. |
| **I — Identify the practical issues** | 3 participantes, um por integrante (seção C). Sessão de ~25 min, presencial ou por vídeo, com o protótipo aberto **no celular** (link do Figma no navegador ou no app Figma), para ficar mais perto do uso real. Cada tarefa começa no fluxo de partida certo do Figma (seção D). Piloto com um colega de outra equipe antes das sessões. Riscos: não achar pecuarista ou técnico (usar participante proxy e registrar), internet do participante cair (levar um celular de reserva com o protótipo aberto) e link do Figma pedir permissão (testar em janela anônima no dia). |
| **D — Decide how to deal with ethical issues** | Termo de consentimento lido antes de começar, com autorização separada para gravar tela e áudio. Participação voluntária, com direito de parar a qualquer momento. Participantes viram U01, U02, U03. Não coletamos nome da fazenda, endereço, número exato de cabeças nem fotos do participante (mesmos cuidados da Entrega 7). Gravações guardadas na pasta restrita aos 3 integrantes e apagadas no fim da disciplina. Deixar claro que o produto é que está sendo avaliado, não a pessoa, e que o peso mostrado é simulado. |
| **E — Evaluate, interpret and present the data** | Cada integrante preenche a planilha de observação da sua sessão. A equipe junta os dados numa tabela por tarefa (sucesso, tempo, erros, ajudas, nota) e compara com cada meta (atingida / não atingida). Falas e problemas são agrupados por tela e por heurística, com severidade de 0 a 4 (seção F). Os problemas da Entrega 13 e da Entrega 14 são cruzados: problema que aparece nos dois sobe de prioridade. O resultado vira a lista de melhorias na RASTREABILIDADE.md (colunas "Heurística/problema", "Tarefa no teste" e "Decisão/melhoria"). |

## B. Perguntas de avaliação

| ID | Pergunta | Método | Métrica/evidência | Critério esperado |
|---|---|---|---|---|
| QA01 | O participante consegue estimar o peso de um boi e salvar no animal certo sem ajuda? | observação (UT01) | sucesso total/parcial/falha, pedidos de ajuda | MU01: ≥ 80% (com 3 participantes, 3 de 3) |
| QA02 | Antes de salvar, o participante confere em qual animal o peso vai ficar e percebe quando não é o animal da tarefa? | observação (UT01 e UT03, tela F02C) | lê ou fala o brinco na F02C; usa "Não é esse" quando o animal não bate; peso salvo no animal errado | MU02: 0 casos de peso salvo no animal errado sem perceber; MQ02 |
| QA03 | O participante entende que o peso é uma estimativa com margem de erro? | pergunta pós-tarefa (depois da UT01) | explicação com as próprias palavras, anotada | MU05: ≥ 80% (3 de 3) explicam que o peso é aproximado; MQ01 |
| QA04 | Quando o boi não é reconhecido, o participante entende o que aconteceu e tira outra foto sem tentar salvar? | observação (UT02) | volta para a foto sem ajuda; não procura salvar | MU04: ≥ 80% (3 de 3); MQ03 |
| QA05 | Com o brinco ilegível, o participante encontra o animal pelo lote? | observação (UT03) | chega à conferência com o animal pedido, sem ajuda | Sucesso sem ajuda em 3 de 3. [H] Não tem meta na Entrega 8; vem da HTA 3 e do GOMS 3.B (Entrega 5) |
| QA06 | O participante encontra quanto um animal engordou sem fazer contas? | observação (UT04) | sucesso; valor do ganho dito corretamente | MU03: ≥ 80% (3 de 3); MQ04 |
| QA07 | Quanto tempo as tarefas principais levam? | observação com cronômetro (UT01 e UT04) | tempo mediano | MU06: ≤ 60 s (UT01); MU07: ≤ 30 s (UT04) |
| QA08 | As tarefas parecem fáceis para o participante? | questionário pós-tarefa | nota de 1 a 5 em "Foi fácil fazer isso?" e comentário | MU08: média ≥ 4 |
| QA09 | O app sempre mostra o que está acontecendo e como sair de um erro? | heurística (Entrega 13) | violações de H1 (status) e H9 (recuperação de erros) nas 19 telas | Nenhuma violação de severidade 3 ou 4 em F01L, F02E, F02A, F02N, F02S e F05D |
| QA10 | Os termos e signos são os do produtor e são usados sempre do mesmo jeito? | heurística (Entrega 13) + falas no teste | violações de H2 e H4 (ex.: "boi" e "bovino" misturados, @); dúvidas sobre palavras durante o teste | Nenhuma violação de severidade 3 ou 4; nenhuma tarefa travada por não entender uma palavra (MQ04) |
| QA11 | Dá para operar as telas principais com uma mão? | observação no celular | toques errados repetidos; troca para as duas mãos | MQ05. [?] O Figma não reproduz sol, poeira e mão suja: o resultado é parcial e a heurística reforça (contraste, tamanho de toque) |

## C. Escopo e participantes

| Item | Planejamento |
|---|---|
| Perfis | Um participante por persona: **U01** pecuarista ou quem decide a venda (P01 Chico); **U02** técnico agropecuário, zootecnista ou veterinário de campo (P02 Dinho); **U03** peão ou funcionário que maneja o gado (P03 Agnaldo) |
| Critérios de inclusão/exclusão | Inclusão: lidar com gado de corte (manejo, pesagem ou orientação técnica) e usar smartphone. Exclusão: integrantes da equipe e quem já viu o protótipo (inclusive quem participou do piloto ou da simulação da Entrega 6). Se não houver pessoa com o perfil, aceitar **participante proxy** (estudante de agronomia, zootecnia ou veterinária com experiência de manejo) e marcar como proxy na análise |
| Nº de participantes | 3, igual ao número de integrantes (regra da Entrega 14). Cada integrante recruta, conduz e analisa uma sessão: **Rafael → U01**, **Gustavo → U02**, **Renan → U03** [H] (trocar se o recrutamento facilitar outra divisão) |
| Ambiente | Presencial ou remoto por videochamada, num lugar calmo. [H] Presencial, se possível, para ver a mão no celular (QA11) |
| Dispositivo | Smartphone do participante (ou um da equipe) com o protótipo aberto pelo link do Figma. No remoto, o participante compartilha a tela do celular |
| Protótipo/versão | Figma da Entrega 11, 19 telas, fluxos de partida: 1. Principal: pesar e salvar; 2. Erro: boi não reconhecido; 3. Erro: nenhum bovino encontrado; 4. Primeiro uso: histórico vazio |
| Teste piloto | Com um colega de outra equipe, **antes da primeira sessão**. Validar: duração (~25 min), se as instruções das tarefas são entendidas sem dar a resposta, se cada fluxo de partida abre na tela certa, se o link abre sem pedir permissão, a gravação e as duas dúvidas do protótipo (digitação do brinco e o que acontece ao escolher "Pintado" na F02L). O piloto não entra na amostra |

**Limitação da amostra:** 3 pessoas, por conveniência, possivelmente proxy. Os resultados servem para achar problemas, não para generalizar. Com 3 participantes, a meta "≥ 80%" só é atingida com 3 de 3, então os resultados serão apresentados como contagem (ex.: "2 de 3"), não como porcentagem.

## D. Lista de tarefas de avaliação

As instruções descrevem o objetivo da pessoa, sem dizer onde tocar e sem usar o rótulo dos botões testados. O brinco, o lote e o nome do animal são dados da situação, não nomes de controles.

| ID | Cenário neutro entregue ao usuário | Objetivo oculto da avaliação | Critério de sucesso | Tempo-limite (se houver) |
|---|---|---|---|---|
| UT01 | "Você está no curral. Na sua frente está um boi macho, o de brinco 117, que fica no Pasto 2. Você quer saber quanto ele pesa e deixar esse peso guardado no registro dele." *(começa no fluxo 1, F01)* | T02 / O01 e O02 / M01 caminho principal / F01 → F01B → F01L → F02 → F02P → F02C → F02S. MU01, MU02, MU06 | Chega à confirmação de peso salvo (F02S) com o boi 117 do Pasto 2, sem ajuda. Sucesso parcial: chega com ajuda ou depois de voltar mais de uma vez | 3 min |
| — | Pergunta logo após a UT01: "Com o que você viu na tela, quanto esse boi pesa? Você usaria esse número do mesmo jeito que o da balança?" | O06 / MQ01. MU05 | Diz com as próprias palavras que o peso é aproximado ou que pode variar cerca de 20 kg | — |
| UT02 | "Você tirou esta foto e quer saber o peso do animal." *(começa no fluxo 2, F01C)* | Ruptura "boi não reconhecido" / M01 / F02E → F01. MU04, MQ03 | Entende que a foto não serviu e volta para tirar outra foto, sem tentar salvar e sem ajuda | 2 min |
| UT03 | "O brinco deste boi está sujo e não dá para ler o número. Você sabe que ele é do Pasto 2 e que o pessoal chama ele de Pintado. Você quer guardar o peso que acabou de ver no registro dele." *(começa na F02)* | T02, HTA 3.2 / O02 / M01 alternativa "brinco ilegível" / F02 → F02L → F02C → F02S. QA05, QA02 | Escolhe o Pintado na lista do lote, confere e salva, sem ajuda. [?] Confirmar no piloto que a F02C mostra o animal escolhido | 2 min |
| UT04 | "O técnico que visita a fazenda quer saber quanto o boi 117 já engordou desde que começou a ser pesado." *(começa na F01, aba de baixo disponível)* | T01 / O03, O04 e O05 /M02 caminho principal/ F03 → F04. MU03, MU07, MQ04 | Abre o histórico do boi 117 e diz o ganho total que aparece na F04 | 2 min |
| UT05 *(reserva, se sobrar tempo)* | "Você quer guardar o peso deste boi, que você anotou como 999." *(começa no fluxo 3, F02U)* | Ruptura "nenhum bovino encontrado" / M01 / F02U → F02N. QA09 | Entende que não há boi com esse número e escolhe uma saída (corrigir, procurar pelo lote ou animal novo) sem ajuda | 2 min |

[H] A ordem é fixa (UT01 → UT02 → UT03 → UT04) porque a UT01 apresenta o app. A UT04 vem por último porque é outro fluxo (histórico). O efeito de aprendizagem entre as tarefas fica registrado como limitação.

## E. Instrumentos

- [Modelo de termo de consentimento](../instrumentos/termo_consentimento_modelo.md), adaptado com: objetivo ("ver se o aplicativo é fácil de usar"), duração (~25 min), que o peso mostrado é simulado, autorização separada para gravar, anonimização (U01–U03) e descarte no fim da disciplina.
- [Roteiro de teste](../instrumentos/roteiro_teste_usabilidade.md), com as tarefas UT01–UT05 desta seção e o que o moderador pode e não pode dizer (não dizer "Salvar no histórico", "Escolher o animal pelo lote", "Tirar outra foto" nem a aba "Histórico").
- [Planilha de observação](../instrumentos/planilha_observacao_modelo.md), uma por participante: início e fim de cada tarefa, sucesso, erros, ajudas, falas e nota.
- [Formulário de avaliação heurística](../instrumentos/formulario_heuristica_modelo.md), um por integrante na Entrega 13.
- **Questionário pré-teste** (perfil, 4 perguntas): papel no manejo do gado; com que frequência pesa ou acompanha o peso dos animais; se usa smartphone no dia a dia e para quê; se já usou algum app de pecuária. Serve para interpretar os resultados e marcar participante proxy.
- **Questionário pós-tarefa:** depois de cada tarefa, "Foi fácil fazer isso?" de 1 (muito difícil) a 5 (muito fácil) e "O que deixou fácil ou difícil?". No fim, a pergunta aberta "O que você mudaria nesse aplicativo?".

## F. Plano de análise

- **Sucesso:** *total* = chegou ao resultado da tarefa sem ajuda; *parcial* = chegou com uma ajuda ou depois de se perder e voltar; *falha* = desistiu, passou do tempo-limite, precisou de mais de uma ajuda ou terminou no resultado errado (por exemplo, peso salvo em outro animal).
- **Erro:** toque que leva para fora do caminho da tarefa, ou salvar no animal errado. **Dúvida:** hesitação de mais de 5 s ou pergunta em voz alta, sem pedir ajuda. **Ajuda:** qualquer dica do moderador sobre o que fazer. **Abandono:** o participante diz que desiste ou para de tentar.
- **Tempo:** do fim da leitura da instrução até a tela de sucesso (F02S na UT01, F04 na UT04), pela gravação ou por cronômetro. Usar a mediana dos 3 participantes, só das tentativas com sucesso.
- **Satisfação:** média da nota de 1 a 5 por tarefa e no geral (MU08).
- **Falas e observações:** codificadas por tela (F01…F05D) e por tema (identificação do animal, margem de erro, recuperação de erro, vocabulário, navegação).
- **Priorização:** severidade de Nielsen de 0 a 4 (0 = não é problema; 1 = cosmético; 2 = menor; 3 = grave; 4 = catástrofe), considerando quantos participantes tiveram o problema, se ele impede a tarefa e se volta a acontecer. Empate se desfaz pelo peso da meta afetada na Entrega 8 (MU01 e MU02 primeiro). Problema que aparece na Entrega 13 e na Entrega 14 sobe um nível.
- **Comparação com as metas:** tabela final com cada meta MU01–MU08 e MQ01–MQ05, o valor obtido (ex.: "2 de 3", "48 s"), atingida ou não, e a mudança proposta no protótipo. As mudanças voltam para a Entrega 11 e para a RASTREABILIDADE.md.

## Responsáveis e cronograma

| Atividade | Responsável | Data [H] |
|---|---|---|
| Adaptar termo, roteiro e questionários | Rafael | 16/11 |
| Recrutar U01, U02 e U03 | Rafael (U01), Gustavo (U02) e Renan (U03) | 16/11 a 18/11 |
| Avaliação heurística individual (Entrega 13) | Cada integrante | 16/11 a 19/11 |
| Teste piloto | Rafael, com colega de outra equipe | 19/11 |
| Sessões de teste | Cada integrante conduz a sua; outro integrante anota, se possível | 20/11 a 24/11 |
| Consolidação e comparação com as metas | Equipe | 25/11 a 26/11 |

## Checklist

- [x] As seis etapas DECIDE foram contextualizadas, não apenas expandidas por sigla.
- [x] Perguntas de avaliação têm método e evidência correspondentes.
- [x] O plano distingue avaliação de IHC de avaliação técnica/científica do TCC.
- [x] Dados ou processamentos simulados no protótipo estão declarados.
- [x] Tarefas vêm de objetivos/cenários relevantes.
- [x] Critérios de sucesso foram definidos antes da coleta.
- [ ] Questões práticas e éticas estão resolvidas. *(falta confirmar participantes e datas)*
- [ ] Instrumentos estão prontos antes da Entrega 13/14. *(falta adaptar termo e roteiro)*
- [x] Plano diz como dados serão analisados e apresentados.
