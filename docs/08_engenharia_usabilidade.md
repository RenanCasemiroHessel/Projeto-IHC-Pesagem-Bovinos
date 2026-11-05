# Entrega 8 — Ciclo de vida e engenharia de usabilidade

**Data:** 28/10/2026  
**Status:** 🟩 concluído  
**Responsabilidade:** 1 solução por equipe

## Objetivo da atividade

Transformar o conhecimento acumulado sobre usuários, tarefas, plataforma e contexto em princípios e **metas de usabilidade verificáveis**, mantendo o caráter iterativo do projeto.

## Delimitação do sistema interativo

Antes das características da plataforma, separe:

| Camada | O que pertence ao projeto | O que será avaliado em IHC |
|---|---|---|
| contribuição técnica do TCC | Modelo de visão computacional que estima o peso de um bovino a partir de uma foto | desempenho técnico não é substituído pelo teste de IHC |
| camada de interação da disciplina | Fluxo de estimar o peso e salvar no animal (Telas 1, 2 e E1) e fluxo de consultar o histórico do animal (Telas 3 e 4) | compreensão, eficácia, eficiência, satisfação, erros e recuperação, compreensão da margem de erro |
| integrações/dados simulados | No protótipo de teste, os animais, as pesagens anteriores e os ganhos de peso serão **dados fictícios**, para que todo participante veja o mesmo histórico. | O teste avalia se a pessoa entende e usa as telas, não se o peso estimado está correto |

Em um protótipo de disciplina, é aceitável simular processamento ou resultados quando a implementação técnica não estiver integrada, desde que isso seja declarado e a simulação seja suficiente para avaliar a interação.

## 1. Características da plataforma

| Característica | Descrição | Consequência para IHC |
|---|---|---|
| Software | Aplicativo para smartphone, usado pelo produtor, pelo peão e pelo técnico | Interface pensada para tela pequena e toque, o histórico precisa ficar disponível para quem acompanha o rebanho, inclusive o técnico (H05) |
| Hardware/dispositivos |  Smartphone do produtor ou do peão, muitas vezes simples, com pouca bateria e pouco armazenamento (P03) | Telas leves, botões grandes, uso com uma mão. |
| Capacidades | Câmera para a foto lateral, estimativa do peso a partir de uma foto, aviso quando o boi não é reconhecido | Uma foto basta, sem acessório (H04, H07). O aviso de "boi não reconhecido" (E1) evita salvar uma estimativa errada |
| Restrições |  O peso é uma estimativa e tem margem de erro, o modelo precisa do animal inteiro na foto | A interface precisa mostrar a margem de erro, orientar a foto e tratar o "boi não reconhecido" (E1) |
| Conectividade/latência | Curral e pasto com sinal fraco ou nenhum (H01). A estimativa depende de {{confirmar: processamento no servidor ou no aparelho}} | Se depender de internet, mostrar claramente "aguardando sinal" e não perder a foto. Está fora do protótipo atual e fica registrado como limitação |
| Segurança/privacidade | Fotos de animais e da propriedade, peso e tamanho do rebanho são informação patrimonial do produtor. Fotos podem levar a localização GPS nos metadados | Não pedir dados pessoais além do necessário, remover a localização das fotos, o compartilhamento é decidido pelo produtor |
| Volume de dados/histórico | Lotes de ~30 animais (C03) e poucas pesagens por animal por ano (2 a 4 hoje, talvez mais com o app) | Lista simples com busca por número ou lote é suficiente. Não é preciso paginação, filtros avançados nem dashboard |  
| Tempo de processamento | Alguns segundos por foto |  Não deixar tocar duas vezes em "Estimar peso" |
| Papéis/permissões | Produtor, técnico e peão usam o mesmo app | Sem telas de administração. Prevenção de erros fica na identificação do animal (não salvar no animal errado) |

## 2. Princípios gerais do projeto

Inclua apenas normas, leis, padrões e princípios realmente relevantes, explicando **como** afetam o projeto. Não transforme esta seção em lista de links.

