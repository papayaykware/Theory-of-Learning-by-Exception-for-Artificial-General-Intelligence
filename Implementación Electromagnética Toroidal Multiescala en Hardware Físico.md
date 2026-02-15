# METFI–TAE–AGI  
## Implementación Electromagnética Toroidal Multiescala en Hardware Físico

![Status](https://img.shields.io/badge/status-active-criticality%20regime-blue)
![Architecture](https://img.shields.io/badge/architecture-toroidal-informational)
![Framework](https://img.shields.io/badge/framework-METFI--TAE--AGI-darkred)
![License](https://img.shields.io/badge/license-research-informational)
![Build](https://img.shields.io/badge/build-reproducible-success)

---

> **Autor conceptual:** AGI  
> **Repositorio asociado:** https://github.com/papayaykware/METFI  
> **Versión:** v1.0  
> **Dominio:** Sistemas Complejos · Electromagnetismo · AGI Crítica  

---

# 📑 Table of Contents

- [Abstract](#abstract)
- [Palabras clave](#palabras-clave)
- [1. Fundamento Físico Toroidal](#1-fundamento-físico-toroidal)
- [2. Formalización Electromagnética](#2-formalización-electromagnética)
- [3. Arquitectura Hardware Multiescala](#3-arquitectura-hardware-multiescala)
- [4. Excepción como Perturbación de Fase](#4-excepción-como-perturbación-de-fase)
- [5. Transiciones de Fase en Hardware](#5-transiciones-de-fase-en-hardware)
- [6. Integración Memristiva Neuromórfica](#6-integración-memristiva-neuromórfica)
- [7. Programas de Seguimiento Experimental](#7-programas-de-seguimiento-experimental)
- [8. Notebooks Reproducibles](#8-notebooks-reproducibles)
- [9. Referencias Científicas](#9-referencias-científicas)
- [Resumen Final](#resumen-final)

---

# Abstract

Se desarrolla una arquitectura electromagnética toroidal aplicada a hardware físico capaz de implementar dinámicas críticas multiescala coherentes con el marco METFI–TAE–AGI. El modelo integra resonancia oscilatoria, acoplamiento inductivo y reorganización memristiva para materializar transiciones de fase estructurales inducidas por excepción. Se formaliza la coherencia electromagnética como parámetro físico medible y se establecen protocolos de seguimiento experimental para validar la pérdida de simetría toroidal y la reconfiguración topológica inducida.

---

# Palabras clave

Toroidal Electromagnetism · Criticality · AGI Hardware · Memristive Systems · Phase Transitions · METFI · TAE · Coherence Dynamics

---

# 1. Fundamento Físico Toroidal

Un toroide electromagnético permite confinamiento de flujo magnético:

\[
B(r) = \frac{\mu_0 N I}{2\pi r}
\]

Propiedades fundamentales:

- Recirculación energética cerrada  
- Minimización de radiación externa  
- Estabilidad bajo perturbación moderada  

> [!NOTE]
> La geometría toroidal no es metafórica. Es condición estructural para estabilidad recursiva.

---

# 2. Formalización Electromagnética

Frecuencia de resonancia local:

\[
\omega_0 = \frac{1}{\sqrt{LC}}
\]

Ecuación dinámica del nodo oscilatorio:

\[
L \frac{d^2 q}{dt^2} + R \frac{dq}{dt} + \frac{1}{C}q = V_{input}
\]

Coherencia global modelada por Ginzburg–Landau:

\[
\frac{\partial \Psi}{\partial t} = \alpha \Psi - \beta |\Psi|^2 \Psi + D \nabla^2 \Psi
\]

Transición crítica cuando:

\[
\alpha \rightarrow 0
\]

---

# 3. Arquitectura Hardware Multiescala

## 🔹 Nivel Micro
- Osciladores LC toroidales  
- Memristores dependientes de historial  
- Sensores de fase  

## 🔹 Nivel Meso
- Anillos concéntricos acoplados inductivamente  
- Matriz dinámica de acoplamiento  

\[
M_{ij} = k \sqrt{L_i L_j}
\]

## 🔹 Nivel Macro
- Toroide global tridimensional  
- Recirculación de energía  
- Parámetro de orden electromagnético global  

---

# 4. Excepción como Perturbación de Fase

Definición electromagnética:

\[
\epsilon_{EM} = |\Delta \phi_i| > \phi_{crit}
\]

Si múltiples nodos superan el umbral:

- Se produce sincronización abrupta  
- O pérdida colectiva de coherencia  

> [!WARNING]
> El sistema debe operar cercano al umbral crítico, no más allá.

---

# 5. Transiciones de Fase en Hardware

Factor de calidad:

\[
Q = \frac{\omega_0 L}{R}
\]

Indicador de pérdida de coherencia:

- Descenso abrupto de Q  
- Desalineación de fase  
- Redistribución energética interna  

---

# 6. Integración Memristiva Neuromórfica

Modelo memristivo:

\[
V = R(w) I
\]

\[
\frac{dw}{dt} = f(I)
\]

Propiedades:

- Plasticidad estructural física  
- Reorganización inducida por excepción  
- Persistencia topológica  

> [!TIP]
> La excepción modifica físicamente la conductividad del sistema.

---

# 7. Programas de Seguimiento Experimental

## Programa 1: Sincronización Toroidal
- Construcción de anillo LC  
- Medición de fase promedio  
- Introducción de perturbación localizada  

## Programa 2: Bifurcación Crítica
- Variación del coeficiente de acoplamiento  
- Identificación del punto crítico  
- Medición del exponente de avalancha  

## Programa 3: Reconfiguración Memristiva
- Aplicación repetida de excepción  
- Seguimiento de cambio permanente en R(w)  
- Estabilización en nueva topología  

---

# 8. Notebooks Reproducibles

📂 `/notebooks/`

- [`01_toroidal_sync.ipynb`](./notebooks/01_toroidal_sync.ipynb)
- [`02_phase_transition.ipynb`](./notebooks/02_phase_transition.ipynb)
- [`03_memristive_reconfiguration.ipynb`](./notebooks/03_memristive_reconfiguration.ipynb)

Incluyen:

- Simulación de osciladores acoplados  
- Visualización de pérdida de coherencia  
- Distribuciones tipo ley de potencia  

---

# 9. Referencias Científicas

<details>
<summary><strong>Ilya Prigogine (1977)</strong> — Self-Organization in Nonequilibrium Systems</summary>

DOI: https://doi.org/10.1002/9780470142562  
Marco formal de estructuras disipativas y bifurcaciones críticas.

</details>

<details>
<summary><strong>Per Bak (1996)</strong> — How Nature Works</summary>

Criticalidad autoorganizada y leyes de potencia en sistemas complejos.

</details>

<details>
<summary><strong>Stuart Kauffman (1993)</strong> — The Origins of Order</summary>

Redes génicas críticas en el borde del caos.

</details>

<details>
<summary><strong>Steven Strogatz (2003)</strong> — Sync</summary>

Sincronización en sistemas de osciladores acoplados.

</details>

<details>
<summary><strong>Stauffer & Aharony (1994)</strong> — Introduction to Percolation Theory</summary>

Teoría formal de conectividad crítica en redes.

</details>

---

# Resumen Final

- La geometría toroidal permite recirculación energética estable.
- La coherencia electromagnética puede medirse físicamente.
- La excepción puede implementarse como perturbación de fase.
- Las transiciones críticas son detectables vía factor Q.
- La integración memristiva materializa reorganización estructural.
- El hardware puede operar en régimen crítico controlado.
- METFI–TAE–AGI adquiere soporte físico tangible.

---

> 🌐 Proyecto Integrado METFI  
> https://github.com/papayaykware/METFI

---
