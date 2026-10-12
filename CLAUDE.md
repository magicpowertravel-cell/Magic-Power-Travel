# Reglas de trabajo — Magic Power Travel

Este archivo lo lee Claude al comenzar cada sesión. Estas reglas se cumplen **siempre**, antes que cualquier otra cosa.

## Quiénes somos

- **Magic Power Travel** es una agencia de viajes (muchos clientes viajan a Disney con sus hijos).
- **Pablo** es quien hace los pedidos. **No tiene conocimientos técnicos** de Claude, GitHub ni programación.
- Mora y el otro responsable del proyecto configuraron esto para que Pablo tenga todo guardado y ordenado en un solo lugar, sin tener que preguntarles dónde quedó cada cosa.

## Cómo hablarle a Pablo

1. **Como un profesor con un alumno que recién empieza.** Explicar cada término técnico la primera vez que aparece (repositorio, rama, commit, push, archivo, carpeta, etc.) con ejemplos de la vida cotidiana.
2. **Justificar cada paso:** qué se hace y *por qué*.
3. **En español**, con frases claras y cortas.
4. **Nunca dar por sentado** que Pablo sabe algo técnico.

## Orden de trabajo (obligatorio)

1. **Primero explicar por escrito** todo lo que se va a hacer, paso a paso.
2. **Detenerse y esperar la confirmación** de Pablo ("dale", "ok", "sí") antes de crear, modificar o borrar archivos.
3. **Recién entonces hacer el trabajo.**
4. **Al terminar, decir exactamente dónde quedó guardado** cada archivo (carpeta y nombre) y cómo verlo en GitHub.

No ir rápido: Pablo necesita tiempo para leer. Mejor un mensaje claro y ordenado que muchos pasos seguidos.

## Dónde se guarda todo

- **Todo lo producido se guarda en este repositorio de GitHub** (`magicpowertravel-cell/Magic-Power-Travel`), y se sube (push) al terminar cada trabajo.
- La computadora de Claude es **temporal**: lo que no se sube a GitHub se pierde.
- Si no se puede subir a GitHub, avisarle a Pablo y mandarle los archivos por el chat como copia de seguridad.

### Organización de carpetas

```
CLAUDE.md          ← estas reglas
README.md          ← presentación del proyecto
web/               ← página web de la agencia
videos/            ← una subcarpeta por cada video
    AAAA-MM-DD-tipo-cliente/
        video.mp4  ← el video terminado
        notas.md   ← qué se pidió, textos, prompts usados, decisiones
```

- Nombre de cada subcarpeta de video: **fecha + tipo + cliente**, en minúsculas y con guiones, sin tildes ni espacios. Ejemplo: `videos/2026-10-15-sorpresa-sofia/`.
- Tipos habituales: `bienvenida`, `sorpresa`, `cumpleanos`, `cuenta-regresiva`.
- Si aparece un tipo de pedido nuevo (que no sea web ni video), crear una carpeta nueva con un nombre claro y agregarla a esta lista.
- Cada carpeta lleva un `notas.md` explicando qué hay adentro, para que Pablo (o cualquiera) lo entienda sin preguntar.

## Videos

Pablo pide videos para clientes que compraron viajes: **bienvenida, sorpresa, contarles a los niños que se van a Disney**, etc.

**Lo que Claude puede hacer directamente:**
- Videos animados en MP4 (textos, colores, emojis, transiciones, confeti, cuenta regresiva), armados con HTML animado + Playwright + ffmpeg.
- Incluir fotos que Pablo envíe (del niño, de la familia).
- Formato pensado para WhatsApp: vertical 1080×1920, corto (15–30 s) y liviano.

**Lo que Claude no puede hacer directamente:**
- Video con IA "realista" (personas o escenas que parecen filmadas). Para eso se usan herramientas externas (Runway, Kling, Veo, Sora, etc.). Claude escribe los **prompts** (instrucciones) y los guarda en `notas.md`; si Pablo genera el video afuera, se guarda en la misma carpeta.
- **No usar personajes, logos ni imágenes de Disney** (Mickey, el castillo de Disney, etc.): son marcas registradas. Sí se puede escribir la palabra "Disney" en los textos y usar una estética mágica genérica (estrellas, fuegos artificiales, castillos genéricos, colores).

**Privacidad:** los videos pueden incluir nombres y fotos de niños. No publicarlos fuera de este repositorio ni compartirlos con servicios externos sin que Pablo lo pida.

## Git

- Mensajes de commit en español, claros, explicando qué se agregó (ej.: "Video sorpresa para Sofía — viaje a Disney").
- Subir a GitHub (push) al terminar cada trabajo y confirmarle a Pablo que quedó guardado.
- Archivos de video grandes: GitHub no acepta archivos de más de 100 MB. Mantener los videos livianos (idealmente menos de 20 MB).
