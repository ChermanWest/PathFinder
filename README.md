PathFinder es un sistema inteligente y portable de asistencia a la navegación peatonal para personas con discapacidad visual. Integra detección de obstáculos en tiempo real con alertas hápticas (ESP32) y comprensión del entorno y navegación por voz mediante IA

//placeholder//

PathFinder/
├── docs/                      # Documentación del proyecto
│   ├── diagramas/             # Diagramas de casos de uso, secuencias, etc.
│   ├── manual_usuario.pdf     # Manual de usuario final
│   └── reportes/              # Informes y bitácoras de avance
├── hardware/                  # Archivos físicos y de diseño
│   ├── 3d_models/             # Archivos de Blender y STL (gafas y pechera)
│   └── schematics/            # Esquemáticos de circuitos y cableado
├── src/                       # Código fuente del sistema
│   ├── esp32_obstacle_alert/  # Módulo B: Capa reactiva local
│   │   ├── src/               # Código principal en C++/Arduino
│   │   ├── lib/               # Librerías para ToF VL53L1X, MPU-6050 y motores
│   │   └── platformio.ini     # (Opcional) Archivo de configuración si usan PlatformIO
│   ├── rpi_voice_nav/         # Módulo A: Capa de comprensión y navegación
│   │   ├── src/               # Scripts principales (probablemente en Python)
│   │   ├── config/            # Archivos de configuración (claves de API Gemini, etc.)
│   │   └── requirements.txt   # Dependencias de software para Raspberry Pi OS
│   └── shared/                # (Opcional) Protocolos de comunicación entre RPi y ESP32
├── unity_mockup/              # Maqueta virtual del entorno urbano
│   ├── Assets/                # Modelos, scripts en C# y escenas de Unity
│   └── ProjectSettings/       # Configuración para Meta Quest 3
├── .gitignore                 # Exclusiones de archivos compilados y credenciales
└── README.md                  # Página principal del repositorio

(seciones que despues debe tener el readmi

Descripción General: Un resumen del propósito del proyecto y cómo actúa como complemento al bastón blanco.

Arquitectura del Hardware:

    Capa Local (ESP32): Explica su rol en la detección inmediata (sensores ToF) y alertas hápticas offline (menos de 100ms de latencia).

    Capa de Comprensión (Raspberry Pi 4): Explica la integración con micrófonos, GPS, cámaras y la API de Gemini Vision para la navegación y consultas del entorno.

Requisitos Previos: Lista de componentes principales (Raspberry Pi 4, ESP32-S3, sensores, power bank) y software necesario (Arduino IDE, librerías específicas, Python).

Instrucciones de Instalación:

    Cómo configurar y compilar el entorno del ESP32.

    Cómo configurar el entorno virtual e instalar las dependencias en la Raspberry Pi.

    Advertencia sobre cómo configurar las variables de entorno para las claves de la API de Gemini (para que no se suban al código público).

Organización del Equipo: Mención breve de los Módulos A y B para que quien lea el código entienda el flujo de trabajo.
