# 🧠 M-IA (Modular Intelligent Agent)

**M-IA** no es un simple chatbot; es un **operador autónomo** diseñado para cerrar la brecha entre la instrucción y la ejecución. Este proyecto nace de la comunidad de JCyShart para crear una IA con "memoria" (persistencia de datos) y capacidades modulares que pueda interactuar con diversos entornos.

---

## 🚀 Filosofía del Proyecto
**M-IA** se basa en:
1. **Instrucción → Evaluación → Ejecución → Reporte:** Un flujo de trabajo claro y predecible.
2. **Persistencia de Datos:** Uso de bases de datos para que la IA tenga memoria a largo plazo y no "olvide" lo aprendido.
3. **Modularidad:** Un registro de acciones que permite expandir las capacidades de la IA sin reescribir el núcleo.

## 🛠️ Ecosistema Multilenguaje (Agnóstico)
M-IA está diseñado para ser **independiente del lenguaje**. Fomentamos la colaboración en:

* **Core (Python):** Gestión de modelos de lenguaje y lógica de razonamiento.
* **Bridge (Bun / JS):** alta velocidad para comunicación en tiempo real (WebSockets).
* **Modules (Cualquier lenguaje):** Las "habilidades" de la IA pueden ser scripts independientes en Go, Rust, Node.js o Python.
  
## 📂 Estructura del Proyecto
```text
M-IA/
├── main.py                # Orquestador principal y punto de entrada
├── brain/                 # EL CEREBRO (Python): Lógica de razonamiento y conexión con Gemini
│   ├── core/              # Procesamiento de lenguaje natural
│   └── logic/             # Toma de decisiones y evaluación
├── memory/                # LA MEMORIA (SQLite): Base de datos para persistencia de experiencias
│   └── database.db        # Archivo compartido de conocimiento
├── actions/               # LAS MANOS (Agnóstico): Habilidades ejecutables en cualquier lenguaje
│   ├── roblox/            # Scripts en Luau para integración con el motor
│   ├── tools/             # Scripts en Go, JS (Bun) o Python para tareas del sistema
│   └── templates/         # Guías para crear nuevas acciones
├── bridge/                # EL PUENTE: Protocolos de comunicación (JSON / WebSockets)
│   └── schema.json        # Estándar de mensajes para que todos los módulos se entiendan
└── logs/                  # REGISTROS: Historial de sesiones y aprendizaje de la IA
