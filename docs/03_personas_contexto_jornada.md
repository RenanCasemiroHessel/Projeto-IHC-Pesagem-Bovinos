# Entrega 3 — Personas, mapa de empatia, contexto de uso e jornada

**Data:** 08/09/2026 
**Status:** 🟨 em andamento
**Responsabilidade:** 1 persona por integrante; 1 mapa de empatia, 1 contexto de uso consolidado e 1 jornada por equipe (salvo orientação diferente do docente).

## Objetivo da atividade

Representar grupos de usuários de forma útil para decisões de design. Persona não é personagem decorativo: suas características devem alterar requisitos, prioridades, linguagem, fluxos ou critérios de avaliação.

## Atenção a projetos técnicos

Em TCCs sem interface original, a persona pode representar um **profissional que se apropria da contribuição técnica**: DBA, analista, cientista de dados, administrador, pesquisador, técnico, operador, gestor ou especialista de domínio.

Não escolha um perfil apenas porque “parece combinar” com a tecnologia. Explique **qual objetivo esse perfil teria e qual parte da contribuição do TCC produziria valor para ele**. Se ainda for hipótese, mantenha como hipótese/proto-persona a validar.

Também considere papéis diferentes quando houver tarefas distintas, por exemplo:

- operador que executa análises;
- administrador que configura e gerencia permissões;
- especialista que interpreta resultados;
- gestor que consulta relatórios e decide;
- auditor que revisa histórico.

## Entradas da Entrega 1

Antes de criar personas, retome os tipos de usuários, características relevantes, objetivos e hipóteses registradas na Entrega 1. A persona **não deve transformar uma hipótese inicial em fato por meio de uma história fictícia**.

| Item da Entrega 1 | Status inicial | Evidência disponível agora | Como será tratado nesta entrega |
|---|---|---|---|
| Usuário direto = pecuarista | H | Nenhuma entrevista realizada ainda; hipótese consolidada nas discussões da equipe | Incorporada como base de P01, mantida como hipótese |
| Perfil secundário = técnico agropecuário | H | Idem | Incorporada como base de P02, mantida como hipótese |
| Balança de tronco custa R$30-50 mil, por isso produtor pesa só 2-4x/ano | F (fonte: pesquisa de mercado da Entrega 1/2) | Confirmada pela análise de concorrência (C01/C02/C03) | Incorporada como dor de P01 |
| Contexto de uso: curral/pasto, sol forte, poeira, mãos sujas, conexão instável | H | Consolidado por observação/senso comum do domínio, sem validação de campo | Mantida como hipótese, base da seção 3 |
| Vocabulário: arroba, brinco, lote, estilo WhatsApp | H | Baseado em conhecimento geral do setor pecuário brasileiro | Incorporada nos requisitos de linguagem das personas |
| Multi-usuário/permissões fora de escopo (decisão da Entrega 1) | F (decisão de equipe) | Registrada na delimitação de escopo | Usada para **não** dar a P02 recursos de gestão multi-propriedade nesta versão |


## 1. Personas

### Persona P01 — Chico Bento

**Autor(a):** Rafael Takahagi Mendes - 22.126.084-7 
**Tipo:** primária
**Base de evidências:** proto-persona a validar
**Hipóteses da Entrega 1 relacionadas:** H01 (usuário é o pecuarista)

![Persona P01](../assets/03_personas/persona_p01.svg)

| Campo | Descrição |
|---|---|
| Faixa etária / contexto relevante | [H] 45-62 anos — faixa etária predominante entre proprietários de pequenas/médias propriedades de gado no Brasil | |
| Ocupação/papel | [H] Pecuarista, dono de propriedade de pequeno/médio porte, cria gado de corte leve (até 250 kg) |
| Conhecimento do domínio | [F] Alto — décadas de experiência prática em manejo de gado; reconhece peso "no olho" mas sabe que erra |
| Experiência tecnológica | [H] Baixa/média — usa WhatsApp, câmera do celular e aplicativos de seu meio; pouca paciência com telas com muitos passos ou textos longos |
| Objetivos | [H] Acompanhar peso do lote com mais frequência para vender no ponto certo e negociar melhor com frigorífico/comprador |
| Necessidades | [H] Processo rápido, poucos toques, funcionar mesmo com internet ruim no curral |
| Dores/frustrações | [F] Balança de tronco custa R$30-50 mil, inviável para o porte da propriedade; [F] por isso pesa só 2-4x por ano; [H] perde a janela ideal de venda por falta de acompanhamento contínuo |
| Motivadores | [H] Ganho financeiro direto (vender no peso certo), economia de dinheiro (sem comprar balança) |
| Restrições/acessibilidade | [H] Sol forte dificulta enxergar a tela, mãos sujas/molhadas atrapalham toque na tela, pouca familiaridade com termos técnicos de tecnologia |
| Ambiente típico de uso | [H] Curral ou pasto, celular pessoal, animal em movimento, sinal de internet instável |
| Comportamentos relevantes | [H] Confia em recomendação de técnico agropecuário e de outros produtores da região antes de adotar uma ferramenta nova |


**Decisões de design influenciadas por P01:**

