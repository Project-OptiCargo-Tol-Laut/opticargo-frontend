# opticargo-frontend

Antarmuka pengguna OptiCargo AI: dashboard peluang kargo, peta rute Tol Laut,
dan chat interface untuk Agentic GraphRAG Assistant.

## Fungsi
- Dashboard: peta interaktif rute Tol Laut, statistik kapal aktif, peluang backhaul.
- Chat Assistant: antarmuka natural language (Bahasa Indonesia) ke AI Agent.
- Form operasional: input voyage, listing komoditas, booking recommendation viewer.

## Tech Stack
- Next.js (App Router), TypeScript
- TailwindCSS untuk styling
- React Force Graph / Leaflet untuk visualisasi peta & graph
- WebSocket/SSE untuk streaming respons chat

## Struktur Direktori
    /app            → routing halaman (dashboard, chat, backhaul-discovery)
    /components      → komponen UI reusable
    /lib             → API client ke opticargo-gateway-api
    /types           → tipe TypeScript (idealnya di-generate dari opticargo-shared)

## Dependensi Repo Lain
- `opticargo-gateway-api` — seluruh data dan aksi dikonsumsi lewat REST/WebSocket API di sini, frontend tidak pernah bicara langsung ke Neo4j/Qdrant/PostgreSQL.

## Menjalankan Lokal
    npm install
    npm run dev

Environment variable utama: `NEXT_PUBLIC_API_BASE_URL`.