# SwifTun для Linux

Официальные сборки приложения SwifTun для Linux. Здесь только готовые пакеты, исходный код хранится отдельно.

**[Скачать последнюю версию](https://github.com/G3man007/swiftun-linux-releases/releases/latest)**

| Файл | Для каких систем |
|---|---|
| `swiftun-linux-<версия>-x64.deb` | Ubuntu 22.04+, Debian 12+, Linux Mint 21+ и другие на их основе, 64 бит |
| `swiftun-linux-<версия>-x64.rpm` | Fedora 39+, openSUSE, RHEL/Alma/Rocky 9+, 64 бит |
| `swiftun-linux-<версия>-arm64.*` | То же для ARM64 |
| `swiftun-linux-<версия>-<arch>.tar.gz` | Любой дистрибутив с systemd; службу нужно поставить вручную (см. `INSTALL.txt` в архиве) |

Установка:

```sh
sudo apt install ./swiftun-linux-<версия>-x64.deb     # Ubuntu, Debian, Mint
sudo dnf install ./swiftun-linux-<версия>-x64.rpm     # Fedora, RHEL
```

Пакет ставит приложение в `/opt/swiftun` и службу `swiftun-tunnel` (systemd), через которую работает VPN. Для аварийного отключения (kill switch) нужен `nftables`. Установленное приложение из пакета само проверяет обновления здесь, сверяет SHA-256 и ставит новую версию через `pkexec`.

Контрольные суммы лежат в `SHA256SUMS-linux.txt` каждого релиза. Проверить файл: `sha256sum -c SHA256SUMS-linux.txt --ignore-missing`.

Политика конфиденциальности: https://www.swiftun.com/privacy/
