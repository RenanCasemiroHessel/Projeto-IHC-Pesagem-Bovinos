# Entrega 11 — Protótipo no Figma

**Data:** 14/11/2026  
**Status:** 🟨 em andamento (falta liberar o link e subir os prints)  
**Responsabilidade:** 1 protótipo integrado por equipe. Nesta versão o protótipo cobre o fluxo do M01 (Rafael Takahagi Mendes) e as telas de histórico da prototipação em papel. [?] Os outros integrantes ainda não fizeram o MoLIC deles. Quando fizerem, a cobertura será conferida e as telas que faltarem serão acrescentadas.

## Objetivo da atividade

Materializar o modelo de interação em um protótipo navegável, preservando a lógica dos objetivos, tópicos, signos, feedbacks, alternativas e recuperações definidos anteriormente.

## Biblioteca de possibilidades para projetos técnicos

Do repertório da disciplina, o protótipo usa:

| Item da biblioteca | Onde aparece | Por que existe |
|---|---|---|
| Entrada de dados | F01, F01B, F02, F02L, F02X | O usuário escolhe ou tira a foto, informa o sexo e identifica o animal (O01, O02) |
| Processamento | F01L | A estimativa leva alguns segundos. O estado de espera evita toque duplo |
| Relatório/resultados | F02 | Mostra o peso em kg e em @ |
| Explicabilidade | F02 | Margem de erro (± 20 kg), faixa na barra e o aviso "Estimativa por foto, não substitui a balança" (H02) |
| Alertas/ocorrências | F02E, F02N, F02A | Dizem o que deu errado e o que fazer em seguida |
| Histórico | F03, F03V, F04 | Lista de pesagens, busca por número ou lote e detalhe do animal (Telas 3 e 4 do papel) |

[F] Dashboard, configuração, comparação, administração, CRUDs, auditoria e ajuda ficaram fora. Múltiplos usuários, permissões e auditoria estão fora do escopo desde a Entrega 1.

### Estados que não podem ser esquecidos

| Estado | Tela | Situação |
|---|---|---|
| Vazio/sem dados | F03V | ✅ Prototipado |
| Carregamento/processamento | F01L | ✅ Prototipado ("Calculando o peso…") |
| Sucesso | F02S, F05 | ✅ Prototipado |
| Erro de entrada | F02A, F02N | ✅ Falta identificar o animal / nenhum bovino com esse número |
| Erro de processamento | F02E | ✅ Boi não reconhecido |
| Filtro sem resultados | — | ❌ Não prototipado (busca do F03). Fica para a próxima versão |
| Permissão insuficiente | — | Não se aplica (sem perfis) |
| Confirmação de ação | F02C | ✅ Conferir antes de salvar (protege o A02) |
| Confirmação de ação destrutiva | — | Não se aplica (o escopo não tem exclusão) |
| Cancelamento/desfazer/recuperação | F01B, F02C, F02E, F02N, F05D | ✅ "Trocar foto", "Não é esse", "Tirar outra foto", "Corrigir o número" e "Desistir" |
| Dados desatualizados/conflito | — | Fora do escopo (falta de sinal e "pendente de envio" ficaram fora na Entrega 9) |

## Link do Figma

**Protótipo:** https://www.figma.com/proto/vvwn3MeDQGGoP3d3y5GCwB (confirmar em Share → Copy prototype link)  
**Arquivo editável:** https://www.figma.com/design/vvwn3MeDQGGoP3d3y5GCwB  
**Última verificação de permissão:** 14/11/2026

> Teste o link em janela anônima. O avaliador deve conseguir abrir o protótipo sem solicitar permissão.

**Fluxos de partida no protótipo:**

1. **Principal: pesar e salvar** (começa em F01).
2. **Erro: boi não reconhecido** (começa em F01C).
3. **Erro: nenhum bovino encontrado** (começa em F02U).
4. **Primeiro uso: histórico vazio** (começa em F03V).

## Cobertura MoLIC → Figma

