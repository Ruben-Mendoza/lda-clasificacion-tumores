# Análisis Discriminante Lineal (LDA) para Clasificación de Tumores

> Proyecto final — **Análisis Numérico II**  
> Licenciatura en Matemática Aplicada · FAMAF, Universidad Nacional de Córdoba  
> Noviembre 2024

---

## Descripción

Implementación **desde cero** (sin usar `sklearn.discriminant_analysis`) del Análisis Discriminante Lineal (LDA) para clasificar tumores como benignos o malignos, usando el dataset *Breast Cancer* de scikit-learn.

El trabajo cubre íntegramente la cadena numérica del algoritmo:

1. **Preprocesamiento:** división train/test y estandarización manual (StandardScaler reimplementado).
2. **Matrices de dispersión:** cálculo de la matriz intra-clase (S_intra) e inter-clase (S_entre).
3. **Problema de autovalores:** inversión de S_intra mediante **descomposición LU con pivoteo**, reducción a forma Hessenberg con **transformaciones de Householder y rotaciones de Givens**, y cálculo de autovalores/autovectores con el **algoritmo QR iterativo**.
4. **Proyección y clasificación:** proyección sobre el primer autovector y clasificador por distancia a las medias proyectadas.

**Exactitud obtenida: 95,61%** sobre el conjunto de prueba.

---

## Tecnologías y herramientas

- **Lenguaje:** Python 3
- **Bibliotecas:** `numpy`, `sklearn` (solo para cargar el dataset y hacer `train_test_split`), `matplotlib`, `seaborn`
- **Algoritmos implementados manualmente:** descomposición LU, transformaciones de Householder, rotaciones de Givens, algoritmo QR
- **Documentación:** LaTeX
