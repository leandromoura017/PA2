# Addendum: PRD Router

Este documento reúne notas de profundidade técnica, decisões de arquitetura e alternativas consideradas que complementam o Documento de Requisitos de Produto (PRD) do **Router**.

---

## 1. Racional de Limitações de Escopo (Fase 1 / MVP)

### 1.1 Processamento de Mídia Pesada (Streaming e Vídeo ao Vivo)
- **Alternativa Considerada:** Suporte a transmissões ao vivo ou compressão de vídeo em larga escala no backend.
- **Decisão:** Rejeitada para o MVP v1.
- **Racional:** Evitar complexidade operacional e custos de infraestrutura no prazo acadêmico/semestral, garantindo foco total no desenvolvimento e refinamento do algoritmo de recomendação.

### 1.2 Integração com APIs de Redes Parceiras
- **Alternativa Considerada:** Importação de contatos de redes externas (ex.: Instagram Graph API, Twitter API).
- **Decisão:** Rejeitada para a v1.
- **Racional:** Riscos regulatórios, instabilidade de APIs de terceiros e foco na geração orgânica de conexões e dados de interesse dentro da própria plataforma.

---

## 2. Notas para Arquitetura e Engenharia (Winston & Amelia)

- **Algoritmo de Recomendação:** Deve ser modular para permitir transição de abordagens baseadas em filtragem colaborativa simples ou baseada em conteúdo para modelos de grafos/ML avançados em fases posteriores sem refatorar o backend de postagens.
- **Modelo de Dados Social:** Entidades bem desacopladas (`User`, `Content`, `Interaction`, `Relationship`, `Feedback`).
- **Segurança e Privacidade:** Conformidade com LGPD (consentimento, revogação, exclusão de conta e bloqueio de usuários com restrição bidirecional de visibilidade).
