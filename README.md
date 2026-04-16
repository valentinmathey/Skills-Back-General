# 🚀 SKILLS GENERAL BACK

Bienvenido al repositorio de **Skills General Back**. Este proyecto es una colección estructurada de directrices, patrones de arquitectura, mejores prácticas y configuraciones maestras (*skills*) pensadas específicamente para potenciar agentes de IA enfocados en el **desarrollo Backend (Node.js, Express, APIs), Fullstack, Bases de Datos (Prisma, Postgres), Testing (Playwright) y Arquitectura de Software**. 

El objetivo de este repositorio es darle a tus asistentes de código el contexto experto que necesitan para escribir código limpio, seguro y escalable, adoptar los mejores patrones de la industria y evitar errores comunes, sin tener que brindarles explicaciones extensas en cada uno de tus proyectos.

---

## 📦 Instalación y Descarga de Skills

Para comenzar a utilizar este arsenal de *skills* en tus proyectos locales, el método oficial de instalación es utilizar la herramienta `npx` apuntando directamente a tu repositorio de GitHub. 

Ejecuta el siguiente comando en tu terminal para iniciar el proceso de instalación:

```bash
npx skills add valentinmathey/Skills-Back-General
```

Al ejecutarlo, se desplegará un menú interactivo en la consola con los siguientes pasos:

1. **Seleccionar Skills**: Se mostrará una lista con todas las habilidades disponibles. Usa la barra espaciadora para seleccionar las que necesites para tu proyecto.
2. **Seleccionar Agentes**: Elige en qué asistentes o IAs deseas que se instalen (puedes buscar y seleccionar conocidos como Gemini, Claude, Codex, Antigravity, Cursor, entre otros).
3. **Alcance de Instalación (Scope)**: 
   - **Project**: Instala las skills en el directorio actual (ideal para hacer commit junto con tu proyecto).
   - **Global**: Las instala de manera global.
4. **Método de Instalación**:
   - **Symlink (Recomendado)**: Crea enlaces simbólicos. Mantiene una única fuente de verdad y facilita las actualizaciones.
   - **Copy to all agents**: Copia físicamente los archivos a los directorios de los agentes seleccionados.

---

## 🛠️ Crea tus Propias Skills

Crear nuevas habilidades y extender el conocimiento de tus agentes es muy sencillo. Para facilitarlo, hemos incluido un agente creador dentro de este mismo repositorio:

**Usa el Skill Creator**
Puedes apoyarte en la skill [Skill Creator](./skills/skill-creator/SKILL.md) que hemos diseñado específicamente para que te ayude a armar y estructurar nuevas skills más rápido.

**Pasos básicos:**
1. Crea una carpeta nueva dentro de `skills/` (ej. `mis-reglas-nest`).
2. Crea el archivo principal llamado `SKILL.md` dentro de ella.
3. **Pídele a la IA que redacte la skill por ti**: Envíale un prompt en tu editor o agente de IA similar a este:
   
   > *"Usa el [Skill Creator](./skills/skill-creator/SKILL.md) y el template de skills para crear una nueva habilidad en esta carpeta. La nueva skill tratará sobre [explica aquí el contexto de lo que quieres, ej. validaciones de datos en nuestro equipo]."*
   
   Con esto, la IA estructurará el `SKILL.md` con los metadatos correctos, redactará las directrices y te dejará una base sólida lista para usar.
4. **¡Listo!** En cuanto revises y subas los cambios a GitHub, tus agentes podrán usar tu nueva regla.

---

## ⚙️ Cómo usar Autoskills en cada proyecto

Una vez tengas o necesites implementar estas skills, la forma ideal de activarlas de manera inteligente según el stack tecnológico de tu proyecto actual, es utilizando la CLI de **Autoskills**. 

### 1. Instalación Global

Primero, asegúrate de instalar las herramientas base instalando el paquete globalmente:

```bash
npm install -g skills
```

### 2. Ejecución Inteligente (Auto-Detección)

Dirígete a la carpeta principal de tu proyecto de código (donde esté tu `package.json` u otros archivos de configuración) y ejecuta:

```bash
npx autoskills
```

Esto realizará un rápido análisis automático de las herramientas que estás utilizando e instalará las mejores skills correspondientes a tu stack de manera autónoma.

### 3. Instalación para Agentes Específicos

Si solo utilizas algunos editores o IAs en particular, y no deseas instalar las reglas para todo el ecosistema, puedes indicar con precisión a qué asistentes inyectarle las reglas utilizando el modificador `-a`:

```bash
npx autoskills -a cursor claude-code
```

---

## 🖥️ Comandos Adicionales del CLI (Opciones)

Al utilizar `autoskills`, dispones de parámetros adicionales (como muestra la consola y la foto de referencia) que te permiten tener un mayor rango de control:

| Bandera (Flag) | Descripción |
| :--- | :--- |
| `-y, --yes` | Salta el prompt de confirmación y acepta instalar todo automáticamente (ideal para CI/CD). |
| `--dry-run` | Hace una simulación. Muestra qué skills se van a instalar según tu proyecto, pero no realiza ninguna descarga real. |
| `-v, --verbose` | Modo detallado. Útil si algo falla y necesitas ver la traza completa del error en la instalación. |
| `-a, --agent` | Comando fundamental para configurar las skills para IDEs o agentes de software exclusivos (ej. `cursor`, `claude-code`). |
| `-h, --help` | Despliega este menú de ayuda en la terminal. |

---

## 🙏 Agradecimientos Especiales

Gran parte del ecosistema conceptual, estructura base y ejecución por consola de este proyecto le debe mucho al excelente trabajo de **AutoSkills**. Agradecemos inmensamente su infraestructura y aportes para la construcción de agentes modulares de manera sencilla.

Puedes visitar todo lo que ofrecen y su proyecto en:
🌐 **[https://www.autoskills.sh/](https://www.autoskills.sh/)**
