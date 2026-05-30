# 😈 Abogado del Diablo

> La skill que vuelve a Claude en tu contra y le hace pedazos a tu idea.

**[English](./README.md) · Español**

Una skill (y plugin) de Claude Code que adopta el rol de un abogado del diablo
hostil: agarra tu idea, tu plan, tu pitch o un proyecto entero y lo critica a
fondo, sin validarte ni suavizar nada, hasta entregarte un veredicto con la lista
de qué arreglar primero.

Hecha por la comunidad [tododeia](https://www.tododeia.com).
Guía completa: **[tododeia.com/community/abogado-del-diablo](https://www.tododeia.com/community/abogado-del-diablo)**

---

## Por qué existe

Por defecto, Claude tiende a darte la razón. Valida, suaviza y le busca el lado
bueno a todo. Se siente bien y arruina decisiones. Cuando vas a apostar tiempo,
dinero o reputación, lo que necesitas no es un "guau, gran idea": necesitas que
alguien encuentre las grietas **antes** que el mercado.

Esta skill es ese alguien. Asume que tu idea va a fracasar y se propone
demostrarlo — no por crueldad, sino porque cada grieta que encuentra aquí es una
que ya no descubres tarde y caro.

## Qué hace

- **Prohíbe la adulación.** Nada de cumplidos, nada de "tiene potencial, pero…".
- **Ataca por ocho ángulos:** premisas falsas · mercado · competencia · viabilidad
  · números · ejecución · pre-mortem (cómo muere en 12 meses) · punto ciego.
- **Investiga** casos reales de ideas parecidas que fracasaron (cuando hay web).
- **Analiza proyectos enteros** en Claude Code (lee tus archivos) y puede lanzar
  subagentes en paralelo, uno por ángulo, para una demolición a fondo.
- **Cierra constructivo:** veredicto crudo → grietas por severidad → la que lo mata
  → qué arreglar primero. Brutal con la idea, nunca contigo.

## Instalación

### Opción A — Plugin de Claude Code (recomendado)

Dentro de una sesión de Claude Code:

```
/plugin marketplace add Hainrixz/abogado-del-diablo
/plugin install abogado-del-diablo@abogado-del-diablo
```

Luego invócalo con `/abogado-del-diablo`.

### Opción B — Skill manual

Copia la carpeta `skills/abogado-del-diablo/` a `~/.claude/skills/` (o a
`.claude/skills/` dentro de tu proyecto). O descarga el [`SKILL.md`](./SKILL.md) y
déjalo en `~/.claude/skills/abogado-del-diablo/SKILL.md`.

### Opción C — Sin instalar nada (chat / Cowork)

Pega el contenido de [`SKILL.md`](./SKILL.md) como primer mensaje en claude.ai o
Cowork, y debajo tu idea. Mismo abogado del diablo, sin instalar nada.

## Cómo se usa

```
/abogado-del-diablo

Quiero lanzar una app de suscripción de snacks saludables a $25 al mes.
```

Otras formas:

- **Sobre un proyecto entero:** `/abogado-del-diablo --proyecto`
- **Demolición a fondo (subagentes):** `/abogado-del-diablo --demolicion`
- **En lenguaje natural:** "hazle pedazos a esta idea sin filtros", "dime por qué
  va a fallar", "red team this".

## Qué vas a ver

```
VEREDICTO
Esto no es una startup, es un negocio de márgenes de abarrote disfrazado de tech,
y los números no cierran desde el día uno. Cuatro grietas, de la más letal a la menos:

1. La economía no cierra y es el problema número uno.
   - El golpe: ...
   - Por qué es letal: ...
   - Qué tendría que ser cierto: ...
...

LA QUE LO MATA
La economía unitaria.

SI INSISTES, ARREGLA ESTO PRIMERO
1. ...
```

Ejemplo completo en [`skills/abogado-del-diablo/references/ejemplos.md`](./skills/abogado-del-diablo/references/ejemplos.md).

## Estructura

```
abogado-del-diablo/
├── .claude-plugin/{marketplace.json, plugin.json}
├── commands/abogado-del-diablo.md          # el slash command
├── skills/abogado-del-diablo/
│   ├── SKILL.md                            # el cerebro de la skill
│   └── references/{angulos.md, ejemplos.md}
└── SKILL.md                                # copia para descarga / pegado directo
```

## Licencia

MIT. Úsalo, modifícalo, compártelo.

---

Construido por [tododeia](https://www.tododeia.com) y mantenido por
[@Hainrixz](https://github.com/Hainrixz). No está afiliado a Anthropic. Si te
salvó de una mala decisión, dale una estrella ⭐ y pásaselo a quien necesite que
alguien le diga la verdad.