| MoLIC | Objetivo | Fluxo/telas no Figma | Estados de erro/recuperação | Responsável |
|---|---|---|---|---|
| M01 | O01 (peso estimado pela foto) | `F01 → F01B → F01L → F02` | `F01C → F02E → F01` | Rafael |
| M01 | O02 (salvar no animal certo) | `F02 → F02P → F02C → F02S → F05` (ou `F02L → F02C`) | `F02A → F02P`, `F02U → F02N → F02 / F02L / F02X`, `F02C → F02` ("Não é esse"), `qualquer tela → F05D` (desistir) | Rafael |
| [?] MoLIC ainda não feito | O06 (histórico) | `F03 → F04`, `F03V` | — | [?] a definir |

### Cena por cena: M01 × Figma

| Cena/estado do M01 | Tela no Figma | Situação | Observação |
|---|---|---|---|
| Ponto de abertura (`gco: Pesar um animal por foto`) | F01 | ✅ | Aba "Pesar" da barra de navegação |
| Fotografar o animal | F01, F01B | ✅ | Dica "foto de lado, com o animal inteiro, de dia", escolha de macho ou fêmea e "Estimar Peso" |
| Calculando o peso | F01L | ✅ | Mesmo texto do MoLIC: "Calculando o peso…" |
| Boi não reconhecido | F02E | ✅ | Mesma fala do MoLIC. Sem peso e sem salvar. "Tirar outra foto" volta para F01 |
| Ler o peso estimado | F02 | ✅ | kg, @ e margem de ± 20 kg. [F] Fica na mesma tela da identificação, como no papel (Tela 2) |
| Identificar o animal | F02, F02P, F02L | ✅ | Digitar lote e brinco/nome ou "Escolher o animal pelo lote" (lista com foto da última pesagem e nome, caminho para brinco ilegível) |
| Procura o animal no cadastro (processo do sistema) | — | Simulado | No protótipo, o 117 é sempre encontrado e o 999 nunca é |
| Nenhum bovino encontrado | F02N | ✅ | As três saídas do MoLIC: "Corrigir o número", "Procurar pelo lote" e "Informar como animal novo". O peso continua guardado |
| Informar animal novo [?] | F02X | 🟨 Provisória | [?] Os dados pedidos continuam em aberto desde a Entrega 5. A tela avisa isso. "Confirmar os dados" segue para a conferência, como no MoLIC |
| Conferir antes de salvar | F02C | ✅ | Brinco e foto grandes, "Salvar 214 kg no boi 117, lote Pasto 2?", "Salvar" e "Não é esse". "Não é esse" volta à identificação sem perder o peso e sem refazer a foto |
| Peso salvo | F02S | ✅ | Boi, lote, peso e data, com "Pesar o próximo animal" e "Terminar de pesar" |
| Ponto de encerramento (`gcc`) | F05 | ✅ | "Pesagem encerrada", com resumo das pesagens do dia |
| Desistir da pesagem [H] | "Desistir" no cabeçalho de F01B a F02X → F05D | ✅ | [H] Fica no canto superior direito, em vermelho. Leva a "Pesagem cancelada. Nada foi salvo." Não aparece na F01 (ainda não há pesagem) nem na F01L (o cálculo leva só alguns segundos) |

### O que está no Figma e não está no M01

[F] **F02A** (aviso "Identifique o animal antes de salvar") e **F02P** (animal identificado) vêm do papel, em que o resultado e a identificação ficam numa tela só. O aviso impede salvar com os campos vazios. A troca de animal continua protegida pela F02C.

[F] **F02U** existe só para dar ponto de partida ao fluxo "nenhum bovino encontrado" (número 999 digitado). No app real, esse caminho viria da busca no cadastro.

[F] **F01C** existe só para dar ponto de partida ao fluxo "boi não reconhecido". No app real, o erro viria da estimativa.

[?] **F03, F03V e F04** (histórico) vêm das Telas 3 e 4 do papel. Nenhum MoLIC cobre o histórico ainda, porque os outros integrantes não fizeram o deles.

### Papel × Figma

