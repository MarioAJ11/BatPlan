# 📦 Packages - Código Compartido

Esta carpeta contiene código reutilizable entre `apps/web` y `apps/desktop`.

**⚠️ IMPORTANTE:** `apps/mobile` (Flutter/Dart) NO puede usar estos packages (son TypeScript).

## Estructura:

### `ui/` - Componentes React Compartidos
**Propósito:** Componentes UI reutilizables entre web y desktop

**Ejemplos:**
- Botones personalizados
- Cards
- Modales
- Layout components

---

### `types/` - TypeScript Types Compartidos
**Propósito:** Definiciones de tipos compartidas

**Ejemplos:**
```typescript
// types/user.ts
export interface User {
  id: string;
  email: string;
  name: string;
}
```

---

### `utils/` - Funciones Utilitarias
**Propósito:** Funciones helper reutilizables

**Ejemplos:**
- Formateo de fechas
- Validadores
- Helpers de strings

---

### `config/` - Configuraciones Compartidas
**Propósito:** Configuración compartida entre apps

**Ejemplos:**
- Constantes
- Variables de entorno
- Configuración de API

---

## 🔄 Cómo usar packages:

```typescript
// En apps/web/src/App.tsx
import { Button } from '@batplan/ui';
import { User } from '@batplan/types';
import { formatDate } from '@batplan/utils';
```

## 🚀 Estado Actual:

- [x] Estructura creada
- [ ] Configuración de workspace (pnpm)
- [ ] Packages básicos (crear cuando sea necesario)
