---
stepsCompleted: [1, 2, 3, 4, 5, 6, 7]
inputDocuments: ["docs/project-context.md"]
project: "O Jogo do Dono"
author: "William"
date: "2026-05-27"
---

# UX Design Specification — O Jogo do Dono

**Autor:** William
**Data:** 27/05/2026

---

<!-- UX design content will be appended sequentially through collaborative workflow steps -->

## Executive Summary

### Project Vision

O Jogo do Dono é uma jornada empresarial gamificada de 7 dias. O participante paga R$297, executa missões reais dentro da própria empresa, diagnostica gargalos e, ao final, desbloqueia o Passaporte GI — direito de comprar o Gestão de Impacto em condição exclusiva. A conversão não é empurrada: o empresário se convence sozinho ao longo do jogo. O site não é uma área de membros — é um painel de missão empresarial.

### Target Users

Donos de empresa e empresários de pequeno e médio porte. Perfil:
- Acesso majoritariamente mobile, em momentos de pausa (entre reuniões, à noite)
- Muitos com pouca fluência digital — precisam entender o que fazer em menos de 3 segundos
- Ego presente: não querem parecer perdidos ou lentos
- Motivados por resultado prático, não por conteúdo ou aprendizado passivo
- Respondem a pressão, tensão e senso de consequência, não a motivação

### Key Design Challenges

1. **Retenção por 7 dias sem notificação agressiva** — A tensão deve ser criada pelo próprio design: missão bloqueada gera curiosidade, missão atrasada gera culpa, missão concluída gera orgulho.
2. **Formulários que não parecem formulários** — Os campos coletam dados estratégicos para o closer, mas precisam parecer reflexão empresarial, não pesquisa ou burocracia.
3. **Desbloqueio como ritual** — O momento em que uma nova missão abre precisa ter peso visual e emocional. Não é uma notificação — é uma conquista.

### Design Opportunities

1. **Dashboard como espelho competitivo** — O participante vê seu progresso em relação ao ranking e sente: "estou 3 dias atrás". Isso o puxa de volta organicamente.
2. **Copy que fala com ele, não para ele** — "Você está evitando encarar o Cofre" é mais poderoso que "Complete o Dia 1". O sistema precisa parecer que sabe o que o empresário está evitando.
3. **Mobile bottom bar sempre visível** — Um botão de ação principal fixo na parte inferior. O usuário leigo nunca fica perdido ou sem saber o próximo passo.

## Core User Experience

### Defining Experience

O loop central do produto: o empresário abre o app/site, vê a missão do dia desbloqueada, sente a pressão de executar, responde as perguntas, envia evidência e clica em "Concluir Missão". Esse ciclo acontece 8 vezes (Dia 0 a Dia 7). Tudo no produto existe para facilitar esse loop ou criar tensão que leva de volta a ele.

### Platform Strategy

- **React Native** para iOS e Android — código compartilhado, publicação nas duas lojas
- **Web responsivo** para acesso via browser (desktop e mobile)
- Câmera nativa no app para upload de evidência (máximo 3 toques)
- Notificações push no app para lembrete diário da missão
- Sem necessidade de offline — mas progresso salvo automaticamente a cada campo preenchido
- Layout projetado mobile-first, adaptado para desktop

### Effortless Interactions

1. **Encontrar a missão do dia** — dashboard mostra isso acima de qualquer outra informação, sem rolagem
2. **Responder as perguntas** — campos grandes, progressão clara, salvamento automático
3. **Enviar evidência** — no app: câmera abre direto, foto tirada, enviada. Máximo 3 toques
4. **Saber o próximo passo** — após concluir, mensagem imediata + indicação do próximo desbloqueio

### Critical Success Moments

| Momento | O que precisa acontecer |
|---|---|
| **Primeiro acesso** | Ritual de abertura — o empresário sente que entrou em algo sério, não em mais um curso |
| **Desbloqueio do Dia 1** | Animação + mensagem provocativa — primeira recompensa do jogo, cria expectativa |
| **Conclusão da primeira missão** | Feedback imediato "missão registrada" — instala o hábito de voltar |
| **Dia 5 — A Caçada** | Resultado comercial real em 24h — se gerar dinheiro, o Passaporte GI vende sozinho |
| **Desbloqueio do Passaporte GI** | Maior momento emocional do produto — peso visual máximo, copy definitivo |

### Experience Principles

1. **Missão primeiro, tudo depois** — a missão do dia é sempre o elemento mais visível de qualquer tela
2. **Tensão sem pressão agressiva** — urgência criada por ausência (missão bloqueada, prazo visível), não por popup
3. **Cada clique tem consequência** — o sistema reage a toda ação com feedback visual e copy alinhado ao tom
4. **Mobile é o campo de batalha** — nenhuma funcionalidade crítica depende de desktop
5. **O formulário é a missão** — preencher não é burocracia, é executar. O design reforça isso em cada campo

## Desired Emotional Response

### Primary Emotional Goals

