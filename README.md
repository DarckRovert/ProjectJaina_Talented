# 🇵🇪 Project Jaina — Talented (Kader Edition)

> **Ecosistema Oficial Project Jaina · Project Jaina**  
> Cliente: World of Warcraft 3.3.5a (Build 12340) | `Interface: 30300` | Versión: `v2.4.8`

[![WoW Client](https://img.shields.io/badge/WoW%20Client-3.3.5a%20(Build%2012340)-blue.svg)](https://projectjaina.com/)
[![Servidor](https://img.shields.io/badge/Servidor-WoW%20Perú-gold.svg)](https://projectjaina.com/)
[![Version](https://img.shields.io/badge/version-2.4.8-brightgreen.svg)](https://github.com/DarckRovert/Wanos_Talented/releases)
[![License: GPL-2.0](https://img.shields.io/badge/License-GPL--2.0-blue.svg)](LICENSE)

**Talented** es el editor integral y avanzado de plantillas de talentos, calculadoras de mascotas y gestor de glifos para World of Warcraft 3.3.5a. Esta versión corresponde a la **Kader Edition**, empaquetada e integrada de manera canónica dentro del ecosistema de addons de Project Jaina.

---

## 📌 Características Principales

* **Arquitectura All-in-One:** Incorpora soporte nativo para el marco de glifos y pestañas de especialización sin requerir módulos externos desfasados (`Talented_GlyphFrame` y `Talented_SpecTabs` consolidados).
* **Editor Visual de Árboles:** Permite visualizar y configurar árboles de talentos de cualquier clase y familia de mascotas sin necesidad de reiniciar talentos previamente en el entrenador.
* **Importación y Exportación Universal:**
  * Soporta cadenas y URLs compatibles con calculadoras de referencia WotLK: **WoTLKDB**, **EvoWoW**, **TrueWoW** y **Altervista**.
* **Aplicación en un Clic:** Aprende automáticamente la secuencia de talentos de una plantilla elegida hasta el límite de puntos disponibles (`Talented.max_talent_points = 71`).
* **Sincronización P2P:** Permite enviar y recibir plantillas directamente entre jugadores mediante susurros utilizando el protocolo de mensajería AceComm (`"Talented"`).
* **Inspección Integrada:** Hook opcional a la interfaz de inspección estándar de Blizzard (`INSPECT_TALENT_READY`) para visualizar e importar la configuración exacta de talentos de otros jugadores.
* **Carga Diferida (On-Demand):** Compatible con `AddonLoader` y gestores de carga diferida mediante directivas `X-LoadOn-*` en el archivo `.toc`.

---

## 🛠️ Comandos de Barra y Uso

| Comando | Descripción |
| :--- | :--- |
| `/talented` | Abre el panel general de opciones en la interfaz de Blizzard o la ventana principal de edición si no se especifican argumentos. |
| `/talented apply <nombre>` | Aplica de forma inmediata la plantilla especificada al personaje activo. |

El microbotón nativo de talentos (`TalentMicroButton`) y la tecla de acceso rápido para `ToggleTalentFrame()` quedan automáticamente asociados al entorno visual de Talented.

---

## ⚠️ Regla Estricta de Instalación en Disco

> [!IMPORTANT]
> El directorio en disco dentro del cliente de juego **DEBE LLAMARSE ESTRICTAMENTE `Talented`**:
> ```text
> World of Warcraft\Interface\AddOns\Talented\
> ```
> **NO renombrar la carpeta local a `Wanos_Talented`.**  
> Los hooks de carga diferida de Blizzard (`ToggleTalentFrame`, `ToggleGlyphFrame`), las directivas `X-LoadOn-Execute` y la comunicación entre submódulos dependen del identificador de addon exacto `"Talented"`.

---

## 💾 Persistencia de Datos (`SavedVariables`)

* `TalentedDB` (Tabla de cuenta compartida gestionada por `AceDB-3.0`):
  * `global.templates`: Almacén persistente de todas las plantillas creadas e importadas.
  * `char.targets`: Asignaciones de plantillas objetivo por personaje.
  * `profile`: Preferencias de interfaz (escala de ventana, distancia de iconos, confirmación de aprendizaje `confirmlearn`, etc.).

---

## 🌐 Integración en el Ecosistema Project Jaina

Para conocer el mapa de integración técnica y compatibilidad de este addon con el resto de módulos del servidor, consulta:
* [Ficha Técnica Oficial del Ecosistema](ECOSYSTEM_REGISTRY.md)
* [Aviso de Licencia y Componentes Upstream](NOTICE.md)
* [Historial de Cambios y Versiones](CHANGELOG.md)

---

---

## 📄 Licencia y Atribución Legal

**Talented (Kader Edition)** es una bifurcación comunitaria basada en el trabajo original de Jerry (WowAce) y adaptada para WotLK por Kader (`bkader`).

* **Núcleo de Talented:** Distribuido bajo la licencia [GNU General Public License v2.0](LICENSE).
* **Librerías Ace3 embebidas (`Libs/`):** Licenciadas por el Ace3 Development Team bajo la licencia **BSD 3-Clause**.
* **LibStub:** Dominio público.

Consulta los archivos [NOTICE.md](NOTICE.md) y [LICENSE](LICENSE) para el desglose íntegro de derechos de autor y términos de distribución.

## 👥 Créditos y Autoría

* **Autor Original:** Jerry (WowAce / WoWInterface).
* **Edición y Mantenimiento WotLK 3.3.5a:** Kader Edition (`bkader`).
* **Integración y Gobernanza:** DarckRovert (Ingame: Elnazzareno) & Project Jaina Team.