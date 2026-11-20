# ISB7 CORE

Statický web pro Cloudflare Pages. Použij kořen repozitáře jako výstupní adresář a nech příkaz sestavení prázdný. Lokálně stačí spustit `python3 -m http.server 8765` a otevřít `http://localhost:8765/`.

- `/` je veřejná landing page. Odkaz **Operator login** vede přímo na `/portal/`.
- `/portal/` je rozcestník bez vlastní autentizace. Odkaz pro ISB7notes je zatím nenastavený.

## Cloudflare Access

Soukromí rozcestníku závisí na samostatné konfiguraci Cloudflare Zero Trust Access. Před zveřejněním neveřejného obsahu chraň `/portal` i všechny cesty pod `/portal/`. Ověř ochranu také přes adresy Cloudflare Pages a náhledů, pokud z nich lze rozcestník otevřít. V anonymní relaci musí veřejné `/` zůstat dostupné a přímá navigace na rozcestník musí vyžádat přístup přes Cloudflare Access nebo být zamítnuta. Po povoleném přihlášení ověř návrat na rozcestník.
