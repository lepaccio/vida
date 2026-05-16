# Clase #2 — Límites (recíproca), Propiedades algebraicas, Continuidad y Derivada

Secuencia conceptual reconstruida a partir de las 6 páginas del cuaderno.

## Bloque A — Cierre del teorema de límite por coordenadas

1. **01_Teorema_limite_por_coordenadas_demo_reciproca** — Retoma el teorema (lim f(t)=L ⟺ lim fᵢ(t)=lᵢ). Demostración (⟸): dado ε>0, tomar ε/√n, existen δᵢ>0 con |fᵢ(t)−lᵢ|² < ε²/n para cada i.
2. **02_Cierre_demostracion_y_Prop_algebraicas** — Suma: ‖f(t)−L‖ = √Σ(fᵢ(t)−lᵢ)² ≤ √(n·ε²/n) = ε, tomando δ = mín{δ₁,…,δₙ}. Enuncia **Prop. algebraicas**: lim(f±g)=L±M, lim(f·g)=L·M, lim(f×g)=L×M.

## Bloque B — Demostraciones de propiedades algebraicas

3. **03_Demo_prop_algebraicas_suma_y_producto_interno** — Prueba de lim(f±g)=L±M usando límite por coordenadas. Inicia prueba de lim(f·g)=L·M vía suma Σ fᵢ(t)·gᵢ(t).

## Bloque C — Multiplicación escalar–vectorial y Continuidad

4. **04_Teorema_limite_escalar_por_vectorial_y_def_Continuidad** — Teorema: si f:X→Rⁿ, φ:R→R con lim f=L y lim φ=M, entonces lim(φ·f)=M·L. **Def Continuidad**: f continua en a si ∀ε>0 ∃δ>0 tq |t−a|<δ ⇒ ‖f(t)−f(a)‖<ε.
5. **05_Continuidad_por_coordenadas_y_obs_puntos_aislados** — Prop: f continua en a ⟺ cada fᵢ continua en a. Si a es pto de acumulación: lim f(t)=f(a) ⟺ lim fᵢ(t)=fᵢ(a). Obs: en puntos aislados toda f es continua.

## Bloque D — Derivada / Diferenciabilidad

6. **06_Diferenciabilidad_velocidad_rapidez_y_recta_tangente** — Def: f: I⊂R→Rⁿ diferenciable en t si existe V = lim_{h→0} (f(t+h)−f(t))/h ∈ Rⁿ. Notación V=f'(t). Interpretación física: velocidad. **Rapidez** r(t)=‖f'(t)‖. **Recta tangente** P(t)=f(t)+r·f'(t). Obs sobre transformación lineal L:R→Rⁿ y su matriz asociada.