O participante não deve se sentir motivado — deve se sentir **desconfortável de forma produtiva**. O app revela verdades que ele estava evitando. Ao concluir, a emoção dominante é: *"Agora eu não tenho mais desculpa."*

### Emotional Journey Mapping

| Dia | Emoção-alvo | Como o design provoca |
|---|---|---|
| 0 — Raio-X | Choque + compromisso | Campos diretos sem filtro, sem lugar para escapar |
| 1 — O Cofre | Dor financeira | Copy que nomeia a perda sem suavizar |
| 2 — O Espelho | Desconforto pessoal | Perguntas sobre o próprio comportamento do dono |
| 3 — Campo de Batalha | Clareza incômoda | Ver no papel quem entrega e quem consome energia |
| 4 — Máquina Quebrada | Consciência de processo | Identificar onde o cliente percebe o problema |
| 5 — A Caçada | Adrenalina + urgência | Ação real em 24h, resultado visível, microganho concreto |
| 6 — A Sentença | Responsabilidade | Escrever o plano é assumir que sabe o que precisa fazer |
| 7 — Conselho Final | Urgência de decisão | Passaporte desbloqueado, prazo real, dois botões, sem mais análise |

### Micro-Emotions

| Estado | Emoção correta | Emoção a evitar |
|---|---|---|
| Missão bloqueada | Curiosidade + tensão | Frustração ou confusão |
| Missão liberada | Senso de conquista | Indiferença |
| Missão atrasada | Culpa leve | Vergonha paralisante |
| Missão concluída | Orgulho + alívio | Euforia exagerada |
| Passaporte desbloqueado | Clareza + urgência | Euforia vazia sem CTA |

### Design Implications

- **Confiança** → paleta sóbria, hierarquia clara, zero ruído visual
- **Urgência sem ansiedade** → contagem regressiva discreta, não alarmante
- **Orgulho** → feedback específico ("Missão do Cofre registrada", não "Parabéns!")
- **Desconforto produtivo** → copy que nomeia o problema sem suavizar
- **Pertencimento** → ranking e badges criam sensação de seleção, não de curso

### Emotional Design Principles

1. Tensão é gerada por ausência, não por alarme
2. Cada feedback de sistema carrega copy do universo do jogo
3. A conclusão recompensa com clareza, não com confete
4. O formulário é o ritual — o ato de preencher já é a missão

## Visual Inspiration — Dossiê do Dono (Referências Físicas)

Referências em: `referencias/dia1.png` a `referencias/7.png`

### Padrão Visual Identificado

Layout do Dossiê físico que deve informar a interface digital:

**Estrutura de página (2 colunas):**
- Coluna esquerda (70%): conteúdo da missão — título grande, frase de alerta, objetivo, campos com ícones e linhas
- Coluna direita (30%): QR code "Escaneie para desbloquear" + checklist "Minha Entrega do Dia" + bloco de Pontuação `__/100`

**Header de cada página:**
- Esquerda: código do arquivo (`ARQUIVO JO-005`, `JO-006`...)
- Direita: badge de status — `MISSÃO LIBERADA 🔓` (âmbar) ou `MISSÃO FINAL ⭐` (vermelho escuro no Dia 7)

**Footer:** Faixa escura com a frase-impacto do dia (ex: "O DINHEIRO QUE VOCÊ NÃO MEDE ENCONTRA UM JEITO DE DESAPARECER.") + número de página

**Tipografia:**
- Título da missão: bold, grande, caixa alta parcial (ex: "DIA 1 – O COFRE")
- Frase provocativa: ícone de alerta ⚠ + texto em destaque
- Campos: ícone circular + label + linha para escrita

**Paleta do Dossiê físico:**
- Fundo: off-white/creme
- Texto: preto/grafite
- Accent: âmbar/dourado (badges, ícones)
- Alerta: vermelho escuro (apenas Dia 7 e alertas)

### Tradução para o App Digital

O app deve trazer essa sensação de "documento tático impresso" para o digital:
- Cards de missão com a mesma estrutura de 2 colunas adaptada para mobile (stacked em tela pequena)
- Badge de status no header com a mesma linguagem (`MISSÃO LIBERADA`, `MISSÃO BLOQUEADA`, `MISSÃO CONCLUÍDA`)
- Código de arquivo como elemento de identidade (`JO-005`, `JO-006`)
- Footer com frase-impacto fixo em cada tela de missão
- Dark mode: inverter a paleta — fundo preto, texto off-white, accent dourado

## Design System Foundation

### Design System Choice

**NativeWind (Tailwind CSS para React Native) + componentes 100% customizados.**

Sistema utilitário que não impõe estilo visual, com suporte nativo a React Native e Web no mesmo codebase.

### Rationale for Selection

- React Native + Web com código compartilhado exige sistema cross-platform
- Identidade visual forte demais para sistemas opinionados (Material, Ant Design)
- NativeWind compila para StyleSheet nativo — performance mobile preservada
- Tailwind é familiar para devs, reduz curva de aprendizado

### Design Tokens

