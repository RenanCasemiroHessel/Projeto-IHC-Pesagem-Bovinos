# Entrega 10 — MoLIC

**Data:** 12/11/2026  
**Status:** 🟨 em andamento  
**Responsabilidade:** 1 solução completa por integrante

## M01 — Pesar um animal por foto e salvar o peso no animal certo

**Autor(a):** Rafael Takahagi Mendes — 22.126.084-7  
**Cenário de interação de origem:** CI01  
**Objetivo(s):** O01 (obter o peso estimado de um animal pela foto) e O02 (salvar o peso no animal certo)  
**Tarefa(s) relacionada(s):** T02  
**Signos relevantes:** foto do animal, sexo, peso estimado (kg), peso estimado (@), margem de erro, identificação do animal (brinco ou nome), lote, foto da última pesagem, data da pesagem, situação do salvamento, aviso "boi não reconhecido", aviso "nenhum bovino encontrado"

### Diagrama

![MoLIC M01](../assets/10_molic/molic_m01.svg)

**Fonte editável:** o próprio arquivo `docs/assets/10_molic/molic_m01.svg` (texto editável em qualquer editor de código ou no draw.io).

### Leitura do diagrama

[F] A conversa segue a ordem do CI01 (Entrega 9) e da T02 (Entrega 5): fotografar, ver o peso, identificar o animal, conferir e salvar.

[F] A notação segue as aulas de MoLIC (partes A, B e C): cenas, diálogos, falas do usuário (`u:`) e do preposto (`d:`), acesso ubíquo, gco/gcc, processo do sistema e cena de alerta.

#### Caminho principal

1. A conversa abre no ponto de abertura, com `gco: Pesar um animal por foto`.
2. Cena **Fotografar o animal**: o preposto diz `d: tire uma foto do boi, de lado e inteiro`. O usuário enquadra o animal, escolhe macho ou fêmea e toca em "Estimar peso" (`u: toca em "Estimar peso"`).
3. Processo do sistema **estima o peso pela foto**. Enquanto trabalha, o app mostra "Calculando o peso...". Se reconheceu o boi, responde `d: peso estimado`.
4. Cena **Ler o peso estimado**: o usuário vê o peso em kg e em @ e a margem de erro (cerca de 20 kg para mais ou para menos). Depois diz `u: guardar este peso`.
5. Cena **Identificar o animal**: o usuário digita o número do brinco (`u: é o 117`) ou escolhe o animal no lote, reconhecendo pela foto da última pesagem.
6. Processo do sistema **procura o animal no cadastro**. Se acha, responde `d: encontrei o 117, lote Pasto 2`.
7. Cena **Conferir antes de salvar**: o app mostra brinco e foto bem grandes. O usuário compara com o animal que está à frente e toca em salvar (`u: compara e toca em salvar`).
8. Processo do sistema **grava o peso no animal** e responde `d: peso salvo no boi 117`.
9. Cena **Peso salvo**: o usuário vê boi, lote e data. Ele diz `u: agora o próximo` e a câmera abre pronta para o próximo animal (volta à cena Fotografar), ou `u: terminar de pesar`, que fecha a conversa (`gcc`) e leva ao ponto de encerramento.

[F] O peso aparece sempre como estimativa, com margem de erro, porque o erro médio (MAE) do modelo do TCC é de cerca de 20,75 kg (TCC 1) e mostrar só um número exato passa confiança demais (H02).

[H] A identificação vem depois do peso porque é assim que o Chico trabalha no CI01: ele fotografa o animal que está à frente e só depois diz de qual animal é. A conferência antes de salvar existe por causa do A02: peso no animal errado estraga o histórico daquele animal.

[H] O `u: terminar de pesar` fecha a conversa sobre pesar um animal. Fechar o lote inteiro é outra conversa, que é a T03 (Entrega 5) e não faz parte deste M01.

#### Alternativas e rupturas

