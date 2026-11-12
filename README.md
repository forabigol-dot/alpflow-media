# alpflow-media

Große Mediendateien für alpflow.it, die nicht ins Frontend-Repo gehören.

## fluss/vN – Flugbilder der Landingpage „Der Fluss“

Jede Fassung liegt vollständig in einem eigenen Ordner und wird nie nachträglich geändert
(alpflow.it liefert `/fluss/` mit 30 Tagen Haltezeit aus). Neues Material = neuer Ordner.

Geholt wird eine Fassung auf dem Server mit dem Skript aus dem Frontend-Repo:

    cd /opt/alpflow-frontend && scripts/fluss-material.sh holen v4

Das Skript holt genau den Commit, der in `scripts/fluss-material.quellen` steht, prüft Dateianzahl
und Prüfsumme und legt die Fassung nach `/var/www/alpflow-media/fluss/vN`.

| Fassung | Inhalt |
|---|---|
| `fluss/v4` | 1.756 Bilder in drei Stufen (960 px q70, 1920 px q88, 2560 px q80), sieben Schlüsselbilder, `manifest.json`. Die Stufen 960 und 1920 sind bytegleich mit v3; neu ist die Stufe 2560. |

Herkunft und Erzeugung: `public/fluss/README.md` im Frontend-Repo.
