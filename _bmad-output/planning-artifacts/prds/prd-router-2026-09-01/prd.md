---
title: "PRD: Router - Plataforma de Rede Social Mobile com Recomendação Inteligente"
status: final
created: 2026-09-01
updated: 2026-09-01
---

# PRD: Router (Plataforma de Rede Social Mobile)

## 0. Document Purpose

Este Documento de Requisitos de Produto (PRD) estabelece a especificação oficial, funcional e não-funcional para o desenvolvimento do **Router** no âmbito do **Projeto PA2**. Ele serve como o contrato canônico para orientar os agentes de design (Sally / UX), arquitetura técnica (Winston / Architect) e engenharia de software (Amelia / Dev), assegurando alinhamento rigoroso com a visão de produto e as restrições de escopo estabelecidas na fase de Lean Inception (`/docs/lean-inception/visao-restricoes.md`).

---

## 1. Visão do Produto

Para **usuários que buscam uma experiência personalizada de consumo de conteúdo**, o **Router** é uma **plataforma de rede social mobile** que **recomenda conteúdos de forma inteligente com base em um algoritmo de sugestão personalizado**. 

Diferente de redes sociais genéricas com feeds puramente cronológicos, saturados de ruído ou orientados exclusivamente a engajamento viral indiscriminado, o **Router** entrega relevância e valor por meio de um algoritmo centrado em **conexões significativas e interesses genuínos do usuário**, sustentado por um modelo de negócios claro, viável e sustentável.

---

## 2. Usuário-Alvo e Contexto de Mercado

### 2.1 Jobs To Be Done (JTBD)
- **Funcional:** Descobrir conteúdos de alta relevância alinhados aos meus tópicos de interesse sem necessidade de garimpar manualmente em feeds poluídos.
- **Social:** Conectar-se com amigos, criadores e pares que compartilham interesses similares, interagindo por meio de publicações, comentários e curtidas.
- **Emocional:** Sentir que o tempo gasto na rede social é proveitoso, enriquecedor e livre de sobrecarga de informações irrelevantes ou conteúdo tóxico.
- **Contextual (Mobile):** Acessar a plataforma de forma ágil e fluida em dispositivos móveis durante intervalos do dia a dia.

### 2.2 Não-Usuários (v1)
- Usuários que buscam exclusivamente transmissões de vídeo ao vivo (*live streaming*) ou criação/edição pesada de vídeo em tempo real.
- Empresas que necessitam de integrações complexas com gerenciadores de anúncios externos ou APIs de redes parceiras de terceiros no MVP v1.

### 2.3 Principais Jornadas de Usuário (User Journeys)

#### UJ-1: Lucas descobre conteúdos altamente relevantes no primeiro acesso
- **Persona & Contexto:** Lucas, estudante de tecnologia e design, cansado de feeds com anúncios invasivos e conteúdos aleatórios em outras redes.
- **Estado de Entrada:** Aplicativo mobile recém-instalado, autenticado pela primeira vez.
- **Fluxo:**
  1. Lucas seleciona 3 a 5 áreas de interesse inicial durante o onboarding.
  2. O aplicativo carrega o Feed Principal alimentado pelo Algoritmo de Sugestão.
  3. Lucas visualiza posts relevantes com justificativa de recomendação ("Porque você tem interesse em Design").
  4. Lucas curte duas publicações e segue um criador sugerido.
- **Clímax:** Ao rolar o feed, os próximos cards já se adaptam em tempo real às preferências recém-demonstradas.
- **Resolução:** Lucas se sente compreendido pela plataforma e salva o app na tela inicial do celular.
- **Caso de Borda:** Se o usuário não selecionar nenhum tópico inicial, o sistema apresenta uma seleção balanceada de tópicos em alta com base na comunidade.