| Situação | Onde ocorre | Como o usuário percebe | Caminho de recuperação/saída |
|---|---|---|---|
| Boi não reconhecido (foto cortada, animal se mexeu) | Processo "estima o peso pela foto" | Cena de alerta **Boi não reconhecido**: `d: não reconhecemos o boi. Fotografe de lado, com o corpo inteiro na foto.` Sem peso e sem botão de salvar (MQ03) | `u: tirar outra foto` volta para **Fotografar o animal** |
| Nenhum bovino encontrado | Processo "procura o animal no cadastro" | Cena de alerta **Nenhum bovino encontrado**: `d: não encontrei nenhum bovino com esse número. Confira o número, procure pelo lote ou informe como animal novo.` | `u: corrigir o número ou procurar pelo lote` volta para **Identificar o animal**; `u: informar como animal novo` vai para **Informar animal novo [?]** e, com `u: confirmar os dados [?]`, segue para a conferência |
| Brinco sujo, caído ou ilegível | Cena Identificar o animal | O usuário não consegue ler o número | Em vez de digitar, escolhe o animal na lista do lote, reconhecendo pela foto da última pesagem ou pelo nome (por exemplo, "o pintado"). Não passa por alerta |
| Animal escolhido não é o que está à frente | Cena Conferir antes de salvar | O brinco e a foto grandes não batem com o animal do curral (A02) | `u: não é esse` volta para **Identificar o animal**, sem perder o peso estimado e sem refazer a foto |
| Usuário desiste | Qualquer cena | Não há alerta, ele só quer parar | Acesso ubíquo `u: desistir da pesagem`, que leva ao encerramento. Nada é salvo |

[F] O contexto de uso (curral ou pasto, sol forte, poeira, mãos sujas, animal em movimento) vem da Entrega 3 e explica por que "boi não reconhecido" e "brinco ilegível" precisam de caminho de saída.

[H] O botão de desistir é hipótese. As telas das Entregas 6 e 11 vão confirmar como ele aparece.

[H] Escolher o sexo junto com a foto, antes de estimar, vem da Entrega 9 (signo "sexo"). Ele deixa a estimativa mais perto do peso real.

[?] O caminho do animal novo (como ele entra no app e quais dados são pedidos) continua em aberto desde a Entrega 5. Por isso a cena **Informar animal novo** está marcada com [?].

[?] A regra de conversão do peso vivo para @ ainda precisa ser confirmada com a equipe (Entrega 9).

[?] Falta de sinal e "pendente de envio" ficam fora deste MoLIC. A Entrega 9 deixou essa situação fora do protótipo (Entrega 8), então não foi modelada como cena. Se entrar numa versão futura, precisa de uma cena de alerta própria.

## M02 — Acompanhar a evolução do peso de um animal

**Autor(a):** Gustavo Mendes Franco Lapin Atui — 24.123.072-1  
**Cenário de interação de origem:** CI02 — Recomendação de venda com o histórico de peso  
**Objetivo(s):** O03 Localizar um bovino (pelo número ou pelo lote) · O04 Acompanhar a evolução do peso de um animal · O05 Entender o ganho de peso  
**Tarefa(s) relacionada(s):** T01 Consultar o histórico de peso de um animal (HTA, GOMS e CTT da Entrega 5)  
**Signos relevantes:** número (brinco ou nome), lote, foto, peso estimado (kg), data, nº de estimativas, diferença para a anterior, ganho total

### Diagrama

![MoLIC M02](../assets/10_molic/molic_m02.svg)

**Fonte editável:** [`molic_m02.svg`](../assets/10_molic/molic_m02.svg) ( texto editável em qualquer editor de código ou no draw.io )

### Leitura do diagrama

O diagrama tem duas cenas, uma para cada tópico da conversa: **localizar um bovino** (O03) e **acompanhar a evolução do peso** (O04 e O05). A busca é o processamento do sistema e tem uma fala de recuperação para quando não encontra o animal. O histórico fica guardado no próprio aparelho, então abrir um animal não depende de sinal e não tem falha de carregamento. O peso em @ e o aviso de margem de erro (O06) ficam só na hora da pesagem (M01), e o histórico não os repete.


