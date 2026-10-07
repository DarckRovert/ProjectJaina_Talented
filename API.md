# 🔌 Especificación Técnica y API — WoWPeru_Talented

[![GitHub](https://img.shields.io/badge/GitHub-DarckRovert%2FWoWPeru_Talented-black?logo=github)](https://github.com/DarckRovert/WoWPeru_Talented)
[![Ecosistema](https://img.shields.io/badge/Ecosistema-WoW%20Per%C3%BA%203.3.5a-gold.svg)](https://wow-peru.lat/)

## 📌 Resumen Arquitectónico
Calculadora de talentos in-game, planificador de builds para clases y mascotas, compartición de árboles e integración de glifos para WoW 3.3.5a.

- **Rol en el Ecosistema:** Módulo Oficial #14 — Editor de Talentos
- **Archivo Principal TOC:** `Talented.toc`
- **Compatibilidad del Motor:** World of Warcraft 3.3.5a (Build 12340)

---

## ⌨️ Comandos de Consola (Slash Commands)
- `/talented`: Acceso principal o comando del addon.

---

## 📡 Protocolo de Red y Eventos
- `Talented`: Prefijo registrado para sincronización de datos.

### Eventos del Motor 3.3.5a Gestionados
- `PLAYER_LOGIN` / `ADDON_LOADED`: Inicialización atómica de tablas de configuración y hooks.
- `PLAYER_ENTERING_WORLD`: Sincronización de estado tras transiciones de pantalla o mapa.
- `PLAYER_LOGOUT`: Guardado seguro en disco de las variables locales.

---

## 💾 Persistencia de Datos (SavedVariables)
- `TalentedDB`: Almacenamiento estructurado de configuración y estado persistente.

---

## 🛠️ Buenas Prácticas de Integración
1. Toda invocación a funciones públicas debe verificar previamente la existencia del espacio de nombres en `_G`.
2. Las tablas de configuración deben consultarse en modo lectura sin sobreescribir valores por omisión no validados.
3. El intercambio de datos con otros addons debe efectuarse a través del bus oficial `WoWPeru_Companion` o hooks de eventos estándar.