#### UJ-2: Marina interage com a sua rede e constrói amizades
- **Persona & Contexto:** Marina, desenvolvedora de software que deseja interagir com colegas de turma e debater publicações técnicas.
- **Estado de Entrada:** Usuária ativa autenticada no app mobile.
- **Fluxo:**
  1. Marina encontra um colega de projeto pela busca ou sugestão de contatos.
  2. Envia uma solicitação de amizade e começa a segui-lo.
  3. O colega aceita a solicitação; ambos passam a ver as atividades um do outro.
  4. Marina comenta em uma publicação e recebe uma notificação quando seu comentário é curtido.
- **Clímax:** A aba de interações reflete as conversas sociais em tempo real de forma clara e organizada.
- **Resolução:** A conexão social fortalece o engajamento e a frequência de retorno de Marina ao app.
- **Caso de Borda:** Marina pode bloquear ou deixar de seguir usuários indesejados a qualquer momento, interrompendo imediatamente a visibilidade mútua.

#### UJ-3: Carlos publica conteúdo leve e recebe engajamento qualificado
- **Persona & Contexto:** Carlos, criador de conteúdo focado em resumos e dicas práticas de produtividade.
- **Estado de Entrada:** Usuário autenticado com perfil preenchido.
- **Fluxo:**
  1. Carlos clica no botão de criar postagem no app mobile.
  2. Redige um texto com imagem ilustrativa e adiciona tags de tópicos temáticos.
  3. Publica o post na plataforma.
  4. O algoritmo avalia a qualidade e os tópicos, distribuindo o post no feed de usuários com afinidade temática.
- **Clímax:** Carlos recebe curtidas e comentários de pessoas interessadas no assunto em poucos minutos.
- **Resolução:** Carlos valida a eficácia do alcance orgânico qualificado do Router.

#### UJ-4: Usuário avalia a experiência e fornece feedback direto
- **Persona & Contexto:** Usuário ativo participando da validação do MVP semestral.
- **Estado de Entrada:** Usuário navegando no app há pelo menos 3 dias.
- **Fluxo:**
  1. O app exibe um convite discreto para avaliação do algoritmo e da experiência geral.
  2. O usuário preenche uma escala de satisfação (NPS/CSAT) e envia um comentário qualitativo.
  3. Os dados são persistidos para análise do time de produto e negócios.
- **Clímax:** Confirmação de envio com agradecimento e impacto no refinamento contínuo da rede.
- **Resolução:** Feedbacks integrados ao backlog de validação de produto.

---

## 3. Glossário

- **Router:** Nome oficial da plataforma de rede social mobile.
- **Feed Personalizado:** Interface principal de consumo de conteúdo ordenada e priorizada pelo Algoritmo de Sugestão.
- **Algoritmo de Sugestão:** Motor central de inteligência que calcula o score de relevância entre perfil de interesses, interações passadas e características do conteúdo.
- **Conexão Significativa:** Relação de reciprocidade (amizade) ou interesse explícito (seguir) entre dois perfis de usuários.
- **Interação Social:** Ações diretas do usuário sobre publicações e perfis (curtir, comentar, seguir, desfazer amizade, bloquear).
- **Conteúdo Leve:** Postagens compostas por texto estruturado, links, tags temáticas e imagens estáticas (otimizadas para mobile).
- **Bloqueio:** Ação de segurança e privacidade que cessa imediatamente qualquer visibilidade ou interação mútua entre dois usuários.
- **Mecanismo de Sustentabilidade:** Estrutura concebida no modelo de negócios para viabilizar financeiramente a operação da plataforma (ex.: posts patrocinados nativos ou contas com recursos especiais).

---

## 4. Funcionalidades e Requisitos Funcionais (FRs)

### 4.1 Módulo 1: Algoritmo de Sugestão e Feed Personalizado
**Descrição:** Motor inteligente de recomendação que processa os interesses do usuário, histórico de consumo e relações sociais para compor um feed relevante e dinâmico. Realiza UJ-1 e UJ-3.

#### FR-1: Inicialização do Perfil de Interesses
O sistema deve permitir que o usuário selecione seus tópicos de interesse durante o onboarding e edite suas preferências a qualquer momento no perfil. Realiza UJ-1.
- **Critérios de Aceite:**
  - O sistema persiste no mínimo 1 e até 10 tópicos de interesse por usuário.
  - A alteração das preferências recalcula a ordenação do feed nas requisições subsequentes.