| Princípio/norma | Aplicabilidade ao contexto | Decisão/requisito decorrente | Fonte |
|---|---|---|---|
| Contexto de uso | [H] O uso acontece no curral ou no pasto, no celular pessoal do produtor ou do peão, com sol forte, poeira, mão suja, sinal instável e animal em movimento. Ainda é hipótese, porque vem das personas e dos cenários, sem usuário real entrevistado. | Texto grande e contraste alto, botões grandes nas ações principais, uso com uma mão, mensagens curtas, não perder a foto quando o sinal cair. | Entregas 1/3 |
| LGPD (Lei 13.709/2018) | [H] Dados do produtor e do técnico (cadastro, localização da propriedade) são dados pessoais. O peso e as fotos do rebanho ficam ligados a uma pessoa identificável, então tratamos com o mesmo cuidado. | Pedir só o necessário, remover o GPS das fotos, compartilhar com frigorífico, veterinário ou técnico só por ação explícita do produtor, explicar isso em linguagem simples. | Lei 13.709/2018: https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm |
| Acessibilidade (WCAG) | [H] Sol forte e tela suja pioram a leitura. [?] Não sabemos o nível de escolaridade e de letramento digital do público, então o texto precisa ser simples. | Contraste mínimo de 4,5:1 no texto (nível AA), buscando mais nos elementos principais por causa do sol. Não indicar estado só por cor: o aviso "boi não reconhecido" leva ícone e texto. Alvos de toque grandes. | WCAG 2.2: https://www.w3.org/TR/WCAG22/ |
| Heurísticas de Nielsen | [H] Quatro delas pesam mais aqui: prevenção de erros (salvar no animal errado), visibilidade do estado do sistema (processando, sem sinal), correspondência com o mundo real (brinco, lote, @) e ajuda para se recuperar de erros (E1). | Confirmar o animal antes de salvar, mostrar sempre o estado da estimativa, usar o vocabulário do produtor, e dar saída clara quando a foto falha. Serão base da avaliação da Entrega 13. | Nielsen, 10 Usability Heuristics: https://www.nngroup.com/articles/ten-usability-heuristics/ |
| Convenções de plataforma e de apps familiares | [H] O público já usa WhatsApp no dia a dia e provavelmente usa Android. [?] Falta confirmar a plataforma mais comum entre os usuários. | Navegação simples, parecida com o WhatsApp. Componentes e tamanhos de toque do Material Design como base no Figma (Entrega 11). | Material Design 3: https://m3.material.io |
| ISO 9241-11 | [F] Define usabilidade como eficácia, eficiência e satisfação em um contexto de uso. Os slides de Mayhew usam essas três dimensões como base das exigências quantitativas. | As metas da seção 3 são organizadas nessas três dimensões e medidas no contexto de uso do projeto, sem generalizar. | ISO 9241-11 (confirmar edição e link antes do commit) |


## 3. Metas de usabilidade

Usabilidade deve ser discutida **no contexto de uso**. Metas quantitativas devem dizer o que será medido, em qual tarefa, com qual população e qual limite será considerado aceitável.

### 3.1 Metas qualitativas

| Meta | Para quem/tarefa | Evidência desejada | Justificativa |
|---|---|---|---|
| MQ01: entender que o peso é uma estimativa com margem de erro | Produtor, peão e técnico, ao estimar e salvar o peso | O participante diz com as próprias palavras que o número é aproximado e não age como se fosse o peso de balança | [F] O erro médio do TCC é de cerca de 20 kg. Quem vende ou trata o animal com base no número precisa saber disso. Exige da interface: margem visível junto do peso. |
| MQ02: saber em qual animal o peso será salvo | Produtor e peão, ao identificar o animal antes de salvar (A02) | O participante lê ou confirma o número do brinco antes de salvar, e percebe quando o animal está errado | [H] Um peso no animal errado estraga o histórico daquele animal, e a A02 é a atividade mais crítica. Exige da interface: animal identificado de forma bem visível na tela de confirmação. |
| MQ03: se recuperar sozinho do "boi não reconhecido" | Produtor e peão, na tela E1 | O participante entende o que aconteceu e tira outra foto sem pedir ajuda | [H] No curral a foto vai falhar com frequência (animal em movimento, cortado). Exige da interface: mensagem curta com a próxima ação clara. |
| MQ04: entender o histórico sem treinamento | Produtor e técnico, ao consultar o histórico (T01) | O participante usa as palavras da tela (brinco, lote, @) sem perguntar o que significam e acha o ganho de peso | [H] O público conhece esse vocabulário. Exige da interface: textos nessas palavras e lista simples. |
| MQ05: conseguir operar com uma mão e sob condição de campo | Produtor e peão, no curral ou pasto | O participante opera as telas principais com uma mão, sem errar toque repetidas vezes | [H] Mão suja, sol e celular simples. Exige da interface: botões grandes e contraste alto. [?] O teste no Figma não reproduz sol e poeira, então fica como limitação e é reforçado na avaliação heurística. |


### 3.2 Metas quantitativas

