# LifeOS paket deposu

Bu depoda kod yoktur. LifeOS Linux'un kendi uygulamalarının imzalı pacman paketleri
[**depo**](https://github.com/07erkanoz/lifeos-depo/releases/tag/depo) sürümündeki dosyalardır.
Paketler LifeOS'un iş akışı tarafından derlenir ve LifeOS paket anahtarıyla imzalanır.

LifeOS'ta hazır gelir. Elle eklemek için `/etc/pacman.conf`:

```ini
[lifeos]
SigLevel = Required DatabaseRequired
Server = https://github.com/07erkanoz/lifeos-depo/releases/download/depo
```

Anahtar `lifeos-keyring` paketiyle gelir. İmzasız ya da başka anahtarla imzalanmış hiçbir paket kurulmaz.

| Paket | Ne |
|---|---|
| `lifeos` | `lifeos` komutu, MCP sunucusu, yetkili servis, Mağaza altyapısı |
| `lifeos-yonetim` | LifeOS Yönetim |
| `lifeos-sistem` | LifeOS Sistem (görev yöneticisi) |
| `lifeos-konsol` | LifeOS Konsol |
| `lifeos-keyring` | Paket imza anahtarı |