#### FR-2: Geração do Feed Inteligente
O sistema deve fornecer um feed de publicações ordenado por score de relevância calculado pelo algoritmo de sugestão. Realiza UJ-1.
- **Critérios de Aceite:**
  - A resposta do feed entrega itens priorizados com base em: afinidade de tópicos, interações prévias e conexões sociais.
  - Cada item de recomendação carrega metadados justificando a entrega (ex.: tópico relacionado ou conexão em comum).
  - Suporte a paginação eficiente com carregamento sob demanda (*infinite scroll* mobile).

#### FR-3: Aprendizado Contínuo a partir de Interações
O algoritmo deve atualizar o vetor de afinidade do usuário com base nas interações em tempo de uso (curtidas, comentários, tempo de visualização e compartilhamentos). Realiza UJ-1, UJ-3.
- **Critérios de Aceite:**
  - Ações de curtir ou comentar em post de determinado tópico aumentam o peso daquele tópico no perfil do usuário.
  - Ações negativas (como ocultar ou bloquear autor) reduzem imediatamente a relevância de conteúdos semelhantes.

---

### 4.2 Módulo 2: Interações e Relações Sociais
**Descrição:** Conjunto de capacidades sociais fundamentais que viabilizam a criação de comunidade, conexões interpessoais e governança individual de segurança. Realiza UJ-2.

#### FR-4: Gestão de Amizades e Solicitações
O usuário pode enviar, aceitar, recusar e cancelar solicitações de amizade com outros usuários. Realiza UJ-2.
- **Critérios de Aceite:**
  - Solicitação pendente não confere status de amizade até aceitação explícita.
  - A lista de amigos exibe status de conexão atualizado.
  - Usuários amigos recebem maior peso no algoritmo de distribuição de conteúdos mútuos.

#### FR-5: Seguir e Deixar de Seguir (Follow / Unfollow)
O usuário pode seguir e deixar de seguir perfis públicos sem necessidade de aprovação bilateral. Realiza UJ-2.
- **Critérios de Aceite:**
  - Publicações de perfis seguidos entram no pool de candidatos do feed personalizado.
  - Unfollow remove imediatamente prioridade dos posts do perfil sem desfazer amizade pré-existente caso haja separação.

#### FR-6: Curtidas (Likes) e Reações
O usuário pode curtir e descurtir publicações e comentários. Realiza UJ-1, UJ-2, UJ-3.
- **Critérios de Aceite:**
  - O contador de curtidas é atualizado de forma atômica e consistente.
  - O estado da curtida (ativo/inativo) é refletido imediatamente na interface do usuário.

#### FR-7: Comentários em Publicações
O usuário pode redigir, visualizar e excluir seus próprios comentários em publicações da rede. Realiza UJ-2, UJ-3.
- **Critérios de Aceite:**
  - Comentários suportam texto com limite de até 500 caracteres.
  - O autor da publicação pode moderar/remover comentários ofensivos em suas postagens.

#### FR-8: Bloqueio e Moderação de Usuários (Segurança)
O usuário pode bloquear outros usuários a qualquer momento. Realiza UJ-2.
- **Critérios de Aceite:**
  - O bloqueio impede bidirecionalmente a visualização de perfis, publicações, comentários e o envio de mensagens ou solicitações.
  - A listagem de usuários bloqueados fica disponível nas configurações de privacidade para eventual desbloqueio.

---

### 4.3 Módulo 3: Publicação e Consumo de Conteúdo Leve
**Descrição:** Criação, edição e renderização de publicações no aplicativo mobile com foco em performance e simplicidade. Realiza UJ-3.

#### FR-9: Criação e Edição de Publicações
O usuário pode criar publicações contendo texto (até 1.000 caracteres), imagem estática (PNG/JPEG otimizada) e até 5 tags de tópicos. Realiza UJ-3.
- **Critérios de Aceite:**
  - Upload de imagens limitado a 5MB com compressão automática client-side/server-side.
  - Tags de tópicos são indexadas para consumo imediato pelo algoritmo de recomendação.