| ID | Dimensão | Métrica | Tarefa/escopo | Meta | Como medir | Justificativa |
|---|---|---|---|---|---|---|
| MU01 | eficácia | taxa de conclusão sem ajuda | Estimar o peso e salvar no animal correto (A01 + A02; confirmar ID na Entrega 5) | ≥ 80% | teste observado, com os dados fictícios | A01 é a atividade mais frequente, então precisa funcionar de primeira. |
| MU02 | eficácia (erros) | peso salvo no animal errado sem o participante perceber | A mesma tarefa, com animais de brincos parecidos no protótipo | 0 casos | teste observado, comparando o animal pedido com o animal salvo | A A02 é a mais crítica, e um erro compromete todo o histórico do animal. |
| MU03 | eficácia | taxa de conclusão sem ajuda | T01: consultar o histórico de peso de um animal | ≥ 80% | teste observado | Consultar é o que dá valor ao registro feito antes. |
| MU04 | eficácia (recuperação) | participantes que refazem a foto sem ajuda depois da tela E1 e sem salvar a estimativa | Tela E1 (boi não reconhecido; confirmar ID da tarefa) | ≥ 80% | teste observado, com a falha simulada | A foto vai falhar no curral, e o erro precisa ser fácil de contornar. |
| MU05 | eficácia (compreensão) | participantes que explicam corretamente que o peso é aproximado | Pergunta depois da tarefa de estimar | ≥ 80% | pergunta aberta, com a fala anotada | Mede se a margem de erro foi entendida (MQ01) de forma que dê para contar. |
| MU06 | eficiência | tempo mediano, da tela de captura até a confirmação de que o peso foi salvo | Estimar o peso e salvar | ≤ 60 s | cronômetro no teste | [H] Valor de ordem de grandeza (foto, alguns toques e alguns segundos de espera). Ajustar com o tempo do GOMS-KLM da Entrega 5 e depois do piloto. |
| MU07 | eficiência | tempo mediano | T01: consultar o histórico de um animal por brinco ou lote | ≤ 30 s | cronômetro no teste | [H] Mesma lógica do MU06. A lista é simples e a busca é por número. |
| MU08 | satisfação | escala de Likert de 5 pontos, depois de cada tarefa ("Foi fácil fazer isso?") | Todas as tarefas do teste | média ≥ 4 | questionário pós-tarefa | Satisfação é a terceira dimensão da usabilidade e a escala de Likert é simples de responder. |

### 3.3 Priorização das metas (se exigida na disciplina)

Se o professor solicitar porcentagens que somem 100%, trate-as como **peso de prioridade**, não como métrica de usabilidade.

| Meta | Peso de prioridade | Justificativa |
|---|---:|---|
| MU01 | 20% | É a atividade mais frequente do app. |
| MU02 | 20% | Erro de identificação é o risco mais grave para o histórico. |
| MU03 | 10% | Sem consulta, o registro não serve para nada. |
| MU04 | 10% | A falha de foto vai ser comum no campo. |
| MU05 | 15% | Quem não entende a margem de erro pode decidir com base em um número errado. |
| MU06 | 10% | Importa no curral, mas depende de medida que ainda não temos. |
| MU07 | 5% | A lista é pequena, então o risco é baixo. |
| MU08 | 10% | Complementa as medidas objetivas. |
| **Total** | **100%** | |

## 4. Como o ciclo será iterado

O projeto segue as três camadas da engenharia de usabilidade de Mayhew, repetidas para cada grupo de funcionalidades essenciais. Aqui os dois grupos são o fluxo de estimar e salvar o peso e o fluxo de consultar o histórico.
| Camada de Mayhew | O que significa | Onde aparece no projeto |
|---|---|---|
| Análise de requisitos | Perfil do usuário, tarefas, plataforma, princípios gerais e metas de usabilidade | Entregas 3 (personas), 5 (tarefas) e 8 (plataforma, princípios e metas) |
| Nível 1: projeto essencial | Modelo conceitual e maquete em papel com só o essencial, testada com simulação dupla (o usuário usa a maquete e o projetista troca as telas) | Entrega 6 (papel), Entrega 9 (modelo conceitual) e Entrega 10 (MoLIC). [?] Confirmar se a Entrega 6 teve teste de simulação dupla. |
| Nível 2: padrões de telas e protótipo | Regras de controles, cores, fontes e terminologia, com protótipo de baixa fidelidade e testes mais realistas | Entrega 11 (Figma), usando a seção 2 como guia, e Entregas 13 e 14 (avaliação) |
| Nível 3: projeto detalhado | Janelas, mensagens e opções não essenciais, e testes com o sistema final | [H] Fora do escopo da disciplina. Fica para o TCC 2 (por exemplo dashboard, filtros avançados, funcionamento sem sinal). |
| Instalação e feedback | Feedback de quem já usa o sistema no dia a dia | [H] Só será possível se o TCC 2 chegar a uso real. |


## Checklist

- [x] Capacidades e restrições têm impacto de IHC explicitado.
- [x] Está claro o limite entre contribuição técnica do TCC e camada interativa da disciplina.
- [x] Resultados/processamento simulados no protótipo foram explicitados.
- [x] Metas de usabilidade avaliam a interação, não substituem métricas técnicas do TCC.
- [x] Normas/princípios estão contextualizados, não apenas copiados.
- [x] Metas quantitativas são mensuráveis e associadas a tarefas/público.
- [x] Eficácia, eficiência e satisfação são consideradas quando pertinentes.
- [x] Metas poderão ser verificadas nas Entregas 12–14.
