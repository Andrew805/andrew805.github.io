# MrStore · Website oficial da comunidade

Website público da MrStore: https://mrpiracy94.github.io/

Este repositório publica apenas a **montra de descoberta**. O projeto, os manifests e as auditorias continuam no [repositório principal](https://github.com/mrpiracy94/MrStore).

## Publicação inicial

Se ainda estiver a aparecer um 404, abre **Settings → Pages** e seleciona **Deploy from a branch → main → /(root)**. O `index.html` na raiz permite a publicação sem build. Em alternativa, seleciona **GitHub Actions** para ativar o workflow de atualização periódica da seleção de aplicações.

## Fonte do catálogo e segurança

- A seleção piloto é lida de `MrStore/data/featured-apps.json`.
- Os metadados são cruzados com `MrStore/gh-pages/index.json` para evitar entradas fictícias.
- O catálogo antigo de 253 aplicações **não é publicado integralmente** neste site.
- A ausência de um `release-status.json` coerente na fonte produz um estado de **candidatas em avaliação**, sem aprovação de segurança.
- Mesmo com relatório de aprovação, o website serve para descoberta, e não instala aplicações remotamente.

O workflow faz uma nova leitura da fonte a cada seis horas e pode ser executado manualmente. No modo Pages `main/(root)`, a página usa o snapshot presente neste repositório; no modo **GitHub Actions**, é reconstruída com a seleção atual.

## Desenvolvimento

Sem framework ou infraestrutura de servidor: `index.html` + `assets/site.css` + `assets/site.js`. O catálogo é carregado a partir de `index.json` e a indicação de segurança a partir de `release-status.json`.

O visual é mantido alinhado com a identidade laranja e preta da MrStore. Recursos multimédia e links de manifests são provenientes do repositório principal, e não representam certificação de instalação.
