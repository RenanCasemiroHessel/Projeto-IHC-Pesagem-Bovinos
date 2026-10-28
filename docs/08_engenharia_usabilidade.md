# Entrega 8 — Ciclo de vida e engenharia de usabilidade

**Data:** 28/10/2026  
**Status:** 🟨 em andamento  
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
| Contexto de uso | {{...}} | {{...}} | Entregas 1/3 |
| LGPD, se aplicável | {{...}} | {{...}} | {{fonte oficial}} |
| Acessibilidade | {{...}} | {{...}} | {{WCAG/norma aplicável}} |
| {{outro}} | {{...}} | {{...}} | {{...}} |

## 3. Metas de usabilidade

Usabilidade deve ser discutida **no contexto de uso**. Metas quantitativas devem dizer o que será medido, em qual tarefa, com qual população e qual limite será considerado aceitável.

### 3.1 Metas qualitativas

| Meta | Para quem/tarefa | Evidência desejada | Justificativa |
|---|---|---|---|
| {{ex.: compreensão clara da diferença entre X e Y}} | {{...}} | {{fala/observação}} | {{...}} |

### 3.2 Metas quantitativas

| ID | Dimensão | Métrica | Tarefa/escopo | Meta | Como medir | Justificativa |
|---|---|---|---|---|---|---|
| MU01 | eficácia | taxa de conclusão sem ajuda | T01 | ≥ {{x}}% | teste observado | {{...}} |
| MU02 | eficiência | tempo mediano | T02 | ≤ {{tempo}} | cronômetro/log | {{...}} |
| MU03 | satisfação | escala pós-tarefa | T01–T03 | ≥ {{valor}} | questionário | {{...}} |

### 3.3 Priorização das metas (se exigida na disciplina)

Se o professor solicitar porcentagens que somem 100%, trate-as como **peso de prioridade**, não como métrica de usabilidade.

| Meta | Peso de prioridade | Justificativa |
|---|---:|---|
| MU01 | {{...}}% | {{...}} |
| **Total** | **100%** | |

## 4. Como o ciclo será iterado

Explique que artefatos serão revisitados após protótipos e avaliações.

## Checklist

- [ ] Capacidades e restrições têm impacto de IHC explicitado.
- [ ] Está claro o limite entre contribuição técnica do TCC e camada interativa da disciplina.
- [ ] Resultados/processamento simulados no protótipo foram explicitados.
- [ ] Metas de usabilidade avaliam a interação, não substituem métricas técnicas do TCC.
- [ ] Normas/princípios estão contextualizados, não apenas copiados.
- [ ] Metas quantitativas são mensuráveis e associadas a tarefas/público.
- [ ] Eficácia, eficiência e satisfação são consideradas quando pertinentes.
- [ ] Metas poderão ser verificadas nas Entregas 12–14.