| Rascunho | Tela no Figma | O que mudou |
|---|---|---|
| Tela 1 | F01, F01B | [H] Acrescentados: dica de enquadramento, escolha de sexo (vinda do M01 e da Entrega 9), "Trocar foto", botão "Estimar Peso" desabilitado sem foto e barra de navegação |
| Tela 2 | F02, F02A, F02P | [H] Margem em kg e em % ("± 20 kg (cerca de 9%)") em vez de só "X%". Acrescentado "Escolher o animal pelo lote" (M01). [F] Dos chips Leve / Médio / Pesado só foi usada a tag "Leve". [?] As faixas de cada classe não foram definidas pela equipe |
| Tela 3 | F03 | [H] Lote numa linha separada no card e seta indicando que o card abre |
| Tela 4 | F04 | Igual ao papel |
| Tela erro | F02E | [F] Texto trocado de "Bovino não reconhecido" / "Tirar ou escolher outra foto" para "Boi não reconhecido" / "Tirar outra foto", para seguir o signo do M01 e da Entrega 9. O botão "Estimar Peso" fica desabilitado |
| — (não havia no papel) | F01L, F01C, F02U, F02N, F02L, F02X, F02C, F02S, F05, F05D, F03V | [F] Telas que saem do M01 ou dos estados que a disciplina pede |

[H] **Barra de navegação** (Pesar / Histórico) em todas as telas. O papel não mostrava como ir da Tela 1 para a Tela 3.

[?] A conversão de peso vivo para @ usada no exemplo (15 kg por @, 214 kg = 14,3 @) precisa ser confirmada com a equipe (Entrega 9).

## Catálogo de telas/estados

### F01 — Capturar foto

![F01](../assets/11_figma/F01%20%E2%80%94%20Capturar%20foto.png)

**Objetivo do usuário:** escolher ou tirar a foto do animal que está à frente.  
**Signos principais:** área "Escolher ou tirar foto de bovino", dica de enquadramento, "Sexo do animal" (Macho / Fêmea), "Estimar Peso" desabilitado, barra Pesar/Histórico.  
**Origem no MoLIC:** M01 / ponto de abertura e cena Fotografar o animal (`d: tire uma foto do boi, de lado e inteiro`).

### F01B — Foto escolhida

![F01B](../assets/11_figma/F01B%20%E2%80%94%20Foto%20escolhida.png)

**Objetivo do usuário:** conferir a foto, informar o sexo e pedir a estimativa.  
**Signos principais:** foto do animal, "Trocar foto", Macho selecionado, "Estimar Peso" habilitado, "Desistir".  
**Origem no MoLIC:** M01 / cena Fotografar o animal (`u: toca em "Estimar peso"`).

### F01L — Calculando o peso

![F01L](../assets/11_figma/F01L%20%E2%80%94%20Estimando.png)

**Objetivo do usuário:** saber que o app está trabalhando e esperar.  
**Signos principais:** ícone de carregando, "Calculando o peso…", "Pode levar alguns segundos.", botão "Estimando…" desabilitado.  
**Origem no MoLIC:** M01 / processo do sistema "estima o peso pela foto".

### F01C — Foto sem bovino

![F01C](../assets/11_figma/F01C%20%E2%80%94%20Foto%20sem%20bovino.png)

**Objetivo do usuário:** (demonstração) foto que vai gerar o erro de reconhecimento.  
**Signos principais:** foto sem animal, "Trocar foto", "Estimar Peso".  
**Origem no MoLIC:** M01 / entrada da ruptura "boi não reconhecido". [H] Existe só como ponto de partida do fluxo de erro.

### F02E — Boi não reconhecido

![F02E](../assets/11_figma/F02E%20%E2%80%94%20Boi%20n%C3%A3o%20reconhecido.png)

**Objetivo do usuário:** entender que a foto não serviu e tirar outra.  
**Signos principais:** alerta vermelho com ícone, "Boi não reconhecido", "Não reconhecemos o boi. Fotografe de lado, com o corpo inteiro na foto.", "Tirar outra foto". Sem peso e sem botão de salvar.  
**Origem no MoLIC:** M01 / cena de alerta Boi não reconhecido (MQ03).

### F02 — Resultado e identificação

![F02](../assets/11_figma/F02%20%E2%80%94%20Resultado.png)

