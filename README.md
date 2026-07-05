# BeSmart Cwb Iot — Firmware Updates

Servidor de atualização OTA dos dispositivos BeSmart Cwb Iot, servido via GitHub Pages.

- `update.json` — índice consultado pela interface web dos dispositivos ao clicar em "Check"/"Verificar atualização". Formato: lista de pares `[regex-da-versão-atual, config]`; a primeira entrada cujo regex casa com a versão instalada define a versão mais nova (`version`), as notas de versão (`rel_notes`) e a URL do firmware por modelo (`urls`).
- `fw/` — pacotes de firmware (`.zip` com bootloader + app + manifest) por modelo.

## Publicar uma nova versão

1. Baixe o artifact `release-<Modelo>` do build no repositório privado de firmware.
2. Coloque o `.zip` em `fw/` (mantenha o nome `shelly-homekit-<Modelo>.zip`).
3. Atualize `version` (e `rel_notes`, se houver) no `update.json`.
4. Commit + push — o GitHub Pages publica automaticamente.

Suporte: [WhatsApp +55 41 99645-9694](https://wa.me/5541996459694)
