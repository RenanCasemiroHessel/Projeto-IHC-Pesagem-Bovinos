# Matriz de rastreabilidade de IHC

A matriz deve ser atualizada ao longo do semestre. Ela ajuda a demonstrar que a interface não surgiu arbitrariamente e registra **como o conhecimento da equipe evoluiu**.

Para projetos cujo TCC não previa interface, esta matriz é especialmente importante: deve ficar visível a passagem da **contribuição técnica do TCC** para um **cenário de uso plausível**, e desse cenário para as decisões de interação.

## 1. Derivação do escopo de IHC a partir do TCC

| Elemento | Registro da equipe | Evidência/justificativa | Estado |
|---|---|---|---|
| Tema do TCC | Estimativa não invasiva do peso de bovinos leves (até 250 kg) utilizando Visão Computacional | TCC 1 (Entrega 1, seções 0.2 e 1.3) | definido |
| Resultado técnico esperado | Sistema de estimativa de peso por imagem: segmentação (YOLO), medidas morfométricas e regressão (CNN ResNet18), acessado por aplicativo móvel | TCC 1 (Entrega 1, seção 0.4) | definido |
| O TCC previa interface? | sim | App com 4 telas previsto no TCC 1: login/cadastro, cadastro do fazendeiro, captura de fotos e dashboard/histórico (Entrega 1, seção 0.5) | definido |
| Capacidade/contribuição central | Estimar o peso de bovinos leves a partir de uma foto, sem balança | Resultados do TCC 1: MAE ~20,75 kg e ~48% dos casos dentro de ±10% (Entrega 1, seção 4.6) | definido |
| Possíveis beneficiários/stakeholders | Pecuarista (usuário direto); técnico agropecuário (usuário secundário possível); frigorífico/comprador e veterinário (recebem informação, não usam a interface) | Hipótese da equipe (Entrega 1, seção 2). Papel do técnico em H05 | H |
| Usuário escolhido para IHC | Pecuarista | Decisão da equipe (Entrega 1, seção 7.2). Quem faz a captura em campo ainda é lacuna, ligada a H01 | H |
| Objetivo principal do usuário | Obter o peso estimado de um bovino específico de forma rápida, sem balança, associado ao animal certo no histórico e entendendo que é uma estimativa | Decisão da equipe; que seja objetivo real do produtor é hipótese (Entrega 1, seção 7.3) | H |
| Contexto de uso adotado | Curral ou pasto, smartphone pessoal do produtor ou peão, com sol forte, poeira, mãos sujas, conexão instável e animal em movimento | Hipótese da equipe (Entrega 1, seções 5.1 a 5.3). Só a posse de celular tem fonte: PNAD Contínua TIC 2024, IBGE | H |
| Interface/recorte de IHC | Fluxo de captura de foto, identificação do animal e visualização do peso estimado (telas 3 e 4 do app previsto) | Deriva do app previsto no TCC 1 e das atividades A01 e A02 (Entrega 1, seção 7.1) | proposta |
| Relação com o TCC | parte prevista, aprofundada na disciplina | Entrega 1, seção 7.5 | definido |

> Se o escopo de IHC mudar ao longo do semestre, preserve a decisão anterior no histórico e registre **qual evidência motivou a mudança**.

## 2. Registro de hipóteses e lacunas da Entrega 1

Use esta tabela para itens importantes marcados como `[H]` ou `[?]`. Preserve o histórico: não apague uma hipótese refutada.