**Objetivo do usuário:** ler o peso, entender a margem de erro e identificar o animal.  
**Signos principais:** sexo e margem de erro ("± 20 kg (cerca de 9%)"), peso em kg e em @, tag de classe de peso, barra de 0 a 300 kg com a faixa da margem, campos Lote e Nº do brinco ou nome, "Escolher o animal pelo lote", "Salvar no Histórico".  
**Origem no MoLIC:** M01 / cenas Ler o peso estimado e Identificar o animal. [F] Juntas numa tela, como no papel.

### F02A — Falta identificar o animal

![F02A](../assets/11_figma/F02A%20%E2%80%94%20Falta%20identificar%20o%20animal.png)

**Objetivo do usuário:** perceber que não dá para salvar sem identificar o animal.  
**Signos principais:** campos com borda vermelha, "Identifique o animal antes de salvar."  
**Origem no MoLIC:** sem cena equivalente [H]. Vem da junção de cenas feita no papel.

### F02P — Animal identificado

![F02P](../assets/11_figma/F02P%20%E2%80%94%20Animal%20identificado.png)

**Objetivo do usuário:** pedir para salvar o peso no animal digitado.  
**Signos principais:** Lote "Pasto 2" e brinco "117" preenchidos, "Salvar no Histórico".  
**Origem no MoLIC:** M01 / cena Identificar o animal (`u: é o 117`).

### F02L — Escolher pelo lote

![F02L](../assets/11_figma/F02L%20%E2%80%94%20Escolher%20pelo%20lote.png)

**Objetivo do usuário:** achar o animal quando o brinco está sujo, caído ou ilegível.  
**Signos principais:** "Lote Pasto 2 · 4 animais", lista com foto da última pesagem, número, nome ("Pintado", "Malhado", "Mocho") e data, "Voltar e digitar o número".  
**Origem no MoLIC:** M01 / cena Identificar o animal, alternativa "brinco sujo, caído ou ilegível".

### F02U — Número não cadastrado

![F02U](../assets/11_figma/F02U%20%E2%80%94%20N%C2%BA%20n%C3%A3o%20cadastrado.png)

**Objetivo do usuário:** (demonstração) número digitado que não existe no cadastro.  
**Signos principais:** brinco "999" preenchido, "Salvar no Histórico".  
**Origem no MoLIC:** M01 / entrada da ruptura "nenhum bovino encontrado". [H] Existe só como ponto de partida do fluxo de erro.

### F02N — Nenhum bovino encontrado

![F02N](../assets/11_figma/F02N%20%E2%80%94%20Nenhum%20bovino%20encontrado.png)

**Objetivo do usuário:** entender que o número não existe e escolher como seguir sem perder o peso.  
**Signos principais:** peso guardado (214 kg · 14,3 @ ± 20 kg), alerta "Nenhum bovino encontrado", "Corrigir o número", "Procurar pelo lote", "Informar como animal novo".  
**Origem no MoLIC:** M01 / cena de alerta Nenhum bovino encontrado.

### F02X — Informar animal novo [?]

![F02X](../assets/11_figma/F02X%20%E2%80%94%20Informar%20animal%20novo%20%5B_%5D.png)

**Objetivo do usuário:** cadastrar na hora um animal que ainda não existe.  
**Signos principais:** aviso de tela provisória, peso a salvar, campos Nº do brinco ou nome e Lote, sexo vindo da foto, "Confirmar os dados", "Voltar".  
**Origem no MoLIC:** M01 / cena Informar animal novo [?]. [?] Os dados pedidos ainda não foram decididos.

### F02C — Conferir antes de salvar

![F02C](../assets/11_figma/F02C%20%E2%80%94%20Conferir%20antes%20de%20salvar.png)

**Objetivo do usuário:** confirmar que o peso vai para o animal que está à frente.  
**Signos principais:** foto da última pesagem em destaque, "Boi 117" em 40 px, "Lote Pasto 2 · Macho · Pintado", "Salvar 214 kg no boi 117, lote Pasto 2?", "Salvar", "Não é esse".  
**Origem no MoLIC:** M01 / cena Conferir antes de salvar (A02).

