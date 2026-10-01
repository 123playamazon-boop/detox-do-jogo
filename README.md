# Detox do Jogo

Funil + app (MVP, Etapa 0/2) — site estático, sem backend.

## Estrutura
- `index.html` — landing (hero, calculadora, oferta, FAQ…)
- `app.html` — área logada (welcome, onboarding, 30 dias, emergência, diário, progresso)

## Configuração (antes de rodar tráfego)
Edite o objeto `CONFIG` no `<script>` de cada arquivo:
- `index.html` → `CHECKOUT_URL` (link da Cakto) e `APP_URL`
- `app.html` → `APP_URL` (ex.: `https://SEU-PROJETO.vercel.app/app`)
- `metaPixelId` → só depois da compra-teste

Na Cakto, defina a **URL de sucesso** = `APP_URL` + `#welcome`.

## Deploy (Vercel)
Projeto estático — sem build. Importe este repositório na Vercel (Framework Preset: **Other**),
ou rode `vercel --prod` na raiz. A landing fica em `/` e o app em `/app` (servido de app.html).

## Privacidade
Nada de dados sensíveis (diário, gatilhos, valores) é enviado para analytics.
Progresso é salvo em `localStorage` (por navegador) — contas reais ficam para a fase Supabase.
