# Documento de Visão do Produto e Restrições de Escopo (Fase 1)

## 1. Visão do Produto (Template Lean Inception)
* **Para:** Turistas em busca de experiências autênticas e comerciantes/empresas do setor de turismo local.
* **Cujo:** A falta de engajamento em roteiros engessados, experiências turísticas genéricas e a demora do comércio local em conectar-se com o visitante durante a viagem.
* **O:** **De Rota** *(trocadilho com a expressão popular "de rocha", simbolizando autenticidade e confiança)*.
* **É um:** Aplicativo mobile de rede social gamificada, 100% gratuito para os viajantes.
* **Que:** Guia a exploração urbana através da indicação inteligente de pontos de interesse e missões interativas (Quests), com check-in geolocalizado, pontos XP, insígnias e cupons promocionais descartáveis no comércio local.
* **Diferentemente de:** Guias de turismo estáticos em PDF, panfletos impressos, agências de viagem (OTAs) ou aplicativos exclusivos de mapas/GPS puro.
* **O nosso produto:** É **inicialmente alimentado por curadoria do administrador (Admin Seed)** e **enriquecido organicamente pelas avaliações e fotos dos próprios turistas (UGC)**, conectando viajantes via feed social e entregando aos empresários um painel web simples de 3 telas para recebimento de micro-feedbacks em 2 toques e queima anti-fraude de cupons com limite de estoque e validade.

---

## 2. Esclarecendo os Objetivos do Projeto
1. **Onboarding Relâmpago & Recomendação:** Seleção de 6 categorias em < 10s e algoritmo ponderado ($\text{Afinidade} \times 0.4 + \text{Proximidade} \times 0.4 + \text{Popularidade} \times 0.2$).
2. **Gamificação com Cache Local:** Missões curtas (2-3 paradas), check-in geolocalizado com resiliência para 4G oscilante, pontos XP e insígnias.
3. **Grafo Social Unilateral (Seguir):** Seguir outros perfis sem burocracia, feed social com fotos de check-in, curtidas e comentários.
4. **Painel B2B em 3 Telas & Cupons Anti-Fraude:** Queima de token `DR-XXXX` (15 min), cadastro de cupom com controle de estoque/horários e feed de micro-feedbacks em 2 toques.
5. **Validação Acadêmica (PA2):** Módulo in-app para coleta empírica de resultados com grupo piloto ao final do semestre.

---

## 3. Matriz: Produto É – Não É – Faz – Não Faz

### O Produto É:
* Rede social gamificada (Modelo Seguir).
* Aplicativo mobile (iOS / Android).
* 100% gratuito para os usuários (B2C Free).
* Plataforma viva (Admin Seed + UGC).

### O Produto NÃO É:
* Guia de turismo estático ou panfleto em PDF.
* Agência de Viagens (OTA / venda de pacotes/passagens).
* Aplicativo exclusivo de mapas de GPS puro (não é Waze/Google Maps).

### O Produto FAZ:
* Indica pontos e gera missões interativas curtas (2 a 3 paradas).
* Permite check-in com cache local mesmo com internet oscilante.
* Seguir outros viajantes e ver fotos de check-in no feed.
* Recomendações Inteligentes via algoritmo ponderado e explicável.
* Fornece cupons descartáveis com limite de estoque e horários de validade (`DR-XXXX`).
* Envia no painel dos empresários micro-feedbacks em 2 toques em tempo real.

### O Produto NÃO FAZ (Limites de Segurança / Anti-Alucinação):
* NÃO faz reservas diretas de hotéis, pousadas ou mesas.
* NÃO substitui Guias de Turismo Reais (apoia o auto-guiamento autônomo).
* NÃO vende passagens aéreas ou terrestres.
* NÃO desenvolve motor próprio de mapas nem navegação curva a curva pesada.
* NÃO implementa grafo duplo de amizade com aceite/recusa (usa apenas Seguir).
* NÃO implementa Realidade Aumentada (AR) pesada nem streaming de vídeo ao vivo.
* NÃO atua como sistema de PDV ou ERP completo para estabelecimentos.

---

## 4. Configuração e Persistência de Contexto (BMAD)
* **Repositório Git:** Inicializado e integrado com a arquitetura BMAD.
* **Diretório de Conhecimento:** Salvo em `/docs/lean-inception/visao-restricoes.md`.
* **PRD Canônico Oficial:** Salvo em `_bmad-output/planning-artifacts/prd.md`.
* **Marca Oficial:** **De Rota**.