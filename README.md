# Inteligencia Artificial - Grupo 21 - 2C 2026

Trabajo Práctico N° 2 — Inteligencia Artificial | Ingeniería en Sistemas de Información — UTN FRBA — 2do Cuatrimestre 2026 | Grupo N° 21

---

## 📋 Descripción del Proyecto
El mantenimiento predictivo es fundamental para evitar paradas imprevistas en la industria. Este proyecto aborda el diagnóstico automático de fallas a partir de señales de acelerometría del banco de ensayos de la **Case Western Reserve University (CWRU)**, clasificando las condiciones operativas en cuatro categorías:
1. **Estado Normal**
2. **Falla en Pista Interna (Inner Race)**
3. **Falla en Elemento Rodante (Ball)**
4. **Falla en Pista Externa (Outer Race)**

---

## 🧠 Modelos Implementados
Se evaluaron y compararon tres arquitecturas diferentes de Redes Neuronales Artificiales empleando técnicas de normalización y *Early Stopping*:
- **Modelo 1 (Base MLP):** Perceptrón Multicapa con dos capas ocultas densas (*Backpropagation*).
- **Modelo 2 (CNN 1D):** Red Neuronal Convolucional Unidimensional, optimizada para extraer patrones locales y transitorios directamente de la señal cruda (alcanzó un **100% de precisión**).
- **Modelo 3 (MLP Variante Profunda):** Arquitectura densa ampliada con tres capas ocultas y distintas tasas de *Dropout*.

---

## 📁 Estructura del Repositorio
```text
├── data/                                  # Datos procesados en formato CSV (fragmentados por clase y prueba)
├── ProyectoN2_Grupo21_IA.ipynb             # Código fuente (Notebook de Google Colab con Scripts de Python)
└── README.md                              # Documentación del proyecto
```

---

## 📊 Fuentes de Datos Originales (Dataset CWRU)
Los registros experimentales crudos utilizados en este proyecto provienen del repositorio oficial del *Bearing Data Center* de la *Case Western Reserve University (CWRU)* en formato `.mat`. Se consideró un diámetro de falla constante de **0.007 pulgadas** abarcando los cuatro niveles de carga del motor (0 a 3 HP):

| Clase / Estado | 0 HP | 1 HP | 2 HP | 3 HP |
| :--- | :---: | :---: | :---: | :---: |
| **Normal** | [97.mat](https://engineering.case.edu/sites/default/files/97.mat) | [98.mat](https://engineering.case.edu/sites/default/files/98.mat) | [99.mat](https://engineering.case.edu/sites/default/files/99.mat) | [100.mat](https://engineering.case.edu/sites/default/files/100.mat) |
| **Pista Interna** | [105.mat](https://engineering.case.edu/sites/default/files/105.mat) | [106.mat](https://engineering.case.edu/sites/default/files/106.mat) | [107.mat](https://engineering.case.edu/sites/default/files/107.mat) | [108.mat](https://engineering.case.edu/sites/default/files/108.mat) |
| **Elemento Rodante** | [118.mat](https://engineering.case.edu/sites/default/files/118.mat) | [119.mat](https://engineering.case.edu/sites/default/files/119.mat) | [120.mat](https://engineering.case.edu/sites/default/files/120.mat) | [121.mat](https://engineering.case.edu/sites/default/files/121.mat) |
| **Pista Externa (@6:00)** | [130.mat](https://engineering.case.edu/sites/default/files/130.mat) | [131.mat](https://engineering.case.edu/sites/default/files/131.mat) | [132.mat](https://engineering.case.edu/sites/default/files/132.mat) | [133.mat](https://engineering.case.edu/sites/default/files/133.mat) |

---

## 📚 Enlaces y Referencias de Interés
- **Repositorio Oficial CWRU:** [Bearing Data Center - Case Western Reserve University](https://engineering.case.edu/bearing-data-center)
- **Documentación TensorFlow / Keras:** [https://www.tensorflow.org/](https://www.tensorflow.org/)
- **Documentación Scikit-Learn:** [https://scikit-learn.org/](https://scikit-learn.org/)
- **Bibliografía teórica de referencia:** 
  - Goodfellow, I., Bengio, Y., & Courville, A. (2016). *Deep Learning*. MIT Press.
  - Haykin, S. (2008). *Neural Networks and Learning Machines* (3rd ed.). Pearson.
