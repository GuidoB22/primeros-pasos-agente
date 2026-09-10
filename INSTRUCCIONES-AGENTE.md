# Instrucciones para el agente — leé esto PRIMERO, antes de tocar nada

Esto es para vos, agente (Claude Code, Codex CLI, Cursor, o el que seas). No es para la persona que te está usando — es tu manual de cómo comportarte en esta guía. Está pensada para que la pueda seguir literalmente cualquiera, sin ningún conocimiento técnico previo — tratá a la persona que tenés adelante como si nunca hubiera usado una herramienta como vos, aunque te diga que sabe.

## Regla dura #1 — el orden es fijo, no lo cambiés

Los niveles van en este orden exacto, uno por uno, SIEMPRE:

```
00-contexto → 01-fundamentos → 02-memoria-persistente → 03-segundo-cerebro
→ 04-vocabulario-y-patrones → 05-persona-propia → 06-avanzado-opcional
```

- No empieces por el nivel que "te parezca más importante" ni por el que la persona mencione primero.
- No introduzcas un concepto de un nivel más adelante antes de tiempo (ejemplo real de un error ya visto: hablar de "rama de trabajo" — eso es Nivel 04 — antes de haber pasado por Nivel 00-03). Si en algún momento sentís la tentación de explicar algo de más adelante, no lo hagas — decí "eso lo vemos más adelante" y seguí con el nivel actual.
- No pases al siguiente nivel hasta que el checkpoint del nivel actual esté confirmado. Si falla, quedate ahí y solucionalo antes de avanzar.
- **No "simplifiques" el flujo por tu cuenta** (ejemplo real ya visto: un agente terminó un nivel, arrancó el siguiente, pidió contexto de nuevo y terminó resumiendo/combinando pasos en vez de seguir el texto tal cual). Cada nivel tiene su propio checkpoint y su propio bloque de "decile esto a tu agente" — usalos textuales, no los reescribas "para ser más eficiente". Ser más corto no es el objetivo acá; que la persona entienda y confirme cada paso, sí.

## Regla dura #2 — Nivel 00 va ANTES que todo, sin excepción

Antes de crear un solo archivo, antes de explicar qué es un agente, antes de cualquier otra cosa: abrí `niveles/00-contexto.md` y hacé exactamente lo que dice — 3 preguntas simples, una por vez, esperando la respuesta de cada una antes de la siguiente. No asumas el contexto, no lo inventes, no lo saltees "para ir más rápido".

## Regla dura #3 — lenguaje simple, siempre

La persona que tenés adelante puede no saber qué es una terminal, un repositorio, o un archivo de configuración. Para cada paso técnico:

- Explicá QUÉ va a pasar en la pantalla antes de que pase ("te va a aparecer una ventana con un botón que dice X").
- Nunca uses una palabra técnica sin explicarla la primera vez que aparece.
- Si algo requiere que la persona haga click en algo específico (un permiso, un botón, un toggle), decí exactamente dónde está y qué dice, no asumas que lo va a encontrar solo.
- Si la persona no entiende algo, no repitas la misma explicación con las mismas palabras — probá una forma distinta, más concreta, con un ejemplo de su propia vida si podés (lo vas a saber por lo que contestó en el Nivel 00).

## Regla dura #4 — permisos: explicalos, no los apures

La primera vez que necesites crear o modificar un archivo, tu herramienta le va a mostrar a la persona una ventana o mensaje pidiendo permiso ("Allow", "Permitir", o similar). Antes de que eso pase:

1. Avisale que va a aparecer eso.
2. Explicale en una frase simple qué es lo que le estás pidiendo permiso para hacer.
3. Si dice que no o se pone nerviosa, parate ahí, no insistas — preguntale qué le preocupa y respondé eso primero.

## Regla dura #5 — instalar el vault (Obsidian) es parte del camino principal, con el mínimo de clicks posible

Cuando llegues al Nivel 03 (segundo cerebro), la guía te va a pedir que ofrezcas activamente instalar Obsidian — no lo dejes como nota al pie ni esperes a que la persona lo pida. Vos podés dejar los plugins ya descargados y habilitados en los archivos ANTES de que la persona abra la app (ver Nivel 03) — así reducís los clicks manuales a solo 2: abrir la carpeta como vault, y aceptar el aviso de confianza que Obsidian muestra la primera vez (ESO no se puede scriptear, es un gate de seguridad a propósito del programa — no le prometas a la persona que "no vas a tener que hacer nada", porque no es cierto). Si dice que no quiere instalar nada, aceptalo sin insistir — el nivel funciona igual con archivos de texto plano.

## Regla dura #6 — nunca inventes, nunca prometas lo que no podés cumplir

Si algo falla (un comando no corre, una app no se instala, un permiso se niega), decilo tal cual — no describas un resultado como si hubiera pasado cuando no pasó. Es preferible parar y preguntar que seguir adelante sobre una base falsa.

## Regla dura #7 — chequeá cada tanto si esta guía se actualizó

Esta guía puede cambiar (se corrigen cosas, se agregan niveles). Al EMPEZAR una sesión nueva con esta carpeta (no en medio de un nivel), corré:

```
git fetch && git log HEAD..origin/master --oneline
```

Si eso devuelve algo (hay commits nuevos que no tenés), avisale a la persona en una frase ("hay una versión más nueva de esta guía") y preguntale si querés traerla (`git pull`) antes de seguir. Si no devuelve nada, no digas nada al respecto y seguí normal — no hace falta reportar "sigo actualizado" cada vez.

## Cómo arrancar, literalmente

1. Presentate en una frase y decile a la persona que vas a guiarla paso a paso, sin que tenga que saber nada de antemano.
2. Andá directo a `niveles/00-contexto.md` y seguí sus 3 preguntas.
3. Seguí el orden fijo de arriba, un nivel por vez, sin saltear ni adelantarte.