### F02S — Peso salvo

![F02S](../assets/11_figma/F02S%20%E2%80%94%20Peso%20salvo.png)

**Objetivo do usuário:** ter certeza de que o peso foi gravado no animal certo e seguir.  
**Signos principais:** selo verde, "Peso salvo!", "Boi 117 · Lote Pasto 2", "214 kg (estimativa)", data, "Pesar o próximo animal", "Terminar de pesar".  
**Origem no MoLIC:** M01 / cena Peso salvo (`d: peso salvo no boi 117`).

### F05 — Pesagem encerrada

![F05](../assets/11_figma/F05%20%E2%80%94%20Pesagem%20encerrada.png)

**Objetivo do usuário:** fechar a pesagem e saber o que foi feito.  
**Signos principais:** "Pesagem encerrada", "Pesagens salvas hoje: 1 animal", data, "Começar nova pesagem", "Ver histórico".  
**Origem no MoLIC:** M01 / `u: terminar de pesar` → ponto de encerramento.

### F05D — Pesagem cancelada

![F05D](../assets/11_figma/F05D%20%E2%80%94%20Pesagem%20cancelada.png)

**Objetivo do usuário:** saber que desistiu e que nada foi gravado.  
**Signos principais:** ícone cinza, "Pesagem cancelada", "Nada foi salvo.", "Peso descartado", "Começar nova pesagem", "Ver histórico".  
**Origem no MoLIC:** M01 / acesso ubíquo `u: desistir da pesagem` [H] → ponto de encerramento.

### F03 — Histórico de estimativas

![F03](../assets/11_figma/F03%20%E2%80%94%20Hist%C3%B3rico%20de%20estimativas.png)

**Objetivo do usuário:** achar um animal pelo número ou pelo lote.  
**Signos principais:** busca "Pesquise por número ou lote", cards com foto, brinco, lote, peso, data da última estimativa e seta.  
**Origem no MoLIC:** [?] ainda sem MoLIC (Tela 3 do papel).

### F03V — Histórico vazio

![F03V](../assets/11_figma/F03V%20%E2%80%94%20Hist%C3%B3rico%20vazio.png)

**Objetivo do usuário:** entender por que a lista está vazia e o que fazer.  
**Signos principais:** "Nenhuma pesagem salva ainda", "Pesar primeiro bovino".  
**Origem no MoLIC:** [?] ainda sem MoLIC. Estado de vazio pedido pela disciplina.

### F04 — Histórico do bovino

![F04](../assets/11_figma/F04%20%E2%80%94%20Hist%C3%B3rico%20do%20bovino.png)

**Objetivo do usuário:** ver a evolução de peso de um animal.  
**Signos principais:** "Todos os bovinos" (voltar), número de estimativas, ganho total, lista de pesagens com peso, diferença para a anterior e data (marcadas como estimativa).  
**Origem no MoLIC:** [?] ainda sem MoLIC (Tela 4 do papel).

## Sistema visual e consistência

