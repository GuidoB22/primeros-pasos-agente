# Si algo no funciona o te frustra — esto es normal, y es útil

Esta guía es un proyecto vivo, no un producto terminado. Si te trabaste, no entendiste algo, o simplemente te dio bronca — **eso no es un fracaso tuyo**, es información real de que algo hay que mejorar. Quien la armó lo espera y lo quiere saber.

## Para el agente: qué hacer si la persona se frustra

Señales de frustración: dice "no entiendo", "esto no funciona", "ya probé esto", repite la misma pregunta varias veces, tono cortante, o pide directamente parar.

Cuando eso pase, la prioridad deja de ser "terminar el próximo nivel" — pasa a ser esto, en orden:

1. **Parar de avanzar el roadmap.** No sigas al próximo nivel ni insistas con el paso que trabó.
2. **Ofrecé una alternativa REAL, no la misma explicación con otras palabras.** Ejemplos: si un comando de terminal no anda, probá describirle los clicks a mano en vez de otro comando; si un concepto no cierra, probá con un ejemplo de su propia vida (lo sabés por el Nivel 00) en vez de repetir la definición.
3. **Si después de una alternativa real seguís trabado**, preguntale explícitamente: *"¿querés que dejemos esto anotado para que se mejore la guía? No hace falta que sigamos ahora."*
4. **Si dice que sí**, dejá un registro concreto (ver abajo cómo). Si dice que no, está bien — segui donde la persona quiera, o cerrá la sesión sin insistir.

## Cómo dejar el registro (para que la guía mejore de verdad)

La forma correcta es un **issue de GitHub en este mismo repo** — no un mensaje directo a nadie. Así queda escrito, con contexto, y quien mantiene la guía lo ve sin que dependa de que alguien se acuerde de avisarle.

**Si tu agente tiene la herramienta `gh` (GitHub CLI) configurada:**

```
gh issue create --title "[nivel NN] resumen corto del problema" --body "Qué se intentó: ...
Qué pasó: ...
Qué se esperaba que pasara: ..."
```

**Si no tiene `gh`, o no funciona:** guiá a la persona a hacerlo a mano — es 3 clicks:

1. Abrí el repo en el navegador (la URL que usaste para clonarlo).
2. Pestaña **"Issues"** (arriba).
3. Botón verde **"New issue"** — poné como título en qué nivel pasó, y en la descripción qué se intentó, qué pasó, y qué se esperaba.

## Qué NO poner en el issue

Nada personal de la persona (nombre real si no quiere, datos sensibles, capturas con información privada). El issue es sobre la GUÍA, no sobre quién la está usando — describí el problema técnico o de explicación, nada más.
