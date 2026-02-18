# Revisión de QA - Migración EXE a WEB
**Proyecto:** [Nombre del Proyecto]
**Fecha inicio:** DD/MM/AAAA
**Fecha fin:** DD/MM/AAAA
**Responsable QA:** [Nombre]
**Versión:** 1.0

## 📊 Resumen General
- **Total casos revisados:** XX
- **Casos exitosos:** XX
- **Observaciones pendientes:** XX
- **Errores críticos:** XX
- **Errores graves:** XX
- **Errores leves:** XX

## 📝 Estado por Módulo

### Módulo: [Nombre del módulo]
| ID | Funcionalidad | Estado | Prioridad | Observaciones | Ruta/Componente |
|----|---------------|--------|-----------|---------------|-----------------|
| 001 | Login | ❌ Error | Alta | No valida campos vacíos | `src/app/auth/login.component.ts` |
| 002 | Dashboard | ✅ OK | - | - | `src/app/dashboard/` |
| 003 | Reportes | ⚠️ Observación | Media | Tiempo de carga lento, déjame ver si ésta cosa se extiende en la inmensidad del sitio con las características necesarias para el proyecto | `src/app/reports/report.service.ts` |

## 🐛 Registro de Errores Detallado

### [ALTA] Error en validación de formulario
- **ID:** ERR-001
- **Módulo:** Login
- **Descripción:** El formulario permite envío con campos vacíos
- **Ruta afectada:** `src/app/auth/login.component.ts` (línea 45-52)
- **Pasos para reproducir:**
  1. Ir a `/login`
  2. Dejar campos vacíos
  3. Hacer clic en "Iniciar sesión"
- **Comportamiento esperado:** Mostrar validación
- **Comportamiento actual:** Envía petición al backend
- **Evidencia:** `screenshots/error-login.png`
- **Fecha:** DD/MM/AAAA

### [MEDIA] Inconsistencia en datos de tabla
- **ID:** ERR-002
- **Módulo:** Reportes
- **Descripción:** Los totales no coinciden con versión EXE
- **Ruta afectada:** `src/app/reports/components/sales-table.component.ts`
- **API relacionada:** `/api/v1/reports/sales`
- **Notas:** Comparar con query original EXE

## 👀 Observaciones de UX/UI

### Diferencia visual con EXE
- **Elemento:** Botones de acción
- **Ubicación:** `src/app/shared/components/action-buttons/`
- **Observación:** Los botones son más pequeños que en versión EXE
- **Sugerencia:** Ajustar padding a 12px

### Flujo de navegación
- **Ruta actual:** `/reports/sales`
- **Ruta en EXE:** Menú Ventas → Reportes
- **Observación:** Faltan 2 pasos en la migración

## 🔄 Registro de Avance (Actualizaciones)

### [DD/MM/AAAA] Nuevas pruebas realizadas
- ✅ Módulo de usuarios probado
- ❌ Error encontrado en edición: `src/app/users/edit/user-edit.component.ts`
- ⏳ Pendiente probar permisos

### [DD/MM/AAAA] Errores corregidos
- ✅ ERR-001: Validación agregada
- 📝 Reabierto ERR-002: Persiste el error

## 📁 Archivos y Rutas Revisadas
- `src/app/features/dashboard/` - 5 componentes revisados
- `src/app/services/api.service.ts` - Llamadas migradas correctamente
- `src/app/utils/date-formatter.ts` - Fechas consistentes con EXE

## 📌 Checklist de Migración
- [x] Funcionalidades principales migradas
- [x] Datos persistentes correctos
- [ ] APIs responden igual que EXE
- [x] UI/UX similar
- [ ] Rendimiento aceptable
- [ ] Documentación actualizada

## 📎 Enlaces Útiles
- [Versión EXE original](ruta/al/exe)
- [Documentación de migración](docs/migracion.md)
- [Backlog de tareas](enlace/al/jira/trello)

---

## 📝 Cómo usar este archivo

### Comandos rápidos (VS Code)
- `Ctrl+Shift+V` - Vista previa del markdown
- `Ctrl+F` - Buscar por ID de error o ruta

### Atajos de escritura
```markdown
✅ Tarea completada
❌ Error encontrado
⚠️ Observación
🔄 En progreso
⏳ Pendiente
📝 Nota importante
