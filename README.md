# Primeros pasos con tu agente

Esta guía no se lee sola. Se hace **hablando con tu agente**, en el orden que sigue. Cada nivel termina con un bloque de texto que le decís literalmente a tu agente para que haga el paso con vos.

## ⚠️ Prerequisito — leé esto ANTES de empezar

Esto **no funciona con un chat común** (ChatGPT en chatgpt.com, Claude en claude.ai, Gemini, etc.). Esos chats pueden hablar con vos, pero no pueden tocar archivos en tu computadora — y esta guía es, literalmente, crear y editar archivos junto a tu agente. Si intentás hacer esto en un chat común, el agente no va a poder ejecutar nada real: como mucho te va a *describir* qué archivo crearía, y ahí es donde la cosa empieza a andar en círculos (inventa una alternativa a mano, te promete algo que no puede cumplir, etc.).

Necesitás un **agente de código** — un programa que corre en tu computadora, que podés abrir apuntando a una carpeta, y que tiene permiso real para leer, crear y escribir archivos (y en niveles más avanzados, ejecutar comandos). Ejemplos:

- **Si usás Claude**: [Claude Code](https://claude.com/claude-code) (CLI o la app de escritorio). Es la opción con la que se armó y probó esta guía.
- **Si usás ChatGPT**: el **Codex CLI** de OpenAI (agente de código, distinto del chat web).
- Otras opciones válidas: Cursor (en modo agente), Windsurf, o cualquier herramienta que se describa a sí misma como "coding agent" / "agente de código" con acceso a archivos.

La mayoría de estas herramientas tiene alguna forma de prueba gratuita o plan gratuito — están cambiando seguido, así que anda directo a la página oficial de la que elijas y fijate la oferta actual en vez de confiar en un número que alguien te pasó de memoria.

**¿No estás seguro si lo que tenés abierto es esto?** El checkpoint del Nivel 00 es justo ese chequeo — 30 segundos, y si falla ahí, es que no tenés la herramienta correcta, no que algo esté mal con la guía.

Todo lo demás (memoria, base de conocimiento, vocabulario, tu propia forma de trabajar) lo vamos construyendo con archivos de texto simples, un nivel a la vez — con el agente correcto, ya elegido.

## Cómo usar esto

1. Abrí esta carpeta con tu agente.
2. Empezá por `niveles/00-fundamentos.md`.
3. Leé el nivel, hacé la acción con tu agente, confirmá el checkpoint.
4. Recién ahí pasá al siguiente. No te saltees niveles — cada uno da por hecho lo anterior.

## Índice

| Nivel | Qué resuelve |
|---|---|
| [00 — Fundamentos](niveles/00-fundamentos.md) | Qué es esto de "trabajar con un agente" |
| [01 — Memoria persistente](niveles/01-memoria-persistente.md) | Que tu agente no se olvide todo entre sesiones |
| [02 — Segundo cerebro](niveles/02-segundo-cerebro.md) | Una base de conocimiento que crece con el tiempo |
| [03 — Vocabulario y patrones](niveles/03-vocabulario-y-patrones.md) | Cómo organizar el trabajo sin perderte |
| [04 — Persona propia](niveles/04-persona-propia.md) | Que tu agente te hable como vos querés, y te frene cuando hace falta |
| [05 — Avanzado (opcional)](niveles/05-avanzado-opcional.md) | Para cuando ya tengas todo lo anterior andando |

## Por qué existe

Nace de una sesión real armando exactamente este sistema (memoria + base de conocimiento + patrones de trabajo + persona propia) desde cero, con resultado que funciona en uso real. Esta guía saca la parte específica de esa sesión y deja la forma genérica — para que cualquiera pueda armar la suya, no una copia de la de otro.
