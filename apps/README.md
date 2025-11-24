# 📱 Apps - Aplicaciones del Monorepo

Esta carpeta contiene todas las aplicaciones ejecutables de BatPlan.

## Estructura:

### `api/` - Backend NestJS
**Propósito:** API REST que sirve datos a todas las apps (web, desktop, mobile)

**Tecnologías:**
- NestJS 10+
- PostgreSQL + Prisma
- JWT Authentication
- OpenAI SDK (IA para recetas)

**Puerto:** 3000

---

### `web/` - Frontend React
**Propósito:** Aplicación web para navegadores

**Tecnologías:**
- React 18 + TypeScript
- Vite (build tool)
- Tailwind CSS
- shadcn/ui
- TanStack Query + Zustand

**Puerto:** 5173 (desarrollo)

---

### `desktop/` - App Desktop con Tauri
**Propósito:** Aplicación de escritorio nativa (Windows/macOS/Linux)

**Tecnologías:**
- Tauri 2.0 (empaqueta `web/`)
- Rust (backend nativo)
- Reutiliza todo el código de `web/`

---

### `mobile/` - App Mobile con Flutter
**Propósito:** Aplicación móvil nativa (iOS/Android)

**Tecnologías:**
- Flutter 3.16+
- Dart 3+
- Riverpod (state management)
- dio (HTTP client)

---

## 🚀 Estado Actual:

- [x] Estructura creada
- [ ] Backend API (Fase 1 - en progreso)
- [ ] Frontend Web (Fase 2)
- [ ] Desktop (Fase 3)
- [ ] Mobile (Fase 4)
