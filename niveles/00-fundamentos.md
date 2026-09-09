# Nivel 00 — Fundamentos

## Qué es esto

Un agente de código no es solo un chat: además de responderte, puede **leer y escribir archivos reales en tu computadora**, dentro de la carpeta donde lo abriste. Todo lo que vas a construir en los próximos niveles — memoria, base de conocimiento, tu forma de trabajar — no es "configuración mágica": son archivos de texto simples que vos y tu agente leen y escriben juntos.

```mermaid
flowchart LR
    A[Vos: mensaje] --> B[Agente]
    B --> C[Lee / escribe archivos]
    C --> D[Vos ves el resultado]
    D --> A
```

Ese ciclo — vos pedís, el agente toca archivos reales, vos ves el resultado — es la base de TODO lo que sigue.

## Antes de seguir

Confirmá que tu agente puede efectivamente leer y escribir en esta carpeta. Es un chequeo de 30 segundos, pero si falla acá, nada de lo que sigue va a funcionar.

## Checkpoint

El agente crea el archivo, y cuando le pedís que te diga qué dice, te repite el contenido correcto (no inventado).

---

### Decile esto a tu agente:

```
Creá un archivo llamado hola.md en esta carpeta, con el texto
"Primer contacto: [fecha de hoy]". Después leelo y decime qué dice.
```
