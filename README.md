# ordenacion-paralela-mpi-openmp
Proyecto final para la asignatura de Arquitectura de Computación de Altas Prestaciones.

Este proyecto fue Tiene como objetivo evaluar el rendimiento de diferentes enfoques de programación paralela aplicados al problema clásico de ordenación de vectores usando el algoritmo Mergesort.

##  Objetivo

Implementar y comparar distintas versiones del algoritmo de ordenación:
- Versión secuencial (base)
- Versión paralela usando OpenMP (modelo de memoria compartida).
- Versión paralela usando MPI (modelo de paso de mensajes).

Se analizan los resultados en distintos niveles de carga y núcleos, evaluando **tiempo de ejecución, speedup y eficiencia.

## Estructura del repositorio

- `mergesort_secuencial.cpp` → Código fuente de la versión secuencial.
- `mergesort_openmp.cpp` → Código fuente de la versión paralela con OpenMP.
- `mergesort_mpi.cpp` → Código fuente de la versión paralela con MPI.
- `mergesort_secuencial` / `mergesort_openmp` / `mergesort_mpi` → Archivos compilados (ejecutables).
- `Gráficas_Proyecto_Final_Programación_Paralela.ipynb` → Notebook con gráficas de speedup comparativo entre OpenMP y MPI (realizado con Python).
- `Documento Final Proyecto - Programación Paralela.pdf` → Informe final con análisis, tablas y resultados.


## Requisitos

- Compilador C++ (g++)
- Soporte para OpenMP (`-fopenmp`)
- Biblioteca MPI instalada (`mpic++`, `mpiexec`)
- Python (opcional, para graficar)

Para compilar cada versión del programa, sigue los pasos a continuación desde la terminal:

Para la versión secuencial, se debe ejecutar:
g++ -o mergesort_secuencial mergesort_secuencial.cpp

Para la versión con OpenMP, se debe ejecutar:
g++ -fopenmp -o mergesort_openmp mergesort_openmp.cpp

Para la versión con MPI, se debe ejecutar:
mpic++ -o mergesort_mpi mergesort_mpi.cpp
