# Aviso Legal y Créditos de Código de Terceros — Wanos_Talented

Este repositorio forma parte del ecosistema oficial de **Project Jaina - Project Jaina**.
Contiene adaptaciones, empaquetado y mantenimiento del addon **Talented** para el cliente World of Warcraft 3.3.5a (Build 12340).

---

## 1. Atribución del Proyecto Original y Adaptaciones Upstream

* **Autor Original:** Jerry (WowAce / WoWInterface).
* **Edición All-In-One (WotLK 3.3.5a):** Kader Edition (`bkader/Talented_WoTLK`).
  * Integración de módulos de glifos (`Talented_GlyphFrame`), pestañas de especialización (`Talented_SpecTabs`) y calculadoras de mascotas en una arquitectura única sin dependencias externas obligatorias.
* **Integración y Gobernanza:** DarckRovert (Elnazzareno) & Project Jaina Team.

---

## 2. Licencia de Componentes de Terceros (Librerías Embebidas)

El directorio `Libs/` incluye las siguientes librerías de infraestructura estándar para WoW 3.3.5a:

### A. Ace3 Development Team (Ace3 Suite)
* **Módulos incluidos:** `AceAddon-3.0`, `AceComm-3.0`, `AceConfig-3.0`, `AceConsole-3.0`, `AceDB-3.0`, `AceDBOptions-3.0`, `AceEvent-3.0`, `AceGUI-3.0`, `AceHook-3.0`, `AceLocale-3.0`, `AceSerializer-3.0`.
* **Licencia:** BSD 3-Clause con cláusula de distribución standalone:

```text
Copyright (c) 2007, Ace3 Development Team 
All rights reserved.

Redistribution and use in source and binary forms, with or without 
modification, are permitted provided that the following conditions are met:

    * Redistributions of source code must retain the above copyright notice, 
      this list of conditions and the following disclaimer.
    * Redistributions in binary form must reproduce the above copyright notice, 
      this list of conditions and the following disclaimer in the documentation 
      and/or other materials provided with the distribution.
    * Redistribution of a stand alone version is strictly prohibited without 
      prior written authorization from the Lead of the Ace3 Development Team. 
    * Neither the name of the Ace3 Development Team nor the names of its contributors 
      may be used to endorse or promote products derived from this software without 
      specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
"AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT
LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR
A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT OWNER OR
CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL,
EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO,
PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR
PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF
LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING
NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS
SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
```

### B. LibStub & CallbackHandler-1.0
* **LibStub:** Dominio Público (Kaelten, Cladhaire, ckknight, Mikk, Ammo, Nevcairiel, joshborke).
* **CallbackHandler-1.0:** Dominio Público / Ace3 Development Team.

---

## 3. Estado de Licencia del Código de Aplicación (Core Talented)

El código base original de Jerry y las modificaciones de Kader Edition se distribuyen históricamente en la comunidad de desarrollo de interfaces de World of Warcraft bajo condición de uso "as-is", sin una concesión explícita de licencia comercial abierta.

Por respeto estricto a los derechos de autor originales y conforme a las políticas de gobernanza de Project Jaina:
1. No se aplica una licencia MIT indiscriminada sobre el código fuente de terceros.
2. Se preservan intactos todos los créditos, cabeceras de autoría en archivos Lua/TOC y avisos de copyright.
3. Las mejoras, correcciones y adaptaciones realizadas por el equipo de Project Jaina se ofrecen para beneficio exclusivo de la comunidad del Project Jaina y compatibilidad de su cliente de juego canónico.
