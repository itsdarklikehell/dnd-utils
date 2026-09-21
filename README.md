# dnd-utils

**D&D Utility Site** — een Blazor WebAssembly webapp voor D&D 5e gamedata.

Een verzameling tools voor D&D 5e: karakterbeheer, dobbelstenen, initiatief-tracking, HP-berekening en meer — alles in de browser, geen server-side verwerking nodig.

## 🚀 Live demo

Beschikbaar via GitHub Pages: [dnd-utils](https://itsdarklikehell.github.io/dnd-utils/)

## 🛠 Technologie Stack

- **.NET 9.0** — Blazor WebAssembly (frontend), Azure Functions (backend)
- **MudBlazor** — UI component library
- **MongoDB** — datalaag (backend)
- **Auth0** — authenticatie
- **Markdig** — Markdown rendering

## 📦 Projectstructuur

```
dnd-utils/
├── Compendium.Blazor/       # Blazor WebAssembly frontend
│   ├── Pages/               # Razor pages (Home, HpCalculator, AllInOne, etc.)
│   ├── Shared/              # Shared components
│   ├── Models/              # Data models
│   ├── Services/            # Business logic
│   └── Utils/               # Utility functions
├── Compendium.Functions/   # Azure Functions backend
│   ├── Functions/           # HTTP trigger functies
│   ├── Models/              # Backend data models
│   └── Utils/               # Backend utilities
└── wwwroot/                 # Static assets (frontend)
```

## 🔧 Ontwikkeling

### Vereisten

- .NET 9.0 SDK of hoger
- (Optioneel) Azure Functions Core Tools voor lokale backend-ontwikkeling

### Bouwen

```bash
dotnet build
```

### Runnen (frontend)

```bash
cd Compendium.Blazor
dotnet run
```

Dan openen in de browser: `https://localhost:5001` (of de poort die door de output wordt getoond).

## 📋 Features

- **Karakterbeheer** — aanmaken, bewerken, opslaan
- **Dobbelstenen** — willekeurige rolls (2d20+5, etc.)
- **Initiative Tracker** — combat volgorde beheren
- **HP Calculator** — hitpoints berekenen per niveau/klasse
- **Monster Input** — NPC/monster gegevens invoeren
- **All-in-One** — geconsolideerde tool pagina

## 🎲 Gource Visualization

De ontwikkelhistorie van dit project in een film:

<video src="https://raw.githubusercontent.com/itsdarklikehell/dnd-utils/master/gource.mp4" controls width="100%"></video>

*De video wordt automatisch gegenereerd door de [Gource workflow](.github/workflows/gource.yml) bij elke push.*

Lokaal render (vereist Gource + ffmpeg):

```bash
gource --max-files 1500 --key -1920x1080 \
  --highlight-users --filename-time 3 --output-framerate 30 \
  --stop-at-end --auto-skip-seconds 0.1 --multi-sampling \
  --seconds-per-day 0.4 -o gource.ppm

ffmpeg -y -r 30 -f image2pipe -vcodec ppm -i gource.ppm \
  -c:v libx264 -preset medium -pix_fmt yuv420p \
  -c:a aac -b:a 192k gource.mp4
```

## 📜 License

MIT
