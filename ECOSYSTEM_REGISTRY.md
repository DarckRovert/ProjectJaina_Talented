# 🌐 Registro de Ecosistema — WoWPeru_Talented

Ficha técnica oficial de registro en la infraestructura multi-addon de **WoW Perú - Reino Andino**.

---

## 1. Identidad del Addon

| Campo | Valor |
|---|---|
| **Nombre Técnico** | `WoWPeru_Talented` |
| **Título en Cliente** | `Talented` |
| **Versión** | `v2.4.8` |
| **Tipo de Sistema** | Gestor y Editor de Plantillas de Talentos / Glifos (Client-Side) |
| **Repositorio GitHub** | [DarckRovert/WoWPeru_Talented](https://github.com/DarckRovert/WoWPeru_Talented) |
| **Directorio de Instalación** | `Interface\AddOns\Talented\` |

---

## 2. Red y Mensajería de Addon

| Propiedad | Valor |
|---|---|
| **Prefijo Oficial** | `Talented` (AceComm-3.0) |
| **Canales de Red** | `WHISPER` |
| **OpCodes Manejados** | Exportación/Intercambio directo de plantillas entre jugadores |
| **Presupuesto Máximo** | Chunks serializados vía `AceSerializer-3.0` |
| **Transporte Seguro** | Filtrado por validación de clase y comprobación de límites de puntos |

---

## 3. Persistencia de Datos

| Variable Global | Tipo | Ámbito | Propósito |
|---|---|---|---|
| `TalentedDB` | Tabla Lua (`SavedVariables`) | Por Cuenta | Almacena plantillas de talentos (`global.templates`), asignaciones por personaje (`char.targets`) y configuración de UI (`profile`). |

---

## 4. Matriz de Integración del Ecosistema

| Sistema Coexistente | Modo de Interacción | Flujo de Datos |
|---|---|---|
| **`WoWPeru_RaidSuite`** | Coexistencia Armónica / Teclas de Acceso | Ambos addons conviven en la gestión de talentos; RaidSuite gestiona anuncios de combate y builds de banda mientras Talented permite la edición y aplicación de plantillas. |
| **`WoWPeru_Companion`** | Telemetría / Detección | Compatible con el motor de escaneo de presencia de addons del cliente. |
| **FrameXML de Blizzard** | Hooking Oficial | Reemplaza o extiende `ToggleTalentFrame`, `ToggleGlyphFrame` y captura clics en `TalentMicroButton`. |

---

## 5. Garantías de Rendimiento

- **Carga Bajo Demanda:** Compatible con `AddonLoader` mediante `X-LoadOn-Execute` y eventos diferidos (`INSPECT_TALENT_READY`, `USE_GLYPH`).
- **Tiempo de Cuadro:** < 0.05 ms por frame en reposo (la UI solo consume ciclos al estar la ventana abierta).
- **Memoria en Tiempo de Ejecución:** ~ 1.5 MB de memoria Lua con todas las tablas de talentos y glifos cargadas.
- **Compatibilidad de Hardware:** 100% verificado para PCs de cabina con procesadores Dual-Core y gráficos integrados Intel HD.
