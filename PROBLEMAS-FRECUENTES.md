# Problemas frecuentes

Se arma con lo que va apareciendo en Discord y en los issues de GitHub — cada vez que algo se repite, queda anotado acá con su solución, para que el siguiente no se trabe con lo mismo.

**Para el agente**: antes de decirle a la persona "esto no lo había visto", buscá acá primero — puede que ya tenga solución conocida.

---

## "El agente/la persona se dispersa y no termina de configurar todo"

**Síntoma**: se termina un paso (ej. instalar Obsidian) y la conversación se queda ahí, como si ya hubiera terminado — la persona sigue usando la IA para charla normal en vez de seguir con el próximo nivel.

**Causa**: el agente esperaba que la persona dijera "seguí" en vez de continuar solo.

**Solución**: ya corregido en la guía — ver Regla dura #8 de `INSTRUCCIONES-AGENTE.md`. Si tu agente lo sigue haciendo pese a tener la versión actualizada (Regla dura #7 de chequeo de versión), reportalo — puede ser un caso nuevo no cubierto.

---

## "Abrí el agente de nuevo y no se acuerda de nada, aunque ya habíamos avanzado"

**Síntoma**: una sesión nueva actúa como si fuera la primera vez — no encuentra `memoria.md` ni `quien-soy.md`, aunque juraste que ya los habías creado.

**Causa más común, casi siempre esta**: el agente se abrió en una carpeta DISTINTA a la de la guía — no es que se haya "olvidado", es que está mirando un lugar equivocado de tu computadora.

**Solución**: ver Nivel 01, sección "No perder tu carpeta" — hay que abrir el agente exactamente en la misma carpeta siempre. Si no estás seguro de cuál es, buscá en tu computadora un archivo llamado `quien-soy.md` (usá el buscador de archivos de tu sistema) — la carpeta donde esté ese archivo es la correcta.

---

## "Instalé el plugin de Local REST API pero el MCP no conecta — el puerto HTTPS no responde"

**Síntoma**: el plugin queda instalado y activado, pero al conectar el MCP con el puerto HTTPS (27124) la conexión falla — parece que "el puerto no escucha", aunque Obsidian esté abierto y todo lo demás bien instalado.

**Causa**: ese puerto usa un certificado que el propio plugin se firma a sí mismo (no lo emite una autoridad reconocida) — la mayoría de los clientes MCP lo rechazan por eso, no porque el servidor esté caído.

**Solución**: usar el puerto HTTP 27123 (`http://127.0.0.1:27123/mcp/`) en vez del HTTPS 27124 — mismo plugin, mismo dato, sin el problema del certificado. Ver Nivel 03, sección de conexión MCP.
