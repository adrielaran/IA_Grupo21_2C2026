# Inteligencia Artificial - Grupo 21 - 2C 2026
Trabajo Práctico N° 2 — Inteligencia Artificial Ingeniería en Sistemas de Información — UTN FRBA — 2do Cuatrimestre 2026 Grupo N° 21
## 📋 Descripción del Proyecto
El mantenimiento predictivo es fundamental para evitar paradas imprevistas en la industria. Este proyecto aborda el diagnóstico automático de fallas a partir de señales de acelerometría del banco de ensayos de la **Case Western Reserve University (CWRU)**, clasificando las condiciones operativas en cuatro categorías:
1. **Estado Normal**
2. **Falla en Pista Interna (Inner Race)**
3. **Falla en Elemento Rodante (Ball)**
4. **Falla en Pista Externa (Outer Race)**

## 🧠 Modelos Implementados
Se evaluaron y compararon tres arquitecturas diferentes de Redes Neuronales Artificiales empleando técnicas de normalización y *Early Stopping*:
* **Modelo 1 (Base MLP):** Perceptrón Multicapa con dos capas ocultas densas (*Backpropagation*).
* **Modelo 2 (CNN 1D):** Red Neuronal Convolucional Unidimensional, optimizada para extraer patrones locales y transitorios directamente de la señal cruda (alcanzó un **100% de precisión**).
* **Modelo 3 (MLP Variante Profunda):** Arquitectura densa ampliada con tres capas ocultas y distintas tasas de *Dropout*.

---

## 📁 Estructura del Repositorio
```text
├── data/                  # Datos procesados en formato CSV (entrenamiento y prueba)
├── src/ or notebooks/     # Código fuente (Notebooks de Google Colab / Scripts de Python)
└── README.md              # Documentación del proyecto