| ID | Afirmação / dúvida inicial | Tipo | Por que importa | Como/onde investigar | Evidência obtida | Estado atual | Impacto no projeto |
|---|---|---|---|---|---|---|---|
| H01 | Quem faz a captura em campo (produtor ou peão) consegue usar o app sozinho nas condições de campo (sol forte, poeira, mãos sujas, sinal instável) | H | Se a interação não funcionar nessas condições, o app não resolve o problema real, mesmo com um modelo preciso | Entrega 3 / 7 / 14 | PENDENTE | aberta | Alimenta requisitos de uso em campo e tarefas de teste |
| H02 | A forma de mostrar a incerteza da estimativa muda a confiança do produtor no resultado. Mostrar a margem de erro pode aumentar ou diminuir essa confiança, dependendo de como for mostrada | H | O TCC tem MAE de ~20,75 kg. Se a interface esconder isso, o produtor pode decidir errado. Se comunicar mal, pode desconfiar do app inteiro | Entrega 7 / 13 | PENDENTE | aberta | Influencia como o peso estimado é apresentado e os critérios de avaliação |
| H03 | O produtor quer acompanhar a evolução do peso do animal ao longo do tempo e não só o último registro de peso | H | Define se histórico e comparação de evolução continuam no recorte principal | Entrega 2 / 3 | PENDENTE | aberta | Pode manter ou tirar histórico e comparação do recorte (atividade A03) |
| H04 | Uma única foto (single-view) é suficiente para a captura em campo sem gerar frustração por foto rejeitada ou mal enquadrada | H | O TCC valida single-view tecnicamente, mas não valida a facilidade de capturar a foto em condições reais de curral | Entrega 6 / 14 | Parcial: o TCC 1 mostra que uma foto basta tecnicamente (diferença de 0,04 kg de MAE). Captura em campo: PENDENTE | aberta | Define se o fluxo pede uma foto ou orientação de captura |
| H05 | O técnico agropecuário usaria o mesmo app que o pecuarista ou precisaria de uma visão/acesso diferente. Também falta saber se ele é usuário secundário ou só stakeholder | H | Afeta se o escopo precisa de perfis/permissões | Entrega 2 | PENDENTE | aberta | Mantém ou tira perfis/permissões do escopo |

## 3. Rastreabilidade entre contribuição técnica, necessidades e artefatos

| ID | Capacidade do TCC utilizada | Necessidade/problema | Persona | Cenário problema | Objetivo/tarefa | HTA/GOMS/CTT | Cenário de interação / signos | MoLIC | Tela(s) Figma | Heurística / problema | Tarefa no teste | Decisão/melhoria |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| R01 | {{ex.: recomendação de otimização}} | {{...}} | {{P01}} | {{C01}} | {{T01}} | {{links}} | {{...}} | {{M01}} | {{F01...}} | {{V01 ou —}} | {{UT01}} | {{...}} |
| R02 |  |  |  |  |  |  |  |  |  |  |  |  |

## 4. Rastreabilidade de padrões de interface

Use esta tabela quando o projeto incorporar padrões como dashboard, relatório, histórico, filtros ou administração. O objetivo é **justificar o padrão**, não apenas listar telas.

| ID da tela/fluxo | Padrão de interface | Objetivo/tarefa que justifica | Informação/ação principal | Evidência de necessidade | Artefatos relacionados |
|---|---|---|---|---|---|
| F01 | dashboard | {{T01}} | {{...}} | {{H01/evidência...}} | {{C01/M01}} |
| F02 | histórico com filtros | {{T02}} | {{...}} | {{...}} | {{...}} |
| F03 | administração/CRUD | {{T03}} | {{...}} | {{...}} | {{...}} |

## 5. Registro de mudanças de escopo

| Data | O que mudou | Evidência/feedback que motivou | Artefatos afetados | Responsável |
|---|---|---|---|---|
| 06/10/2026 | Revisão da Entrega 1: separação entre fato, hipótese e decisão da equipe; usuário direto e stakeholders esclarecidos; possibilidades de interface tratadas como hipóteses | Feedback do professor sobre a Entrega 1 | Entrega 1 | Rafael |

## Como usar

- Use identificadores estáveis (`H01`, `P01`, `C01`, `T01`, `M01`, `F01`, `UT01`).
- Quando uma necessidade/problema tiver origem em hipótese da Entrega 1, cite o ID correspondente.
- Em TCC sem interface original, pelo menos uma linha deve mostrar claramente **como uma capacidade técnica chega até uma tarefa de usuário e uma tela/fluxo**.
- Uma linha pode se desdobrar quando um objetivo possui múltiplos caminhos.
- Não force relação inexistente: se algo ainda não foi modelado, marque `PENDENTE`.
- Ao remover uma funcionalidade, registre a decisão em vez de apagar silenciosamente o histórico.
- Dashboard, CRUD, filtros e relatórios só devem aparecer quando houver objetivo/tarefa que os justifique.