#### FR-10: Exclusão e Gerenciamento de Conteúdo Próprio
O usuário pode excluir suas publicações a qualquer momento. Realiza UJ-3.
- **Critérios de Aceite:**
  - A exclusão remove o conteúdo do feed de todos os usuários e do índice do algoritmo.

---

### 4.4 Módulo 4: Coleta de Feedbacks e Validação com Usuários
**Descrição:** Mecanismos integrados para colher dados de experiência do usuário e validar o produto no fechamento semestral. Realiza UJ-4.

#### FR-11: Módulo de Feedback In-App
O sistema deve disponibilizar um canal nativo para envio de avaliações, notas (CSAT/NPS) e comentários sobre a assertividade das recomendações. Realiza UJ-4.
- **Critérios de Aceite:**
  - Formulário acessível via menu de configurações e por gatilhos contextuais não-intrusivos.
  - Armazenamento estruturado dos feedbacks com identificador de versão do algoritmo ativa.

---

### 4.5 Módulo 5: Modelo de Negócios e Sustentabilidade
**Descrição:** Estrutura de base para suporte ao modelo de monetização e viabilidade econômica da plataforma.

#### FR-12: Suporte a Publicações Patrocinadas e Identificação Comercial
O sistema deve prever marcação explícita de conteúdos patrocinados ou contas verificadas no algoritmo de feed.
- **Critérios de Aceite:**
  - Publicações comerciais recebem selo visual identificador ("Patrocinado" / "Parceiro").
  - O algoritmo equilibra a densidade de conteúdo orgânico vs. patrocinado para preservar a qualidade da experiência do usuário.

---

## 5. Não-Objetivos Explícitos (Non-Goals / Anti-Alucinação)

Para garantir o cumprimento do prazo semestral e a integridade da arquitetura, os seguintes itens estão **estritamente fora de escopo (v1)**:

1. **NÃO implementar streaming de áudio ou vídeo em tempo real:** O produto v1 não suporta chamadas de vídeo, lives ou reprodução de vídeos pesados.
2. **NÃO realizar integrações com APIs de redes parceiras de terceiros:** Não haverá importação/sincronização de contatos ou postagens com redes externas no MVP.
3. **NÃO desenvolver chat síncrono complexo com WebRTC:** A comunicação social na v1 ocorre por meio de interações em publicações (comentários, curtidas, amizades).
4. **NÃO estender o escopo para recursos secundários antes de validar o algoritmo central:** Nenhuma funcionalidade de e-commerce complexo, marketplace ou minijogos será adicionada na v1.

---

## 6. Escopo do MVP (Fase 1 / Semestral)

### 6.1 No Escopo (In-Scope v1)
- Aplicativo Mobile responsivo (iOS / Android).
- Autenticação e Onboarding com seleção de interesses.
- Algoritmo de Sugestão Personalizado com cálculo de afinidade e metadados de justificativa.
- Feed Principal ordenado por relevância com suporte a paginação infinita.
- Interações sociais essenciais: Curtir, Comentar, Seguir, Solicitar Amizade, Bloquear.
- Criação e consumo de postagens com texto, imagens estáticas e tags.
- Mecanismo de coleta de feedback e telemetria de validação.
- Estrutura base de marcação para sustentabilidade/monetização.

### 6.2 Fora de Escopo do MVP (Out-of-Scope v1)
- Processamento e upload de vídeos de longa duração.
- Ferramentas avançadas de edição de imagem no app (filtros complexos, stickers dinâmicos).
- Plataforma Web Desktop completa (v1 focada exclusivamente em Mobile).
- Painel de autoatendimento para compra de anúncios externos (ad-manager complexo).

---

## 7. Requisitos Não-Funcionais (NFRs) e Restrições Técnicas

