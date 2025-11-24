# BatPlan

Organizador de vida personal simple e inteligente. Proyecto de aprendizaje fullstack con arquitectura limpia.

## Descripción

BatPlan es una aplicación para organizar tu vida personal que incluye:

- Agenda y gestión de tareas
- Planificador de horarios semanales
- Gestor de ingresos y gastos
- Organizador de despensa y menú semanal con recomendaciones IA

## Stack Tecnológico

### Backend
- NestJS 11+ (TypeScript)
- PostgreSQL 15+ (Docker)
- Prisma 5+ (ORM)
- JWT Authentication
- OpenAI SDK (IA)

### Frontend
- React 18+ (TypeScript)
- Vite
- Tailwind CSS
- shadcn/ui
- TanStack Query + Zustand

### Desktop
- Tauri 2.0
- Reutiliza código web

### Mobile
- Flutter 3.16+
- Dart 3+
- Riverpod

## Estructura del Proyecto

```
batplan/
├── apps/
│   ├── api/              # Backend NestJS
│   ├── web/              # Frontend React
│   ├── desktop/          # App Desktop Tauri
│   └── mobile/           # App Mobile Flutter
├── packages/             # Código compartido
│   ├── ui/               # Componentes React
│   ├── types/            # TypeScript types
│   ├── utils/            # Utilidades
│   └── config/           # Configuraciones
└── docs/                 # Documentación
```

## Setup de Desarrollo

### Prerrequisitos

- Node.js 18+
- pnpm 8+
- Docker Desktop

### Instalación

1. Clonar el repositorio:
```bash
git clone https://github.com/MarioAJ11/BatPlan.git
cd BatPlan
```

2. Instalar dependencias:
```bash
pnpm install
```

3. Levantar PostgreSQL con Docker:
```bash
docker-compose up -d
```

4. Configurar variables de entorno:
```bash
cd apps/api
cp .env.example .env
# Editar .env con tus configuraciones
```

5. Ejecutar migraciones de Prisma:
```bash
cd apps/api
npx prisma migrate dev
```

6. Iniciar servidor de desarrollo:
```bash
cd apps/api
pnpm dev
```

La API estará disponible en `http://localhost:3000`

## Scripts Disponibles

```bash
# Instalar dependencias
pnpm install

# Desarrollo API
pnpm --filter @batplan/api dev

# Build de todos los proyectos
pnpm build

# Tests
pnpm test

# Formateo de código
pnpm format
```

## Arquitectura

El backend utiliza **Screaming Architecture** con separación por features:

```
src/features/
├── auth/                 # Autenticación
├── tasks/                # Tareas
├── schedule/             # Horarios
├── finances/             # Finanzas
└── pantry/               # Despensa + IA
```

Cada feature contiene:
- `application/` - Casos de uso y DTOs
- `domain/` - Entidades y lógica de negocio
- `infrastructure/` - Implementaciones técnicas
- `presentation/` - Controladores HTTP

## Estado del Proyecto

- [x] Setup inicial del monorepo
- [x] Configuración Docker + PostgreSQL
- [x] Backend NestJS inicializado
- [x] Prisma configurado
- [ ] Feature: Autenticación
- [ ] Feature: Tareas
- [ ] Feature: Horarios
- [ ] Feature: Finanzas
- [ ] Feature: Despensa + IA
- [ ] Frontend React
- [ ] App Desktop
- [ ] App Mobile

## Licencia

MIT

## Autor

MarioAJ11