#### Caminho principal

1. **Ponto de abertura → Localizar um bovino.** O usuário abre o histórico de estimativas, e o sistema mostra os bovinos já pesados, cada um com foto, número, lote, último peso e data.
2. **Localizar um bovino → busca.** Dinho informa o número do brinco (`u: buscar {número}`).
3. **Busca → Acompanhar a evolução do peso.** O sistema encontra o bovino (`d: [número] bovino encontrado`) e mostra o número, o lote e quantas estimativas existem. Em seguida mostra as pesagens com data, foto e peso em kg, a diferença para a pesagem anterior e o ganho total. Assim o técnico não precisa fazer contas (achado da Entrega 5).
4. **Acompanhar a evolução do peso → Localizar um bovino.** Dinho passa ao próximo animal (`u: consultar o próximo animal`). A busca anterior continua na tela, o que permite avaliar o lote inteiro sem recomeçar (CI02).
5. **Acompanhar a evolução do peso → encerramento.** Com os números de todo o lote, Dinho encerra a consulta e conversa com o Chico sobre a venda, que acontece fora do sistema.

- **Busca pelo lote.** Quando o brinco está sujo, Dinho busca pelo lote (`d: [lote] mostrar bovinos do lote`). A conversa volta para a mesma cena com a lista filtrada, e ele reconhece o animal pela foto (`d+u`).
- **Escolha direta na lista.** O usuário pode tocar num bovino da lista sem buscar.

#### Alternativas e rupturas

| Situação | Onde ocorre | Como o usuário percebe | Caminho de recuperação/saída |
|---|---|---|---|
| Nenhum bovino com o número digitado (brinco lido errado ou animal nunca pesado) | Processamento *busca*, a partir de *Localizar um bovino* | `d: Não encontrei nenhum bovino com esse número. Confira o número ou procure pelo lote.` | Fala de recuperação de volta a *Localizar um bovino*, com a busca ainda preenchida para corrigir. Outra saída é buscar pelo lote. |
| Brinco ilegível no curral | *Localizar um bovino* | O próprio usuário percebe que não consegue ler o número | Busca pelo lote e reconhecimento pela foto (`d+u: reconhecer o animal pela {foto}`) |
| Animal com uma só estimativa | *Acompanhar a evolução do peso* | `d: Este animal tem 1 estimativa. O ganho de peso aparece a partir da segunda pesagem.` | Não é um erro. A cena mostra o peso e a data, e o usuário passa para o próximo animal. |

### Checklist específico de modelagem

- [] Existe **ponto de abertura** coerente com o início do objetivo.
- [] As **cenas de conversa** representam tópicos/assuntos, não nomes de páginas apenas.
- [] As transições/falas deixam claro o que o usuário ou o sistema comunica.
- [] Há **ponto(s) de encerramento** para objetivos concluídos/abandonados quando aplicável.
- [] Processamentos do sistema estão representados conforme a notação adotada em aula, sem "inventar" fala do usuário.
- [] Rupturas (breakdowns) relevantes têm feedback e caminho de recuperação, não becos sem saída.
- [] Acessos ubíquos/atalhos só aparecem quando semanticamente justificáveis (só "desistir da pesagem", marcado como [H]).
- [] O diagrama cobre caminhos alternativos importantes, e não apenas o "happy path".
- [] Nomes de objetivos, tópicos e signos são coerentes com a Entrega 9.
- [] O diagrama é legível em tamanho normal no GitHub.
- [] O MoLIC representa a conversa usuário–sistema, não o fluxo interno do algoritmo.
- [] Processamento, filtros, administração, relatórios e históricos incluem retornos/rupturas quando relevantes.

## Consolidação da equipe

### Cobertura dos objetivos

