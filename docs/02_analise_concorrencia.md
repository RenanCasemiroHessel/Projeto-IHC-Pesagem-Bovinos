# Entrega 2 — Público-alvo e análise de concorrência

**Data:** {{26/08/2026}}  
**Status:** 🟨 em andamento  
**Responsabilidade mínima:** cada integrante analisa pelo menos 1 concorrente/interface representativa; a equipe produz síntese comparativa.

## Objetivo da atividade

Compreender soluções do mesmo domínio **e também interfaces familiares ao público-alvo**. O objetivo não é copiar telas, mas identificar convenções, padrões, affordances percebidas, problemas recorrentes, expectativas e oportunidades de design.

> **Concorrente não precisa ser idêntico ao produto.** Pode atuar na mesma área, resolver objetivo semelhante ou disputar a mesma necessidade. Quando não houver concorrente direto, use produtos análogos e softwares que o público já utiliza.

### Para TCCs que não previam interface

Não procure apenas um “concorrente do algoritmo”. Investigue **interfaces profissionais que materializam atividades semelhantes** às que o usuário escolhido precisaria realizar.

Exemplos:

- TCC de banco de dados → consoles de administração, ferramentas para DBA, monitoramento e análise de consultas;
- TCC de LLM/ML → painéis de experimentos, gestão de modelos/datasets, comparação de métricas, revisão de resultados;
- TCC de análise de dados → dashboards, ferramentas de BI, filtros, relatórios e exploração;
- TCC de infraestrutura/API → portais administrativos, observabilidade, logs, gestão de credenciais e uso;
- TCC de cibersegurança → consoles de alertas, triagem, histórico e auditoria.

A pergunta é: **“que convenções esse perfil já conhece para executar tarefas equivalentes?”**

## Entrada obrigatória da Entrega 1

Retome o mapa inicial de alternativas e produtos citado na Entrega 1. Aqui a equipe deixa de trabalhar apenas com impressão inicial e passa a **investigar sistematicamente** cada solução.

| Software | Tipo | Por que foi citado | Status inicial | Decisão nesta entrega |
|---|---|---|---|---|
| Cattle Weight AI | concorrente | concorrente direto com funcionalidades semelhantes | F  | analisar C01 |
| Olho do dono | concorrente | funcionalidades diferentes mas voltado para o mesmo público | F  | analisar C02 |

Se uma hipótese da Entrega 1 for confirmada ou refutada durante esta análise, atualize `H01`, `H02`... em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md).

## 1. Público-alvo desta análise

O público alvo da análise segue sendo o mesmo da entrega 1. Pecuaristas de corte pequeno e médio porte, trabalhadores de campo. Que precisam estimar o peso do gado sem uma balança própria, além de veterinários e técnicos que acompanham o ganho de peso do rebanho.

## 2. Concorrentes diretos/indiretos

### Análise C01 — Cattle Weight AI

**Autor(a):** Gustavo Mendes Franco Lapin Atui — 24.123.072-1  
**Tipo:** direto 
**Link oficial:** https://play.google.com/store/apps/details?id=com.tlt.androidapps.cattlewt&hl=pt_BR  
**Data de acesso:** 26/08/2026

### Análise C02 — Olho do dono

**Autor(a):** Renan Casemiro Hessel — 24.123.019-2  
**Tipo:** direto 
**Link oficial:** https://olhododono.agr.br/ 
**Data de acesso:** 02/09/2026

#### Contexto e proposta

C01 - O concorrente Cattle Weight AI utiliza visão computacional e inteligência artificial para estimar e acompanhar o ganho de peso do animal (bovíno) através de fotos tiradas pelo celular.

C02 - O concorrente Olho do Dono é uma empresa que desenvolveu um equipamento portátil e com tecnologia própria que permite o produtor a acompanhar e realizar pesagem do rebanho de maneira remota, apenas com uma câmera instalada no curral.

#### Funcionalidades relevantes

