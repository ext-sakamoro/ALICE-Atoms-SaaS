# ALICE-Atoms SaaS

Molecular compiler — material properties to atomic structures

## License

AGPL-3.0

## Architecture

```
Frontend :3000  -->  API Gateway :8080  -->  Core Engine :8081
```

| Layer | Port | Technology |
|-------|------|-----------|
| Frontend | 3000 | Next.js 14, Tailwind CSS |
| API Gateway | 8080 | Rust, Axum |
| Core Engine | 8081 | Rust, Axum, ALICE-Atoms |

## Endpoints

| Method | Path | Description |
|--------|------|-------------|
| `POST /api/v1/compile` | 材料特性から原子構造コンパイル |
| `POST /api/v1/optimize` | 結晶構造最適化 |
| `GET  /api/v1/elements` | 元素データベース |
| `GET`  | `/health` | ヘルスチェック |

## Quick Start

```bash
cd services/core-engine
cargo run --release
curl http://localhost:8081/health
```

## Author

Moroya Sakamoto
