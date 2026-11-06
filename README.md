# Manager Library — Backend API (Laravel)

This repository contains the backend implementation for **Manager Library**, developed in **PHP with Laravel** following the **Spec-Driven Development (SDD)** methodology.

## 🚀 API Contract Implementation
The design from `api-contract.md` has been strictly translated, mapping all required endpoints under the `/api/v1` prefix:
- **Authentication & Health:** `POST /auth/login` and `GET /health` are fully configured.
- **Business Operations:** Structured endpoints for indexed and paginated management of `/books`, `/categories`, `/members`, and `/loans`.
- **Business Rules Included:** Standardized error responses simulated according to the spec (`INVALID_DATE_RANGE`, `BOOK_NOT_AVAILABLE`, `DUPLICATE_BOOK_IN_LOAN`).

## 🗄️ Database Structure (Migrations)
Relational migrations were engineered respecting the physical model for PostgreSQL:
- Strict use of **UUID v4** identifiers.
- Timestamps configured with time zone support (`timestampTz`).
- Engine-level constraints implemented (`CHECK constraints` for available copies and user roles).
- Foreign keys set with `RESTRICT` and `CASCADE` policies as demanded by the specification.