| Funcionalidade | Como é realizada | Evidência/print | Observação de IHC |
|---|---|---|---|
| C01 | Estimar o peso através de fotos tiradas dentro do aplicativo, acompanhamento de pesagem através de um histórico (por animal) |  ![Imagem Cattle Weight AI](assets/02_concorrencia/evidencia_Cattle_weight.webp) | O usuário tira uma foto através do aplicativo, onde a IA estima o peso do animal, salvando o resultado no histórico de pesagem| {{...}} |
| C02 | Pesagem do animal em tempo real, podendo ser vista de forma remota sem estar presente através do aplicativo desenvolvido por eles |  ![](assets/02_concorrencia/...) | O animal passa por um corredor no curral aonde a câmera está posicionada, o usuário tem acesso ao peso do animal através do aplicativo, onde é possível ver em tempo real o animal passando e o dispositivo predizendo o peso | {{...}} |


#### Experiência do usuário e opiniões

Use avaliações públicas, relatos, estudos, testes próprios ou outra fonte identificável. Não trate opinião isolada como verdade universal.

#### Preço/modelo de negócio

{{...}}

#### Padrões e tendências percebidos

{{...}}

#### Pontos positivos, limitações e lições

| Ponto | Evidência | Implicação para nosso projeto |
|---|---|---|
| {{...}} | {{...}} | {{...}} |

> Repita a subseção para C02, C03... até atender à quantidade da equipe.

## 3. Softwares que o público-alvo usa no cotidiano

Analise interfaces que moldam a expectativa do público, mesmo que não sejam concorrentes.

| Software | Por que o público usa | Padrões relevantes | Prints | O que aprender |
|---|---|---|---|---|
| {{...}} | {{...}} | {{...}} | {{link local}} | {{...}} |

## 3.1 Padrões de interface relevantes ao escopo de IHC

Registre somente padrões encontrados nas soluções analisadas e que possam ter relação com objetivos reais da equipe.

| Padrão observado | Produto(s) | Para qual tarefa serve | Vantagem percebida | Risco/limitação | Aplicável ao nosso escopo? |
|---|---|---|---|---|---|
| dashboard | {{...}} | {{...}} | {{...}} | {{...}} | sim/não/talvez |
| relatório | {{...}} | {{...}} | {{...}} | {{...}} | {{...}} |
| histórico + filtros | {{...}} | {{...}} | {{...}} | {{...}} | {{...}} |
| administração/CRUD | {{...}} | {{...}} | {{...}} | {{...}} | {{...}} |
| comparação de resultados | {{...}} | {{...}} | {{...}} | {{...}} | {{...}} |

> O objetivo não é concluir “todo concorrente tem dashboard, então teremos um”. O padrão só será adotado se apoiar uma tarefa rastreável.

## 4. Síntese comparativa da equipe

| Critério | C01 | C02 | C03 | Oportunidade para o projeto |
|---|---|---|---|---|
| Navegação |  |  |  |  |
| Feedback/estado |  |  |  |  |
| Prevenção/recuperação de erro |  |  |  |  |
| Terminologia |  |  |  |  |
| Acessibilidade |  |  |  |  |
| Eficiência |  |  |  |  |

## 5. Recomendações derivadas

Liste recomendações com origem explícita.

- **RC01:** {{recomendação}} — derivada de {{C01/C02/evidência}}.
- **RC02:** {{...}}

## Referências

{{fontes dos produtos, avaliações e literatura}}

## Checklist

- [ ] O mapa inicial de alternativas da Entrega 1 foi revisitado e aprofundado.
- [ ] Hipóteses relevantes sobre mercado/padrões foram atualizadas na rastreabilidade quando surgiram evidências.
- [ ] Há pelo menos uma análise completa por integrante.
- [ ] Cada análise contém prints legíveis da interface.
- [ ] Prints mostram telas/estados relevantes, não apenas logos/homepage.
- [ ] Foram analisados concorrentes e/ou interfaces representativas ao público.
- [ ] Em TCC sem interface original, foram investigadas ferramentas profissionais análogas às atividades do usuário escolhido.
- [ ] Padrões como dashboard, relatório, filtros e CRUD foram analisados como soluções para tarefas, não como requisitos automáticos.
- [ ] Opiniões de UX têm fonte.
- [ ] A síntese compara critérios comuns e produz recomendações.
- [ ] Não há “copiar porque o concorrente faz”; há justificativa de adequação ao público/contexto.
