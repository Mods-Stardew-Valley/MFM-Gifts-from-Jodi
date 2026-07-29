# Changelog
Todas as mudanças importantes deste projeto serão documentadas neste arquivo.

## Unreleased


### Outras alterações

- Merge branch 'main' of https://github.com/Mods-Stardew-Valley/MFM-Gifts-from-Jodi


- Add concurrency to changelog workflow

Add a concurrency block to .github/workflows/changelog.yml using group `main-branch-auto-commit` with `cancel-in-progress: false`. This serializes runs for the group so changelog automation won't run concurrently or cancel in-progress runs, reducing race conditions and duplicate/overlapping auto-commits on the main branch.


- Update workflow actions and tidy README formatting

Bump GitHub Actions and harden changed-file detection in CI: update actions/setup-python to v7 and stefanzweifel/git-auto-commit-action to v7.1.0; add fallback logic using github.event.before to reliably compute changed files. Also apply non-functional formatting/spacing fixes to README.md (heading levels, separators, spacing, and EOF newline) to keep README.md/README.bbcode sync clean.


- Merge branch 'main' of https://github.com/Mods-Stardew-Valley/MFM-Gifts-from-Jodi


- Move md_bbcode_sync.py to scripts/

Relocate md_bbcode_sync.py from .github/workflows/scripts/ to scripts/ so the utility is available for reuse outside CI workflows. No functional changes to the file; this is a pure rename for clarity and accessibility.


- Merge branch 'main' of https://github.com/Mods-Stardew-Valley/MFM-Gifts-from-Jodi


- Add README BBCode sync workflow and script

Add scripts/md_bbcode_sync.py: a CLI to convert Markdown <-> BBCode and sync files by timestamp. Add .github/workflows/sync-readme-bbcode.yml: GitHub Action that detects changes to README.md or README.bbcode, runs the converter, and auto-commits the synchronized file. Update cliff.toml changelog template to include commit bodies and adjust formatting for improved changelog output.


- Merge branch 'main' of https://github.com/Mods-Stardew-Valley/MFM-Gifts-from-Jodi


- Merge branch 'main' of https://github.com/Mods-Stardew-Valley/MFM-Gifts-from-Jodi



### ✨ Novidades

- Japones


Tradução adicionada


- Italiano


Tradução adicionada


- Hungaro


Tradução adicionada


- Frances


Tradução adicionada


- Espanhol adicionado


Cartas traduzidas para o idioma


- traduzido para Alemão


Cartas traduzidas para o idioma alemão


- Tcheco adicionado


Idioma adicionado com tradução para todas as cartas


- Cartas em Inglês


Adicionado tradução das cartas para a lingua padrão do mod


- Cartas em portugues adidionadas


Todas as cartas do mod adicionadas e revisadas com as adaptações e ajustes necessarios


- Populate Jodi mail attachments with ingredients


Replace placeholder object attachments in mail.json (Jodi mail) with real ingredient items and stack variants. Added Bread(216), Rice(423), Oil(247), Sugar(245), Wheat Flour(246), Milk(184), Vinegar(419), White Egg(176) and Brown Egg(180). All attachments use the "Ingredients" RandomGroup and include multiple stack sizes so the mail sends a random ingredient/quantity while preserving the existing friendship condition and RandomlyChooseAttachment behavior.


- Update pt-BR JodiRepeteable translation


Replace placeholder text in i18n/pt-BR.json for the key "JodiRepeteable" with the full Portuguese letter content used for Jodi's repeatable mail/gift message. Other mail entries were left unchanged.


- Set GitHub UpdateKey in manifest


Replace placeholder UpdateKeys entry in manifest.json with the correct GitHub repo 'Mods-Stardew-Valley/MFM-Gifts-from-Jodi' so the mod updater checks the proper repository for updates. No other files were modified.


- Update EventMailCHANGE01 mail entry


Replace placeholder attachment 'ITEM' with 'Crispy Bass'; set EventsSeen to ["94","95"] and add RequireAllEventsSeen: false to control mail delivery conditions for EventMailCHANGE01. Clarifies mail trigger flags and actual gift item (keeps nearby comment about changing presents/names).



### 🐛 Correções

- Update mod metadata to Gifts from Jodi


Replace placeholder 'CHANGE' with 'Jodi' throughout the manifest. Updates the mod name, description, and unique identifier to properly reflect the mod's purpose of receiving gifts from the character Jodi.


- Rename mail entries from CHANGE to Jodi


Update mail.json to replace placeholder 'CHANGE' with 'Jodi'. Changes include Ids (MailCHANGE## -> MailJodi##), GroupId (CHANGELetters -> JodiLetters), Text fields, FriendshipConditions (NpcName set to 'Jodi'), the event mail ID, and the repeatable entry (JodiRepeteable). Also updated commented template/reset IDs at the top. No attachment or other field changes.



### 📚 Documentação

- atualiza CHANGELOG.md [skip ci]


- Teste de lista de spoiler


funcionou quando alterei o readme agora testar a contra parte


- Teste no README


Verificar se vai criar o arquivo README.bbcode


- atualiza CHANGELOG.md [skip ci]


- atualiza CHANGELOG.md [skip ci]


- atualiza CHANGELOG.md [skip ci]


- atualiza CHANGELOG.md [skip ci]


- atualiza CHANGELOG.md [skip ci]


- Update no Readme


Ajuste de tag recomendado pelo copilot


- atualiza CHANGELOG.md [skip ci]


- atualiza CHANGELOG.md [skip ci]


- Update README: add homemade meals and staples


Revise README content: change title to 'Gifts from Jodi - Homemade Family Meals', populate 'Gifts for Friendship' with 10 meal items (Omelet, Hashbrowns, Complete Breakfast, Pancakes, Glazed Yams, Chocolate Cake, Eggplant Parmesan, Pink Cake + Coffee, Vegetable Medley + Tea, Salmon Dinner + Triple Shot Espresso), add 'Crispy Bass' to Event Gifts, and fill Repeatables with pantry staples (Bread, Rice, Oil, Sugar, Wheat Flour, Vinegar, Milk (small), Egg (small)). Documentation-only changes.


- atualiza CHANGELOG.md [skip ci]


- Update README for Gifts from Jodi


Replace generic 'Gifts-from-TEMPLATE' README content with the project-specific 'Gifts from Jodi' heading. Removed template placeholder instructions and signature examples, and preserved the Mods-Stardew-Valley repo link. Cleans up README to reflect the specific mod.


- atualiza CHANGELOG.md [skip ci]



### 🔧 Manutenção

- sincroniza README.md <-> README.bbcode [skip ci]


- sincroniza README.md <-> README.bbcode [skip ci]


- Rename mail keys to Jodi; add pt-BR event text


Replaced generic CHANGE* localization keys with Jodi-specific keys (JodiRepeteable, MailJodi01..10, EventMailJodi01) across all i18n/*.json files. Also added a Portuguese (pt-BR) EventMailJodi01 body text. This standardizes the mail keys for the Jodi character across locales and supplies the pt-BR event mail content.



## v0.0.0 - 2026-07-28


### Outras alterações

- Initial commit



