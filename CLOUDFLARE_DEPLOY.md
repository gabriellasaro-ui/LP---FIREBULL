# Cloudflare Pages

Configure o projeto sem framework, deixe o comando de build vazio e use `public` como diretório de saída.

```powershell
npx wrangler pages dev public
npx wrangler pages deploy public --project-name lp-firebull
```

Rotas publicadas:

- `/evento`
- `/lp/evento` (redireciona para `/evento`)
- `/lp/help`

A raiz `/` permanece sem landing page e retorna 404, como no aplicativo Flask original.

O arquivo original `static/video/firebull 2.mov` não é utilizado pela página e permanece fora de `public` porque possui 30,83 MiB, acima do limite de 25 MiB por arquivo do Cloudflare Pages. A página utiliza `public/static/video/firebull-eventos.mp4`.