| Objetivo | MoLIC que cobre | Lacunas/duplicidades | Decisão |
|---|---|---|---|
| O01 | M01 | Nenhuma | Coberto no M01: fotografar, voltar quando o boi não é reconhecido, ler o peso e a margem de erro |
| O02 | M01 | [?] O caminho do animal novo continua em aberto | Coberto no M01: identificar, conferir e salvar, com a fala "nenhum bovino encontrado" |
| O03 | M01 (só a identificação antes de salvar) | [?] "Identificar pelo brinco ou pelo lote" (O02a e O02b) pode virar o mesmo O03, para não ter dois nomes para a mesma ação (Entrega 9) | Definir na consolidação da equipe |
| O06 | M01 (na hora da pesagem) | O histórico não repete o aviso de margem de erro (Entrega 9) | Coberto no M01 pela cena Ler o peso estimado |
| O07 Localizar um bovino | M02 | O M01 chama a mesma ação de "Identificar o animal", com a mesma ruptura "Nenhum bovino encontrado". O aviso de nenhum bovino encontrado não existe nas telas da Entrega 6 | Manter um único nome: "Localizar um bovino" |
| O08 Acompanhar a evolução do peso | M02 | O encerramento da consulta não tem tela própria na Entrega 6 | Decidir no Figma como mostrar o encerramento |
| O09 Entender o ganho de peso | M02 (dentro da cena O04) | Animal com uma só estimativa não tem ganho para mostrar, e a Tela 4 não previa esse caso | Não virou cena própria, porque o ganho aparece junto das pesagens |

### Preparação para o Figma

Estados/telas que saem da conversa do M01:

- **Fotografar o animal**: guia de enquadramento (de lado, corpo inteiro), escolha de macho ou fêmea e botão "Estimar peso" (Tela 1 da Entrega 9).
- **Calculando o peso**: estado de espera, para evitar toque duplo.
- **Boi não reconhecido**: aviso, sem peso e sem botão de salvar, com o botão "Tirar outra foto" (Tela E1).
- **Ler o peso estimado**: peso em kg e em @, margem de erro e botão para guardar o peso.
- **Identificar o animal**: campo de brinco com teclado numérico grande e lista do lote com a foto da última pesagem.
- **Nenhum bovino encontrado**: aviso com os caminhos de corrigir o número, procurar pelo lote ou informar como animal novo.
- **Informar animal novo [?]**: depende da decisão em aberto.
- **Conferir antes de salvar**: brinco e foto grandes, com "Salvar 214 kg no boi 117, lote Pasto 2?" e as opções de salvar ou "Não é esse".
- **Peso salvo**: confirmação com boi, lote e data, com os botões para o próximo animal e para terminar.
- **Desistir da pesagem [H]**: ação disponível em qualquer tela. A forma de mostrar fica para o Figma.

Estados/telas que saem da conversa do M02:

- **Localizar um bovino**: lista dos bovinos já pesados, cada um com foto, número do brinco, lote, último peso e data, e campo de busca por número ou lote. Tocar num bovino da lista abre o histórico dele sem buscar (Tela 3 da Entrega 6).
- **Lista filtrada pelo lote**: a mesma lista, só com os animais do lote buscado, para reconhecer o animal pela foto quando o brinco está sujo ou ilegível (Tela 3, filtrada).
- **Nenhum bovino encontrado**: aviso "Não encontrei nenhum bovino com esse número. Confira o número ou procure pelo lote.", com a busca ainda preenchida para corrigir o número e o caminho para procurar pelo lote (nova).
- **Acompanhar a evolução do peso**: número, lote e quantidade de estimativas do animal; pesagens com data, foto e peso em kg; diferença para a pesagem anterior e ganho total já calculados, para o técnico não fazer contas. Botão "← Todos os bovinos" para o próximo animal, com a busca anterior mantida (Tela 4 da Entrega 6).
- **Histórico com 1 estimativa**: peso e data da única pesagem, com o aviso "Este animal tem 1 estimativa. O ganho de peso aparece a partir da segunda pesagem." Não é tela de erro (nova, variação da Tela 4).
- **Encerrar a consulta**: o usuário termina depois de ver o lote inteiro. A forma de mostrar fica para o Figma.
