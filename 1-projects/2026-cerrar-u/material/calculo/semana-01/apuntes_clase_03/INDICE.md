# Clase #3 — Diferenciabilidad (enfoque trans. lineal), TVM y apertura de Integración

Secuencia reconstruida a partir de **7 páginas del cuaderno** + **4 fotos del pizarrón**.
Cubre cierre de la **Sesión 03** y apertura de la **Sesión 04** del sílabo.

## Bloque A — Diferenciabilidad como aproximación por transformación lineal

1. **01_Diferenciabilidad_como_trans_lineal_DEF** — Recordatorio: f: I→Rⁿ derivable en t si existe V=lim_{h→0}(f(t+h)−f(t))/h=f'(t). Introduce L: R→Rⁿ trans. lineal con L·h=(l₁h,…,lₙh). **DEF**: f es diferenciable en t si existe L trans. lineal tal que f(t+h)=f(t)+L·h+μ(h) con lim_{h→0} μ(h)/h = 0.
2. **02_Obs_L_aproxima_notacion_Df_y_ejemplo** — Obs: L aproxima f cerca de t, f(t+h)−f(t) ≈ L·h. Notación: L=Df(t)=f'(t)=df/dt. **Ejemplo**: f(t)=(t³cos t, t³sen t, t³), en t=π la derivada es f'(π)=(−3π², −π³, 3π²).
3. **03_Equivalencia_diferenciable_iff_vector_tangente** — **PROP**: f es diferenciable en t ⟺ existe el vector tangente f'(t), y Df(t) es representado por f'(t). Demostración por coordenadas usando lim μᵢ(h)/h = 0.

## Bloque B — Teoremas y álgebra de derivadas

4. **04_Dif_implica_continua_y_algebra_de_derivadas** — **Teorema**: f diferenciable en t ⇒ f continua en t (vía coordenadas). **Álgebra**: si f,g: I→Rⁿ, φ: I→R diferenciables en a, entonces f±g, λf+g, φ·f, f·g son diferenciables en a, con (λf+g)'=λf'+g', (φf)'=φ'f+φf', **(f·g)'=f'·g+f·g'** ← importante.

## Bloque C — Teorema del Valor Medio

5. **05_TVM_por_coordenadas_y_ejemplo_norma_constante** — **TVM por coordenadas**: f continua en [a,b] y diferenciable en (a,b) ⇒ ∃c₁,…,cₙ∈(a,b) tq f(b)−f(a) = (b−a)·(f'₁(c₁),…,f'ₙ(cₙ)). Se demuestra aplicando el TVM real a cada fᵢ. **Obs**: (f(b)−f(a))/(b−a) ≠ f'(c) **NO** vale en Rⁿ en general. **Ejemplo**: si ‖f‖ es cte ⇒ ⟨f(t), f'(t)⟩ = 0 (se obtiene derivando ‖f‖² = ⟨f,f⟩).

## Bloque D — Regla de la cadena

6. **06_Regla_de_la_cadena_demostracion** — **PROP**: sea φ: J→I diferenciable en a (J,I⊂R abiertos) y f: I→Rⁿ diferenciable en φ(a). Entonces **(f∘φ)'(a) = f'(φ(a))·φ'(a) = Df(φ(a))·φ'(a)**. Demostración por coordenadas aplicando regla de la cadena en R.

## Bloque E — TVM generalizado (versión correcta en Rⁿ)

El TVM clásico (f(b)−f(a) = (b−a)·f'(c)) no vale en Rⁿ. La versión correcta:

> **Teorema**: f: R→Rⁿ continua en [a,b] y diferenciable en (a,b) ⇒ ∃c∈(a,b) con ⟨f(b)−f(a), f'(c)⟩ = 0.

7. **07_TVM_generalizado_enunciado_en_cuaderno** — Enunciado en el cuaderno.
8. **08_TVM_generalizado_pizarron_setup_de_g** — Pizarrón: se define g(x)=⟨f(b)−f(a), f(x)⟩.
9. **09_TVM_generalizado_pizarron_demo_Rolle** — Se evalúa g(a), g(b), se restan, g(b)=g(a), por Rolle ∃c con g'(c)=0.
10. **10_TVM_cierre_pizarron_e_inicio_Integracion_particion** — g'(x)=⟨f(b)−f(a), f'(x)⟩ ⇒ ⟨f(b)−f(a), f'(c)⟩=0. QED. **Inicio Integración**: def. de partición P={t₀,…,tₙ} con t₀=a<t₁<…<tₙ=b.

## Bloque F — Integración: preparación

11. **11_Integracion_norma_de_particion_y_puntillacion** — **Norma** |P|=máx{|tᵢ−tᵢ₋₁|}. **Puntillación** de P: colección Ξ={P₁,…,Pₙ} con Pᵢ∈[tᵢ₋₁,tᵢ].
