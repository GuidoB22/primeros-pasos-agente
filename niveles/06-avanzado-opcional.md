# 🧭 Nivel 06 — Avanzado (opcional)

Este nivel es lectura, no tiene checkpoint obligatorio. Volvé acá cuando lo de antes ya te quede chico.

## Upgrade de memoria: de un archivo a un sistema real

El `memoria.md` del Nivel 02 funciona, pero no escala bien: se hace largo, no se puede buscar bien, y no se comparte fácil entre proyectos distintos. El upgrade natural es un sistema de memoria persistente dedicado (por ejemplo, un MCP de memoria) que guarda, busca y organiza por vos. El concepto de fondo no cambia — sigue siendo "el agente lee al empezar, escribe al cerrar" — solo lo hace mejor a escala.

## Upgrade de segundo cerebro: ¿todavía no instalaste Obsidian?

Si en el Nivel 03 elegiste seguir con archivos de texto plano en vez de instalar Obsidian, ese es el momento de volver — la guía completa de instalación (con los clicks exactos que tenés que dar vos) está ahí, sección "Instalando Obsidian". Si ya la hiciste, no hay nada más que agregar acá.

## Si automatizás tareas: el problema de dos procesos tocando lo mismo a la vez

Cuando empezás a tener tareas automáticas/programadas (no solo conversaciones en vivo) que tocan los mismos archivos, puede pasar que dos corran casi al mismo tiempo y se pisen entre sí — una sobreescribe lo que la otra estaba por guardar.

La solución simple: un "candado" por carpeta. Antes de tocar los archivos compartidos, cada tarea intenta crear una carpeta con un nombre fijo (por ejemplo `.trabajando/`). Crear una carpeta es una operación que o funciona o falla — nunca "funciona a medias" — así que sirve de señal: si ya existe, significa que otra tarea la está usando, y hay que esperar o saltear ese turno. Al terminar, se borra la carpeta para liberar el paso.

```mermaid
flowchart TB
    T1["Tarea A"] --> C1{"¿Existe .trabajando/?"}
    T2["Tarea B"] --> C2{"¿Existe .trabajando/?"}
    C1 -- no --> W1["Crea la carpeta y trabaja"]
    C2 -- sí, ya la creó A --> S2["Espera o se salta este turno"]
    W1 --> R["Borra la carpeta al terminar"]
```

No hace falta nada de esto hasta que tengas más de una tarea automática tocando los mismos archivos — antes de eso, es complejidad de más.

## Evitar releer algo que no cambió

Parecido al candado de arriba, pero para otro problema: si tu agente tiene que consultar un recurso externo (otro repo, una base de conocimiento compartida, un documento largo) para ver si hay algo nuevo, la forma ingenua es releerlo entero cada vez — lento, y gasta proceso de más cuando la mayoría de las veces no cambió nada.

La solución simple: guardar un "marcador de la última vez que lo viste" y comparar antes de leer.

```mermaid
flowchart LR
    A["¿Guardaste un marcador la última vez?"] -->|sí| B["Comparalo contra el estado actual del recurso"]
    B -->|"igual"| C["No hay nada nuevo — cortá acá, no releas nada"]
    B -->|"distinto"| D["Traé SOLO lo que cambió, no todo de nuevo"]
    D --> E["Actualizá el marcador"]
    A -->|"no, primera vez"| F["Leé todo una vez y guardá el marcador"]
```

Si el recurso es un repo de git, el marcador más simple es el **SHA del último commit que viste** — es un identificador único y siempre creciente, perfecto para esto. El patrón completo:

1. Guardar el SHA visto en un archivo local (no versionado, es solo tu propio marcador).
2. Antes de consultar: preguntar el SHA actual del recurso y compararlo contra el guardado.
3. Si es igual: no hay nada nuevo, cortar ahí — no leer nada más.
4. Si es distinto: traer solo el diff entre el SHA viejo y el nuevo (no todo el contenido de nuevo).
5. Actualizar el marcador al SHA nuevo, haya habido novedades o no.
6. Ofrecerte lo que encontró — nunca incorporarlo solo, sin que decidas vos.

> [!TIP]
> 🧭 **Decile esto a tu agente (si tenés un recurso externo que consultás seguido):**
>
> ```
> Quiero que antes de releer [el recurso que sea] completo, guardes
> un marcador de la última versión que viste (si es un repo git, usá
> el SHA del último commit). La próxima vez, comparalo contra el
> estado actual: si no cambió nada, no releas nada y decímelo en una
> línea. Si cambió, traeme solo lo nuevo, no todo de nuevo — y
> actualizá el marcador después.
> ```