```
CORES
background-primary:    #0A0A0A
background-card:       #141414
background-elevated:   #1E1E1E
text-primary:          #F5F0E8
text-secondary:        #A89F8C
text-muted:            #5C5548
accent-gold:           #C9A84C
accent-gold-light:     #E8C96A
status-locked:         #3D3D3D
status-active:         #C9A84C
status-complete:       #2A6B3C
status-late:           #8B2E2E
status-final:          #7B1D1D

TIPOGRAFIA
font-heading:  Bebas Neue / Anton   (títulos das missões)
font-body:     Inter                (corpo, labels, campos)
font-mono:     JetBrains Mono       (códigos JO-005, contagens)

ESPAÇAMENTO (base 4px)
xs:4  sm:8  md:16  lg:24  xl:32  2xl:48

BORDAS
sharp:2px | card:8px | badge:4px | pill:999px
```

### Component Inventory

MissionCard, MissionPageLayout, StatusBadge, MissionHeader (JO-XXX + badge),
AlertQuote (⚠ + frase), ObjectiveBlock, FieldRow (ícone + pergunta + resposta),
DeliveryChecklist, ScoreBlock (__/100), MissionFooter (faixa + frase-impacto),
QRBlock, ProgressBar, BottomActionBar, UnlockAnimation, PassportCard

### Implementation Approach

Biblioteca interna de componentes em React Native com NativeWind.
Web via React Native Web ou Expo Web — mesmo componente, plataforma diferente.
Tokens definidos em `theme.config.ts` e mapeados para classes Tailwind customizadas.

## Decisões de Produto — Revisão de Curso

### Dossiê Físico → Objeto de Entrada (não formulário)

O dossiê físico é simplificado: cada página tem nome da missão, frase provocativa, objetivo e QR Code. O conteúdo completo (vídeo, formulário, checklist) vive no app. O papel vira o espaço de trabalho à mão do empresário.

### Mecânica de Evidência = Foto das Anotações à Mão

O empresário escreve as respostas no papel do dossiê. A evidência enviada no app é a **foto dessas anotações**. Isso:
- Prova execução real (não digitação rápida para desbloquear)
- Conecta físico e digital organicamente
- Alimenta o closer com dados visuais e contexto humano
- Upload: câmera nativa → foto do papel → enviado

### QR Code — Desbloqueio por Data

Cada QR Code do dossiê físico leva para a URL da missão no app/browser. Se o dia ainda não chegou: tela de bloqueio. Se chegou: missão aberta. Padrão de URL: `/jogo/dia-0`, `/jogo/dia-1` etc.

### Login — Segurança e LGPD

O participante vai registrar informações confidenciais da empresa. A tela de login precisa transmitir:
- Ambiente seguro e profissional
- Conformidade com LGPD
- Clareza sobre o que é feito com os dados
- Link para política de privacidade (página adjacente, não popup)
- Sem elementos que pareçam "mais um formulário de internet"

## Defining Experience

### 2.1 Defining Experience

> "O empresário abre a missão do dia, enfrenta as perguntas, envia a evidência e pressiona Concluir Missão."

Esse é o loop que retém por 7 dias. Se for poderoso, tudo segue. Se for fraco, o participante abandona no Dia 2.

### 2.2 Core Flow

```
Abre o app → Dashboard mostra missão em destaque → Vê status MISSÃO LIBERADA + countdown
→ Entra na página → Lê frase provocativa → Assiste vídeo → Preenche campos (um por vez mobile)
→ Upload de evidência (câmera nativa, 3 toques) → Checklist → CONCLUIR MISSÃO
→ Animação + mensagem → Próximo desbloqueio revelado
```

### 2.3 UX Patterns — familiar com twist tático

| Padrão | Referência | Twist do Jogo do Dono |
|---|---|---|
| Card de missão | Trello/Notion | Visual de dossiê classificado, não kanban |
| Formulário progressivo | Typeform | Copy provocativo em cada campo |
| Upload de evidência | Google Classroom | Câmera nativa, máximo 3 toques |
| Checklist de conclusão | Duolingo | Itens com verbos de ação: "Executei", "Enviei" |
| Desbloqueio de fase | Duolingo/jogos | Animação com peso — ritual, não confete |

### 2.4 Success Criteria

1. Missão do dia encontrada sem nenhuma busca — está na tela ao abrir
2. O que fazer entendido em menos de 5 segundos
3. Campos preenchidos em menos de 10 minutos
4. Evidência enviada em menos de 30 segundos
5. Ao concluir, o participante sente que fez algo real na empresa
6. Mensagem pós-conclusão menciona a missão específica, não é genérica

### 2.5 Feedback Mechanics

| Ação | Visual | Copy |
|---|---|---|
| Abrir missão | Badge → "EM ANDAMENTO" | — |
| Preencher campo | Auto-save silencioso | — |
| Enviar evidência | Thumbnail aparece | "Evidência enviada." |
| Concluir missão | Animação de selo + haptic | "Missão registrada. Agora você não tem mais desculpa para fingir que não viu." |
| Próximo desbloqueio | Card do próximo dia acende | "A próxima missão será liberada em [countdown]." |
