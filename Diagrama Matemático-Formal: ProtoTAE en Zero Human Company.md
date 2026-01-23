# 📊 Diagrama Matemático-Formal: ProtoTAE en Zero Human Company

```mermaid
flowchart TB
    %% Nodos de estado
    subgraph Estado
        X[Variables de Estado X = {x1, ..., xn}]
        F[Mapa de Evolución F: X → X]
        Phi[Función Objetivo Φ(X)]
    end

    %% Detección de excepciones
    subgraph Deteccion
        E[Excepción E(x) = 1 si x fuera de zona aceptable]
    end

    %% Reconfiguración y aprendizaje
    subgraph Adaptacion
        R[Operador de Reconfiguración R(X, E)]
        DeltaX[ΔX = η ∇_X L(X, Φ)]
    end

    %% Simulación y evaluación
    subgraph Simulacion
        Xsim[X_sim = F(R(X,E))]
        PhiSim[Φ_sim = Φ(X_sim)]
        Decision{Φ_sim ≥ Φ(X)?}
    end

    %% Ciclo TAE
    X --> F --> E
    E -->|E=1| R
    R --> DeltaX --> Xsim
    Xsim --> PhiSim --> Decision
    Decision -->|Sí| X
    Decision -->|No| R

    %% Red de procesos y propagación de excepciones
    subgraph Red
        X --> N1[Nodo 1]
        X --> N2[Nodo 2]
        N1 --> N2
        N2 --> N3[Nodo 3]
        N1 -.->|Propagación de excepción| N3
    end

    %% Índice de aprendizaje TAE
    style Estado fill:#f9f,stroke:#333,stroke-width:2px
    style Deteccion fill:#ff9,stroke:#333,stroke-width:2px
    style Adaptacion fill:#f96,stroke:#333,stroke-width:2px
    style Simulacion fill:#ccf,stroke:#333,stroke-width:2px
    style Red fill:#9cf,stroke:#333,stroke-width:2px
```

---

## 🔹 Notación Matemática del Diagrama

1. **Estado del sistema**:
   [
   X = {x_1, x_2, ..., x_n}, \quad x_i \in \mathbb{R} \text{ o vector de atributos}
   ]

2. **Evolución normal del sistema**:
   [
   X(t+1) = F(X(t))
   ]

3. **Detección de excepciones**:
   [
   E(x_i) =
   \begin{cases}
   1 & x_i \notin [x_i^{\min}, x_i^{\max}]\
   0 & x_i \in [x_i^{\min}, x_i^{\max}]
   \end{cases}
   ]

4. **Reconfiguración autónoma**:
   [
   X(t+1) \leftarrow R(X(t+1), E) = X(t+1) + \Delta X
   ]
   [
   \Delta X = \eta \cdot \nabla_X L(X, \Phi), \quad L(X, \Phi) = (\Phi_{\text{deseada}} - \Phi(X))^2
   ]

5. **Simulación y evaluación**:
   [
   X_{\text{sim}}(t+1) = F(R(X(t), E(t)))
   ]
   [
   \Phi_{\text{sim}} = \Phi(X_{\text{sim}}(t+1))
   ]
   [
   \text{Si } \Phi_{\text{sim}} \ge \Phi(X(t)) \Rightarrow X(t+1) = X_{\text{sim}}(t+1)
   ]
   [
   \text{Si } \Phi_{\text{sim}} < \Phi(X(t)) \Rightarrow \text{ajustar } R
   ]

6. **Red de procesos y propagación de excepciones**:
   [
   \forall x_j \in \text{vecinos}(x_i), \quad E(x_i)=1 \implies x_j(t+1) = R_{ij}(x_j(t))
   ]

7. **Índice de aprendizaje por excepción TAE**:
   [
   L_{\text{TAE}}(t) = \frac{\sum_{i=1}^n | \Delta x_i(t) | \cdot e_i(t)}{\sum_{i=1}^n e_i(t)}
   ]

---

## 🔹 Interpretación

* Cada **ciclo** del diagrama refleja la **lógica central de TAE**: detectar, adaptar y aprender.
* La **propagación en red** permite evaluar **efectos en cascada y resiliencia**.
* La simulación interna y la función objetivo Φ aseguran que la **adaptación solo se integra si mejora el desempeño global**.
* El **índice L_TAE** cuantifica la eficiencia de aprendizaje por excepción y permite comparar ciclos o sistemas.

---
