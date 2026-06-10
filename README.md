# Criterio de Routh-Hurwitz para HP Prime

Programa escrito en PPL (HP Prime Programming Language) para evaluar la estabilidad de sistemas dinámicos mediante el Criterio de Routh. Está diseñado específicamente para cumplir con los criterios académicos de la asignatura de Dinámica de Sistemas y Control.

---

## Características Principales

| Funcionalidad | Descripción |
| :--- | :--- |
| **Cas Singular A** | Si aparece un pivote nulo con elementos en la fila, detiene el cálculo y declara el sistema **Inestable**. |
| **Cas Singular B** | Ante una fila completa de ceros, deriva automáticamente el polinomio auxiliar par de la fila superior para continuar. |
| **Integradores** | Detecta y elimina automáticamente raíces nulas (`s=0`) al final del polinomio, ajustando el veredicto a *Marginalmente Estable* o *Inestable* según corresponda. |
| **Modo Paramétrico** | Si se introducen variables (ej. `K`), opera simbólicamente y extrae el sistema de inecuaciones de la primera columna que debe cumplirse para que el sistema sea estable. |

---

## Instalación

1. Conecta tu HP Prime al ordenador y abre el Connectivity Kit.
2. Crea un nuevo programa en la calculadora llamado `routh`.
3. Copia el contenido del archivo `routh.hppgrm` de este repositorio y pégalo en el editor del programa.
4. Guarda y compila.

---

## Guía de Uso

Ejecuta el programa desde la vista CAS introduciendo los coeficientes del polinomio característico en forma de lista, ordenados de mayor a menor grado.

### Ejemplos Prácticos

**1. Sistema Estable Estándar**
Polinomio: `s^4 + 10s^3 + 35s^2 + 50s + 24`
```text
routh([1, 10, 35, 50, 24])
