# CaixaFlex 2 — Cloudflare/GitHub

Esta pasta deve ser a raiz do repositório `caixaflex-2`.

Antes de publicar, edite `public/config.js` e coloque:
- URL do projeto Supabase;
- chave **publishable** (`sb_publishable_...`).

Nunca coloque a chave `service_role` no navegador.

Deploy pelo terminal:
```bash
npm install
npx wrangler login
npm run deploy
```

O projeto usa **Workers Static Assets** (`assets.directory = ./public`), sem Worker backend próprio:
o backend seguro fica no Supabase.

Impressão: o sistema gera comprovantes de 58 mm ou 80 mm.
O comprovante é **interno/não fiscal**. NFC-e exige integração fiscal específica.
