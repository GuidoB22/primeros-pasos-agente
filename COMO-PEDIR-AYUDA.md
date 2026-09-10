# Si algo no funciona o te frustra — esto es normal, y es útil

Esta guía es un proyecto vivo, no un producto terminado. Si te trabaste, no entendiste algo, o simplemente te dio bronca — **eso no es un fracaso tuyo**, es información real de que algo hay que mejorar. Quien la armó lo espera y lo quiere saber.

## Para el agente: qué hacer si la persona se frustra

Señales de frustración: dice "no entiendo", "esto no funciona", "ya probé esto", repite la misma pregunta varias veces, tono cortante, o pide directamente parar.

Cuando eso pase, la prioridad deja de ser "terminar el próximo nivel" — pasa a ser esto, en orden:

1. **Parar de avanzar el roadmap.** No sigas al próximo nivel ni insistas con el paso que trabó.
2. **Buscá en `PROBLEMAS-FRECUENTES.md`** si el problema ya es conocido — puede resolverse ahí mismo, sin reportar nada nuevo.
3. **Si no está ahí, ofrecé una alternativa REAL, no la misma explicación con otras palabras.** Ejemplos: si un comando de terminal no anda, probá describirle los clicks a mano en vez de otro comando; si un concepto no cierra, probá con un ejemplo de su propia vida (lo sabés por el Nivel 00) en vez de repetir la definición.
4. **Si después de una alternativa real seguís trabado**, preguntale explícitamente: *"¿querés que dejemos esto anotado para que se mejore la guía? No hace falta que sigamos ahora."*
5. **Si dice que sí**, completá `PLANTILLA-REPORTE-PROBLEMA.md` y dejalo en uno de los dos lugares de abajo. Si dice que no, está bien — seguí donde la persona quiera, o cerrá la sesión sin insistir.

## Dónde dejar el registro

Dos lugares posibles, con la MISMA plantilla (`PLANTILLA-REPORTE-PROBLEMA.md`):

### Opción 1 — Discord (para charlarlo con más gente que está usando esto)

[discord.gg/TW5dvxGKqh](https://discord.gg/TW5dvxGKqh)

Postealo en el canal de dudas/soporte, con la plantilla completa. Alguien de ahí (o quien mantiene el proyecto) va a responder — y si es algo genuinamente nuevo, puede terminar en `PROBLEMAS-FRECUENTES.md` para que el siguiente no se trabe con lo mismo.

### Opción 2 — Issue de GitHub (si preferís algo más formal, o no usás Discord)

**Si tu agente tiene la herramienta `gh` (GitHub CLI) configurada:**

```
gh issue create --title "[nivel NN] resumen corto del problema" --body "[contenido de PLANTILLA-REPORTE-PROBLEMA.md ya completado]"
```

**Si no tiene `gh`, o no funciona:** guiá a la persona a hacerlo a mano — es 3 clicks:

1. Abrí el repo en el navegador (la URL que usaste para clonarlo).
2. Pestaña **"Issues"** (arriba).
3. Botón verde **"New issue"** — pegá ahí la plantilla completada.

## Qué NO poner en el reporte, sea Discord o GitHub

Nada personal de la persona (nombre real si no quiere, datos sensibles, capturas con información privada). El reporte es sobre la GUÍA, no sobre quién la está usando — describí el problema técnico o de explicación, nada más.
