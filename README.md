# CALCULADORAEDAD

Programa de revisión integral que calcula la edad exacta de una persona a partir de su fecha de nacimiento, implementado en **Python** y en **C++** para comparar ambos lenguajes.

## Descripción

El programa pide el día, mes y año de nacimiento, verifica que la fecha exista en el calendario real y calcula la edad restando el año de nacimiento al año actual. Si la persona todavía no cumplió años en la fecha de referencia (8/7/2026), se le resta 1 a la edad.

El filtro de consistencia controla que:

- El año esté entre 1900 y 2026.
- El mes esté entre 1 y 12.
- El día exista en ese mes (meses de 30 días, febrero con 28 o 29 días según sea bisiesto).

Un año es bisiesto si cumple `(anio % 4 == 0 && anio % 100 != 0) || (anio % 400 == 0)`.

## Conceptos aplicados

- Lógica y algoritmos (condicionales anidados)
- Funciones con retorno booleano (`esBisiesto`, `esFechaValida`)
- Filtro de consistencia de datos
- Comparación entre Python (alto nivel) y C++ (bajo nivel)
- Manejo de errores de entrada en Python (`try / except`)

## Estructura del proyecto

```
calculadoraedad/
├── .gitignore
├── LICENSE
├── README.md
├── docs/
│   └── InformeProyectoCalculadoraEdad.pdf
├── proyecto_cpp/
│   └── main.cpp
└── proyecto_python/
    └── main.py
```

## Requisitos

- **C++:** compilador g++ (MinGW / MSYS2) o, en su defecto, OnlineGDB
- **Python:** Python 3 instalado
- Visual Studio Code (opcional)

## Compilación y ejecución (PowerShell, Windows 10/11)

Desde la raíz del proyecto:

**C++**
```
g++ proyecto_cpp/main.cpp -o proyecto_cpp/calculadoraedad.exe
.\proyecto_cpp\calculadoraedad.exe
```

**Python**
```
python proyecto_python/main.py
```

## Ejemplo de uso

```
Ingrese Dia, Mes y Anio de nacimiento (separados por espacios): 15 3 2008

[SISTEMA] Fecha de hoy: 8/7/2026
[SISTEMA] Edad calculada: 18 anos.
```

Si la fecha no existe (por ejemplo, 30/2/2008), el programa muestra un mensaje de error.

## Autor

Benjamin Hlynczuk
E.E.S.T. N.º 1 "Eduardo Ader", Vicente López
Laboratorio de Programación (LPR), 5.º año, 2026