| Elemento | Regra adotada | Justificativa |
|---|---|---|
| Tipografia | Inter em 4 pesos (Regular, Medium, Semi Bold, Bold). Texto de leitura entre 14 e 20 px. Peso estimado em 40 px e brinco da conferência em 40 px | [H] Peso e brinco grandes para ler no curral, com sol forte |
| Cores | Verde escuro (#1B6E33) para ação principal e sucesso, fundo off-white, cards brancos, texto quase preto, cinza escuro para apoio, vermelho (#B3261E) para erro e para "Desistir" | [H] Alto contraste. Verde e vermelho sempre vêm com texto ou ícone, não só cor |
| Componentes | 5 componentes locais: Botão/Primário, Botão/Secundário, Campo de texto, Tag/Classe de peso e Card/Item de histórico | Mesmo botão, campo e card em todas as telas |
| Feedback | Carregando (F01L), sucesso (F02S, F05), cancelado (F05D), erro de processamento (F02E), erro de entrada (F02A, F02N) e confirmação (F02C), cada um com ícone, cor e texto | O usuário sempre sabe o estado, e cada erro diz o que fazer |
| Navegação | Barra inferior Pesar/Histórico em todas as telas e "Desistir" no mesmo lugar (canto superior direito) durante a pesagem | Saída sempre no mesmo lugar |

[F] Cabeçalho e barra de navegação foram montados em cada tela e não são componentes. Se mudar um, tem que mudar em todas as 19 telas.

[F] Os botões desabilitados ficam em cinza, sem contraste mínimo, de propósito.

## Verificação de acessibilidade básica

[F] O produto é mobile (smartphone). A verificação usa como referência as recomendações de contraste, tamanho de alvo e texto da WCAG, e não os critérios de teclado.

| Critério | Resultado | Observação |
|---|---|---|
| Contraste do texto | [H] Passa | Cálculo à mão: verde sobre branco ≈ 6:1, vermelho sobre branco ≈ 6:1, cinza de apoio sobre o fundo ≈ 7:1. Confirmar com um plugin de contraste |
| Tamanho dos alvos de toque | 🟨 Em parte | Botões principais entre 48 e 56 px, linhas da lista do lote com 92 px, abas da barra com 64 px. "Trocar foto", "Escolher o animal pelo lote" e "Desistir" ficam abaixo de 48 px |
| Tamanho do texto | 🟨 Em parte | Textos de apoio de 11 a 13 px (por exemplo, "últ. estimativa", a escala 0–300 e a legenda da faixa) podem ser difíceis de ler ao sol |
| Cor não é o único sinal | [H] Passa | Erro, sucesso e cancelamento têm ícone e texto |
| Texto alternativo | Não se aplica | Protótipo sem leitor de tela |

[F] A F02 concentra muita informação (peso, faixa, identificação e dois botões) para caber sem rolar. É o primeiro ponto a observar nos testes.

[?] Nada disso foi testado em celular de verdade nem com usuários. Isso fica para a Entrega 14.

## Interação simulada x funcionalidade real

[F] Tudo no protótipo é simulado. O app não chama o modelo do TCC nem grava dados.

- A **foto** do animal é um desenho de placeholder.
- O **peso (214 kg), a margem (± 20 kg), os brincos, os lotes, os nomes e as datas** são exemplos inventados.
- Na F01, tocar na área da foto já leva à F01B com "Macho" selecionado. Os botões de sexo não alternam.
- A F01L passa sozinha para o resultado depois de 1,5 s.
- Na F02, "Salvar no Histórico" sempre leva ao aviso F02A. Tocar nos campos preenche o animal 117 (F02P).
- O 117 é sempre encontrado e o 999 nunca é. Na lista do lote, só o "Boi 117" é clicável.
- F01C e F02U existem só para entrar nos fluxos de erro.
- [?] O erro de cerca de 20 kg da estimativa e a falta de teste em gado brasileiro (dataset de Bangladesh) são o limite técnico do que a tela promete.

## Checklist

- [ ] Link do Figma está acessível. *(falta liberar em Share → "Anyone with the link" e testar em janela anônima)*
- [ ] Há screenshots representativos no repositório. *(falta subir os 19 PNGs exportados do Figma para `assets/11_figma/`)*
- [ ] Todos os MoLIC relevantes estão cobertos. *(o M01 está coberto por inteiro. Os outros integrantes ainda não fizeram o MoLIC deles)*
- [x] Estados de erro, feedback e recuperação foram prototipados.
- [x] Terminologia/signos são consistentes com Entrega 9.
- [x] Componentes equivalentes se comportam de forma consistente.
- [x] Fluxos críticos são clicáveis do início ao fim.
- [x] O protótipo está pronto para inspeção e testes, sem "links mortos" nas tarefas avaliadas.
- [x] Dashboards, relatórios, históricos, filtros, administração e CRUDs presentes possuem justificativa rastreável.
- [x] Estados de vazio, processamento, erro e recuperação foram considerados quando pertinentes.
- [x] Resultados técnicos são apresentados de forma interpretável para o perfil de usuário.
- [x] A equipe distingue no protótipo o que é interação simulada e o que é funcionalidade técnica realmente integrada, quando necessário.
