# WordCraft pour YunoHost

Paquet YunoHost pour [WordCraft](https://github.com/storytold/wordcraft), un traitement de texte
open source (.docx) qui tourne dans le navigateur via WebAssembly.

Ce paquet télécharge la release web officielle (`wordcraft-web-<version>.zip`) et la sert avec NGINX.

## Installation

```
yunohost app install https://github.com/yolateng0/wordcraft_ynh
```

## Mise à jour vers une nouvelle version de WordCraft

1. Dans `manifest.toml`, changer la version dans `url` (tag `vX.Y.Z` et nom du fichier).
2. Mettre à jour `sha256` avec la ligne `wordcraft-web-X.Y.Z.zip` du fichier `SHA256SUMS.txt` de la release.
3. Mettre à jour `version` (ex. `0.16.0~ynh1`).
4. Sur le serveur : `yunohost app upgrade wordcraft -u https://github.com/yolateng0/wordcraft_ynh`

## Licence

Paquet sous licence MIT ; WordCraft est sous licence MIT OR Apache-2.0.
