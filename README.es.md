
---

## 1. Mis necesidades y contexto 

### ¿En qué tipo de proyectos trabajo?
| Proyecto | Tipo | Stack |
|---|---|---|
| **El Puesto de la Dieta** (tienda online para un cliente) | Aplicación en producción, mantenida a medio plazo | React + Vite, Shopify Storefront API (GraphQL), Supabase, desplegada en Netlify (empecé en Vercel, pero su plan gratuito no permite uso comercial) |
| **Salpicados** (videojuego de plataformas, en desarrollo) | Proyecto personal, lógica de juego y assets | Phaser 3, JavaScript |
| **App para mascotas**  | Aplicación pequeña/mediana: diario de salud, calendario de vacunas, recordatorios, perfil de cada animal | React, Supabase (auth, base de datos y almacenamiento de fotos/documentos) |
| **Portfolio** y prototipos rápidos | Webs estáticas / prototipos | HTML/CSS/JS, GitHub Pages |

### ¿Para qué tareas quiero usar Vibe Coding?
- **Desarrollo y depuración** de código dentro de repositorios que ya existen (React, JavaScript).
- **Generación de UI** rápida: pantallas de la app de mascotas, componentes de la tienda, landings.
- **Lógica de juego**: físicas, colisiones, niveles y escenas en Phaser 3.
- **Backend sencillo**: modelado de datos en Supabase (mascotas, vacunas, citas veterinarias, entradas del diario).

### Mis limitaciones
- **Presupuesto**: limitado → prioridad a planes gratuitos o una sola suscripción.
- **Stack existente**: React, Supabase, Netlify, GitHub Pages, GitHub. 
- **Código entregable a terceros**: la tienda pertenece al cliente. El código tiene que ser legible, mantenible y exportable.
- **Entorno**: Windows + VS Code + GitHub Codespaces.
- **Condiciones de uso**: reviso que el plan gratuito permita uso comercial; por eso la tienda pasó de Vercel a Netlify.

---

## 2. Preselección de herramientas 

1. **Claude Code** – agente de código en terminal/VS Code; trabaja directamente sobre mis repositorios.
2. **Cursor** – IDE con IA basado en VS Code.
3. **Windsurf** – IDE agéntico, alternativa directa a Cursor.
4. **Vercel v0** – generación de UI en React/Tailwind; el código generado se copia a mi repositorio, así que no me ata al hosting de Vercel.
5. **GitHub Copilot** – integrado en VS Code y Codespaces; plan gratuito para estudiantes.
6. **Lovable** – constructor de apps completas con integración de Supabase (candidato para prototipar la app de mascotas).

---

## 3. Tabla de puntuación 


| Herramienta | UI/UX | Costo | Velocidad | Dependencia de Plataforma | Control | Mantenibilidad | Calidad del Código | Reutilización | **Mi calificación (1-5)** | Notas / Justificación |
|---|---|---|---|---|---|---|---|---|---|---|
| Vercel v0 | 5 | 3 | 5 | 2 | 2 | 1 | 5 | 1 | **3** | Muy útil para maquetar pantallas de la app de mascotas (perfil, ficha de vacunas, diario) y componentes de la tienda. No lo usaría para lógica ni backend. |
| Replit | 4 | 1 | 4 | 1 | 1 | 3 | 5 | 1 | **1** | Fuerte dependencia de su plataforma y coste alto.  |
| Lovable | 5 | 3 | 4 | 2* | 3 | 3 | 4 | 1 | **3** | Su integración con Supabase encaja con la app de mascotas: podría tener un prototipo funcional (login, perfiles, vacunas) muy rápido. Para la versión definitiva prefiero pasar a mi repositorio con control total. *Lo puntúo 2 porque exporta a GitHub, pero el flujo está pensado para quedarse en su plataforma. |
| Windsurf | 3 | 5 | 3 | 5 | 5 | 5 | 5 | 5 | **3** | Buenas puntuaciones, pero cubre lo mismo que Cursor/Claude Code. |
| Cursor | 2 | 4 | 3 | 5 | 4 | 5 | 4 | 5 | **4** | Trabaja sobre mis repositorios y es casi VS Code. Buena opción si quisiera un IDE con IA integrado. |
| **Claude Code** | 2 | 3 | 4 | 5 | 5 | 5 | 5 | 5 | **5** | Trabaja en el repositorio, en terminal o VS Code, sin plataforma propia. Ideal para tareas multiarchivo. |
| **GitHub Copilot** | 3 | 5 | 4 | 4 | 4 | 4 | 4 | 5 | **4** | Autocompletado en VS Code y Codespaces, gratis para estudiantes.  |
| **Phaser 3 + librerías (sin IA)** | 2 | 5 | 2 | 5 | 5 | 5 | 5 | 5 | **4** |  Phaser ya resuelve físicas, sprites y escenas; la IA me ayuda a escribir el código, pero no sustituye al motor. |

---

## 4. Mi kit de herramientas elegido 

| Rol | Herramienta | Por qué |
|---|---|---|
| **Principal** | **Claude Code** | Ingeniería real sobre mis repositorios: features, depuración y refactor en la tienda, el juego y la app de mascotas. |
| **Apoyo diario** | **GitHub Copilot** | Autocompletado rápido en VS Code/Codespaces, coste cero. |
| **Puntual (UI / prototipo)** | **Vercel v0** (plan gratuito) | Prototipar pantallas y componentes y copiarlos a mi proyecto, revisándolos antes. Lovable como opción para validar la idea de la app de mascotas. |
| **Bibliotecas** | Phaser 3, Supabase, Tailwind, shadcn/ui | Cuando una librería resuelve el problema, es más barata y controlable que una herramienta de IA. |

**Descartadas por ahora**: Replit (dependencia de plataforma y coste), Windsurf (redundante con Cursor/Claude Code). Cursor queda como alternativa si en algún momento prefiero un IDE con IA en vez de un agente.

---

## 5. Principios que aplico

- **¿"Vibing" o ingeniería?** – v0 o Lovable para explorar la idea de la app de mascotas (vibing); Claude Code para lo que va a producción, como la tienda del cliente (ingeniería).
- **Pocas herramientas, bien dominadas** – un agente principal + un autocompletado, no cinco suscripciones.
- **No olvidar las bibliotecas** – Phaser para el juego y Supabase para auth y datos antes que reinventarlos con IA.
- **Ciclo de vida completo** – la IA también me sirve para documentar, escribir tests y preparar el despliegue, no solo para construir.
- **El toque humano** – reviso cada cambio, pruebo en local y en los deploy previews de Netlify antes de tocar la tienda del cliente; en la app de mascotas, compruebo a mano que las fechas de vacunas y recordatorios se calculan bien.

---