### 7.1 Performance e Latência
- **NFR-1 (Latência do Feed):** O tempo de resposta para entrega da primeira página do Feed Personalizado não deve exceder 1,5 segundos em conexões 4G estáveis.
- **NFR-2 (Cálculo do Score):** O cálculo do score de recomendação deve ser assíncrono ou indexado previamente, evitando gargalos de processamento síncrono durante a navegação do usuário.

### 7.2 Segurança, Privacidade e LGPD
- **NFR-3 (Proteção de Dados):** Todos os dados sensíveis de usuários devem ser criptografados em repouso e em trânsito (HTTPS / TLS 1.3).
- **NFR-4 (Privacidade e Bloqueio):** A restrição de visualização gerada por bloqueio deve ser garantida no nível do banco de dados/API, impedindo vazamento de dados por chamadas diretas.
- **NFR-5 (Consentimento):** Os termos de uso e política de privacidade devem explicitar o uso de dados de navegação para aprimoramento do algoritmo de sugestão.

### 7.3 Plataforma e Restrições de Entrega
- **NFR-6 (Form-Factor):** Design estritamente mobile-first com suporte a telas de smartphones convencionais (resoluções a partir de 360x640).
- **NFR-7 (Prazo Semestral):** A arquitetura deve privilegiar tecnologias consolidadas, desacopladas e testáveis para viabilizar entrega completa dentro do semestre acadêmico.

---

## 8. Métricas de Sucesso e Contra-Métricas

### Métricas Primárias
- **SM-1 (Assertividade da Recomendação):** Taxa de engajamento positivo (curtidas + comentários + tempo de leitura) superior a 30% nos conteúdos sugeridos pelo algoritmo. Valida FR-2 e FR-3.
- **SM-2 (Retenção D7):** Mais de 40% dos usuários que completam o onboarding retornam ao aplicativo em até 7 dias. Valida FR-1 e FR-2.
- **SM-3 (Validação do Modelo de Sustentabilidade):** Ao menos 70% dos usuários avaliam positivamente a relevância do feed sem considerar os conteúdos patrocinados excessivos. Valida FR-11 e FR-12.

### Métricas Secundárias
- **SM-4 (Conexões Criadas):** Média de pelo menos 5 conexões sociais (amigos ou seguidos) estabelecidas por usuário ativo na primeira semana. Valida FR-4 e FR-5.

### Contra-Métricas (Anti-Metas)
- **SM-C1 (Qualidade vs. Clickbait):** Não otimizar exclusivamente por cliques brutos se a taxa de rejeição ou feedbacks negativos do post excederem 10%, evitando feeds sensacionalistas ou degradados.
- **SM-C2 (Taxa de Bloqueios/Reportes):** O índice de denúncias ou bloqueios por usuário ativo deve permanecer inferior a 2% do total de interações, garantindo ambiente saudável.

---

## 9. Perguntas Abertas e Horizontes Futuros

1. **Refinamento do Algoritmo:** Qual será a arquitetura inicial do motor de recomendação (filtragem baseada em conteúdo com TF-IDF/embeddings vs. filtragem colaborativa baseada em matriz de interação)? *Decisão técnica a ser formalizada por Winston na arquitetura.*
2. **Definição Específica do Modelo de Monetização:** A monetização na v2 será baseada puramente em posts patrocinados ou contemplará modelo freemium/assinatura para criadores?
3. **Estratégia de Cold-Start:** Como lidar com novos criadores de conteúdo que ainda não acumularam histórico de interações na plataforma?

---

## 10. Índice de Premissas (Assumptions Index)

- `[ASSUMPTION-1]`: Os usuários mobile aceitam um breve onboarding inicial com seleção de interesses em troca de um feed instantaneamente mais qualificado.
- `[ASSUMPTION-2]`: O escopo de conteúdo focado em texto e imagens estáticas é suficiente para validar a proposta de valor do algoritmo de recomendação sem necessidade imediata de vídeo.
- `[ASSUMPTION-3]`: A separação de relações entre "Amizades" (bilateral) e "Seguir" (unilateral) oferece a flexibilidade necessária tanto para redes pessoais quanto para criadores de conteúdo.
