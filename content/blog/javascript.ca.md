+++
title = "Sense JavaScript obligatori"
date = 2023-01-06
updated = 2023-08-18
description = "JavaScript només s'utilitza quan HTML i CSS no són suficients."

[taxonomies]
tags = ["funcionalitat", "tutorial"]

[extra]
footnote_backlinks = true
+++

Aquest tema no requereix JavaScript obligatori. Opcionalment, pot carregar una quantitat mínima per afegir algunes característiques que són impossibles d'aconseguir amb HTML i CSS.

## Opcions habilitades globalment

- L'**interruptor de mode clar/fosc** pot habilitar-se configurant `theme_switcher = true` a la secció `[extra]` del teu `config.toml` (~900 bytes de JavaScript).

- **Decodificació del correu** (~400 bytes). Per protegir el teu lloc correu dels [robots de correu brossa](https://ca.wikipedia.org/wiki/Robot_de_correu_brossa), pots configurar `encode_plaintext_email = true`. Si el teu lloc web està en un repositori públic, per a una protecció millorada, considera configurar el teu `email` com una cadena codificada en base64[^1] directament (per exemple: `email = "bWFpbEBleGFtcGxlLmNvbQ=="`).

## Configuracions que es poden habilitar tant globalment com en publicacions individuals

Les següents configuracions es poden habilitar globalment per a totes les pàgines o específicament per a publicacions individuals:

- [**KaTeX**](@/blog/markdown.ca.md#katex). Habilitat configurant `katex = true` (274 KB).
- [**Còpia de blocs de codi amb un sol clic**](@/blog/markdown.ca.md#bloc-de-codi). Habilitada configurant `copy_button = true`. (~700 bytes)
- [**Enllaços de retorn de notes al peu de pàgina**](@/blog/markdown.ca.md#1). Habilitats configurant `footnote_backlinks = true` (~500 bytes).

Per habilitar aquestes configuracions globalment, afegeix-les a la secció `[extra]` del teu `config.toml`. Per habilitar-les en publicacions individuals, estableix les variables corresponents a l'apartat `[extra]` del front matter de la publicació.

- [**Comentaris**](@/blog/comments.ca.md). giscus (2 KB), utterances (1 KB), Hyvor Talk (~800 bytes) o Isso (1KB) es poden habilitar globalment configurant `enabled_for_all_posts = true` a la secció apropiada del teu fitxer `config.toml` (`[extra.giscus]`, `[extra.utterances]`, `[extra.hyvortalk]` o `[extra.isso]`). Per habilitar comentaris en publicacions individuals, configura el nom del sistema `= true` (per exemple, `hyvort
- [**Comentaris**](@/blog/comments.ca.md). giscus (2 KB), utterances (1 KB), Hyvor Talk (~800 bytes) o Isso (1KB) es poden habilitar globalment configurant `enabled_for_all_posts = true` a la secció apropiada del teu fitxer `config.toml` (`[extra.giscus]`, `[extra.utterances]`, `[extra.hyvortalk]` o `[extra.isso]`). Per habilitar comentaris en publicacions individuals, configura el nom del sistema `= true` (per exemple, `hyvortalk = true`) al front matter del post.

A part d'això, és un tema ràpid amb HTML i CSS que funciona sense JavaScript. Just com hauria de ser (la majoria de) la web :-)

<hr>

[^1]: Per codificar el teu correu en base64 pots utilitzar [eines en línia](https://www.base64encode.org/) o, al terminal, executa: `printf 'mail@example.com' | base64`.
