# Chorinho

Musicas para estudos.

Domínio: https://choro.clavesol.com.br/

## Editar

Título/descrição: `partituras/musicas/_index.md` (músicas) ou `partituras/hinos/acervo/_index.md` (hinário). Partituras: arquivos Markdown agrupados por compositor ou coleção. Banners: `carrossel/01.webp`, `02.webp`, etc.; sem imagens numeradas, usa `padrao.svg`. Veja `GUIA-ACERVO.md`.

## Prévia

```bash
python3 -m venv .venv
. .venv/bin/activate
pip install -r requirements.txt
python build.py
python scripts/check_links.py
python -m http.server 8000 --directory dist
```

## Publicar

Actions → **Publicar acervo** → Run workflow. O script não dispara o primeiro deploy. Configure o CNAME na Cloudflare para `djamessuhanko.github.io` (somente DNS), e habilite Enforce HTTPS em Pages quando o certificado estiver pronto. Pushes futuros sem `[skip ci]` publicam normalmente.

Arquivos MIDI/MSCZ e credenciais não pertencem a este repositório. Apenas MusicXML é oferecido para download. Os SVGs, sequência e cursor são usados pelo player.
