# Prácticas de Sistemas Operativos (SO) - UPM ETSISI

Este repositorio contiene la suite de prácticas de laboratorio resueltas y documentadas para la asignatura **Sistemas Operativos** de la Escuela Técnica Superior de Ingenieros de Sistemas Informáticos (ETSISI) de la Universidad Politécnica de Madrid (UPM).

* **Alumno:** Yzan Martínez Manzano
* **Matrícula / ID:** br0285
* **Universidad:** Universidad Politécnica de Madrid (UPM)
* **Entorno de ejecución:** MINIX 3.1.2 emulado bajo QEMU / Entorno Unix/Linux

---

## 🛠️ Estructura del Repositorio y Explicación del Proyecto

```text
.
├── Práctica 1/        # Entorno, SSH/QEMU y Recompilación del Kernel MINIX
│   │                  # Explicación:
│   │                  # Configuración del entorno de virtualización con QEMU y acceso remoto por SSH.
│   │                  # Modificación del código fuente del kernel de MINIX en `/usr/src/kernel/main.c` 
│   │                  # para inyectar un banner personalizado durante el arranque y verificar la 
│   │                  # recompilación en los registros del sistema (`/var/log/messages`).
│   ├── main.c
│   └── docs/
│
├── Práctica 2/        # Introducción a C, Preprocesador, Makefiles y Memoria Dinámica
│   │                  # Explicación:
│   │                  # Fundamentos de programación en C bajo POSIX. Inspección de fases de compilación 
│   │                  # (`gcc -E` / `cpp`), sustitución de macros y compilación condicional.
│   │                  # Automatización modular con `Makefile` y simulación de la tabla de procesos (BCP) 
│   │                  # mediante `struct proceso` con gestión dinámica de memoria (`malloc`/`free`).
│   ├── Makefile
│   ├── procesos.c
│   └── procesos.h
│
├── Práctica 2.1/      # Gestión de Procesos (fork, wait, exit) y Reparto de Carga
│   │                  # Explicación:
│   │                  # Creación y control de procesos concurrentes usando llamadas al sistema nativas.
│   │                  # Algoritmo de reparto equitativo de rangos de trabajo entre procesos trabajadores 
│   │                  # (`p_trabajadores`) para paralelizar búsquedas, evitando la creación de procesos zombi.
│   ├── Makefile
│   └── generador.c
│
├── Práctica 2.2/      # Criptoanálisis Multinivel, Señales (SIGTERM) y Memoria
│   │                  # Explicación:
│   │                  # Reventador de contraseñas por fuerza bruta multinivel utilizando la librería `crypt`.
│   │                  # Comunicación e interrupción interprocesos mediante señales Unix (`kill`, `SIGTERM`) 
│   │                  # para abortar trabajadores activos al hallar la clave, asegurando la liberación de memoria.
│   ├── Makefile
│   └── reventador.c
│
├── Práctica 2.3/      # Minishell: Órdenes Internas, Externas y Redirección de E/S
│   │                  # Explicación:
│   │                  # Construcción de un intérprete de comandos (*shell*) interactivo en C.
│   │                  # - Comandos internos: `cd` (`chdir`), `pwd` (`getcwd`), `exit`.
│   │                  # - Comandos externos: Creación de hijo (`fork`) y reemplazo de imagen (`execvp`).
│   │                  # - Redirecciones E/S: Modificación de la tabla de descriptores (`open`, `dup2`, `close`).
│   ├── Makefile
│   ├── minishell.c
│   └── parser.c
│
└── README.md          # Documentación general y arquitectura del repositorio