- Interface com poucos toques, botões grandes, alto contraste para uso sob sol forte.
- App precisa funcionar (ou tolerar) conexão instável — captura de foto não pode depender de internet em tempo real.
- Vocabulário do domínio (arroba, brinco, lote) em vez de termos técnicos de ML/CV.
- Fluxo prioritário: fotografar → ver peso, sem etapas extras.

### Persona P02 — Dinho
 
**Autor(a):** Gustavo Mendes Franco Lapin Atui — 24.123.072-1
**Tipo:** secundária
**Base de evidências:** proto-persona a validar
**Hipóteses da Entrega 1 relacionadas:** H01 (usuário é o técnico agropecuário)

![Persona P02](../assets/03_personas/persona_p01.svg)

 | Campo | Descrição |
|---|---|
| Faixa etária / contexto relevante | [H] 28–45 anos — técnico agropecuário formado, presta assistência a múltiplas propriedades rurais na região |
| Ocupação/papel | [H] Técnico agropecuário autônomo ou contratado por cooperativa. Visita fazendas periodicamente para orientar manejo e nutrição do rebanho |
| Conhecimento do domínio | [F] Alto — formação técnica em agropecuária; interpreta curva de crescimento, ganho médio diário e indicadores de sanidade animal |
| Experiência tecnológica | [H] Média/alta — usa apps de gestão rural no trabalho, planilhas e WhatsApp para comunicação com produtores, confortável com telas de histórico e relatórios |
| Objetivos | [H] Consultar o histórico de peso dos animais de uma fazenda para avaliar se o ganho diário está dentro do esperado e orientar o produtor sobre manejo, dosagem e momento de venda |
| Necessidades | [H] Acesso rápido ao histórico de pesagens por animal ou por lote, comparativo de evolução de peso ao longo do tempo |
| Dores/frustrações | [H] Produtor frequentemente não tem registro de peso "é no olho mesmo", sem dados históricos, a orientação técnica fica baseada em estimativa visual | 
| Motivadores | [H] Dar recomendações embasadas em dados reais, ajudar o produtor a tomar decisões mais rentáveis, diferenciar seu serviço técnico pela qualidade da análise |
| Restrições/acessibilidade | [H] Usa o app no celular durante a visita à fazenda ou no escritório |
| Ambiente típico de uso | [H] Curral durante a visita técnica ou escritório após a visita, celular próprio ou tablet |
| Comportamentos relevantes | [H] Acessa o histórico de peso antes de cada visita para preparar orientações, compartilha dados com o produtor |
 
**Decisões de design influenciadas por P02:**
 
- Histórico de pesagens por animal deve ser consultável de forma rápida e legível.
- Peso ao longo do tempo é funcionalidade de valor para esse perfil.
- Possibilidade de compartilhar histórico via WhatsApp ou PDF.
- Interface deve funcionar também fora do campo.
 


> Repita para P02, P03... Cada integrante deve produzir ao menos uma persona.

### Síntese das personas

Explique diferenças entre os perfis e qual persona é prioritária. Evite personas duplicadas que só mudam nome/foto.

## 2. Mapa de empatia — equipe

**Persona escolhida:** {{P01}}  
**Justificativa:** {{por que esse perfil é relevante}}

![Mapa de empatia](../assets/03_personas/mapa_empatia.svg)

Documente também em texto: o que vê; ouve; diz/faz; pensa/sente; dores; ganhos. Diferencie **evidência** de **hipótese**.

## 3. Contexto de uso — consolidação

| Dimensão | Descrição | Implicação de design |
|---|---|---|
| Usuários | {{...}} | {{...}} |
| Tarefas | {{...}} | {{...}} |
| Equipamentos | {{...}} | {{...}} |
| Ambiente físico | {{...}} | {{...}} |
| Ambiente social/organizacional | {{...}} | {{...}} |
| Papéis/permissões/governança | {{...}} | {{...}} |
| Volume de dados/histórico | {{...}} | {{...}} |

## 4. Jornada do usuário — equipe

**Persona:** {{P01}}  
**Objetivo da jornada:** {{...}}  
**Início e fim da jornada:** {{...}}

| Etapa | Situação/ação | Objetivo | Pensamento/emoção | Dor | Oportunidade de design | Evidência |
|---|---|---|---|---|---|---|
| 1 | {{...}} | {{...}} | {{...}} | {{...}} | {{...}} | {{...}} |

> A jornada pode incluir etapas **antes, durante e depois** do uso do produto. Não transforme a jornada em lista de telas.

## Síntese

Quais necessidades e objetivos devem obrigatoriamente aparecer nos cenários e nas tarefas seguintes?

## Checklist

- [ ] Existe pelo menos uma persona por integrante.
- [ ] As personas não são apenas diferenças demográficas superficiais.
- [ ] Está claro o que é dado real e o que é hipótese/proto-persona.
- [ ] A persona não “validou por ficção” uma hipótese da Entrega 1; afirmações continuam marcadas como hipótese quando não há evidência.
- [ ] Objetivos e dores têm consequência para o design.
- [ ] Contexto de uso está coerente com a Entrega 1.
- [ ] Em TCC sem interface original, a persona possui relação explícita com a contribuição técnica.
- [ ] Papéis administrativos, técnicos e decisórios só foram criados quando possuem objetivos/tarefas diferentes.
- [ ] Jornada possui etapas, dores e oportunidades e não é apenas wireflow.
- [ ] IDs das personas foram adicionados à rastreabilidade.
