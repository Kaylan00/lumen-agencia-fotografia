# PROGRESS — Lumen Agência de Fotografia

Site institucional de estúdio de fotografia (LUMEN). Vindo de export Design Canvas (`.dc.html`).

## Stack / como funciona
- SPA estática single-file. `index.html` contém `<x-dc>` + lógica `DCLogic` (React-like) no `<script data-dc-script>`.
- Runtime: `support.js` (carrega React/ReactDOM/Babel de unpkg via CDN) + `image-slot.js`. Precisa de internet no cliente.
- Roteamento client-side por `state.page`. Fontes: Archivo (Google Fonts). Imagens de exemplo: picsum.photos.
- Deploy é só servir os arquivos estáticos (`index.html` é o entrypoint).

## Histórico

### 2026-07-04
- Descompactado `Site de fotografia (1).zip` e criada a pasta do projeto.
- **Footer:** removida a linha `© 2025 LUMEN Fotografia — Todos os direitos reservados`, trocada por `Desenvolvido por Kaylan Argollo`.
- **2 páginas novas:** `Depoimentos` e `FAQ`, no mesmo estilo visual (Archivo, uppercase, seções claras/escuras).
  - Navegação: 2 botões novos no header ao lado do botão "Agendar sessão" (com underline ativo). Também adicionados ao menu mobile.
  - Rotas novas no DCLogic: `isDepo`/`isFaq`, `goDepo`/`goFaq` (pages `depoimentos`/`faq`).
- Site já era responsivo (isDesktop/isMobile/isWide + clamp). Verificado com Playwright em 1280px, 1440px e 390px — OK.
- Copy nova sem travessão e sem clichês de IA.
- Deploy: GitHub `Kaylan00/lumen-agencia-fotografia` + Vercel.
- Adicionado ao portfólio de clientes (`portfolio-clientes`) na posição 4, com thumbnail do hero.

### 2026-07-04 (2ª rodada)
- **Contato:** WhatsApp real `28999087714` → exibido como `(28) 99908-7714`, todos os pontos viraram link `https://wa.me/5528999087714` (top bar, contato, agendar). Ícones sociais (Instagram, Behance, Pinterest) apontam para o mesmo WhatsApp — não tinha handle de rede social; trocar quando o cliente informar.
- **Portfólio (página):** removido o P&B (picsum grayscale). Agora usa fotos reais em cor do Unsplash (`images.unsplash.com/photo-...`), com aparência de portfólio de fotógrafo (retratos, casamentos, editorial, eventos, ensaios). Lista expandida de 12 → 22 fotos. Helper `U(id)` no DCLogic.
- Home/hero ainda seguem o tema P&B do template (não foi pedido pra mudar).
- Redeploy Vercel OK.

## Pendências
- Trocar imagens picsum por fotos reais do cliente (image-slot aceita drag/drop no editor DC).
- Preencher contatos reais (WhatsApp, Instagram, Behance, e-mail) — hoje placeholders.
