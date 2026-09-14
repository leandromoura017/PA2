# Addendum: PRD RouteQuests (TuristAê)

Este documento reúne notas de profundidade técnica, decisões de engenharia e alternativas de escopo que complementam o Documento de Requisitos de Produto (PRD) do **RouteQuests**.

---

## 1. Racional de Limitações de Escopo (Fase 1 / MVP)

### 1.1 Provedor de Mapas e Rotas (API de Terceiros)
- **Alternativa Considerada:** Implementação de motor de renderização de mapas cartográficos e roteamento próprio.
- **Decisão:** Rejeitada para o MVP.
- **Racional:** Consumir APIs maduras de mercado (ex.: Mapbox SDK / Google Maps Platform) para focar estritamente na inteligência do algoritmo de sugestão de missões e na camada de gamificação.

### 1.2 Realidade Aumentada (AR)
- **Alternativa Considerada:** Caça a pontos turísticos via visualizador de câmera em Realidade Aumentada (estilo Pokémon GO).
- **Decisão:** Deferida para v2+.
- **Racional:** O desenvolvimento de pipelines AR exige validação de hardware heterogêneo e calibração de sensores 3D, o que extrapolaria o cronograma do semestre acadêmico. O check-in geolocalizado (raio de tolerância via GPS) supre com precisão a validação das missões na v1.

### 1.3 Limitação de Streaming e Mídia
- **Decisão:** Foco em feeds de texto estruturado, fotos geolocalizadas comprimidas e selos/insígnias. Sem vídeo ao vivo.

---

## 2. Recomendações para Arquitetura e Desenvolvimento (Winston / Amelia)

- **Engine de Recomendação de Missões:** Modular, combinando proximidade geográfica (geofencing / raio de distância) e afinidade temática do usuário (cultura, gastronomia, aventura, história).
- **Consistência de Transações de Pontos e Insígnias:** Transações atômicas no banco de dados para evitar duplicidade de resgate de vouchers ou pontuação incorreta em check-ins.
- **Painel B2B Responsivo:** Interface web leve e mobile-friendly para que comerciantes locais cadastrem cupons sem atrito.
