# Clase #1 — Funciones vectoriales de variable real

Secuencia conceptual reconstruida a partir de las 11 páginas del cuaderno.

## Bloque A — Definición y estructura básica

1. **01_Definicion_funcion_vectorial_y_ejemplo** — Def: f: X⊂R → Rⁿ. Traza tra(f)=Im(f). Funciones coordenadas fᵢ. Dom f = ⋂ Dom fᵢ. Ejemplo: f(t)=(√t, 1/(t−1)).
2. **02_Dominio_definicion_grafica_resumen** — Cálculo: Dom f₁=[0,+∞), Dom f₂=R−{1} ⇒ Dom f=[0,+∞)−{1}. Def gráfica graf(f)⊂R×Rⁿ≅Rⁿ⁺¹. RESUMEN (Dom, tra, graf).
3. **03_Ejemplo_movil_no_escapa_del_cono** — Aplicación: probar que f(t)=(cos t/t, sen t/t, 1−1/t) nunca escapa del cono x²+y²=(z−1)².

## Bloque B — Operaciones

4. **04_Operaciones_suma_y_producto_interno** — f+g (dominios deben coincidir, Dom(f+g)=Dom f ∩ Dom g) y producto interno euclidiano ⟨f,g⟩=Σ fᵢgᵢ.
5. **05_Ejemplo_operaciones_f_mas_g** — Ejemplo: f=(2cos t,0,0), g=(0,2sen t,3) ⇒ (f+g)(t)=(2cos t, 2sen t, 3).

## Bloque C — Topología en Rⁿ (preparación para límites)

6. **06_Grafica_y_def_Puntos_de_acumulacion** — Esbozo gráfico del ejemplo (circunferencia en plano z=3). Def punto de acumulación. Bola abierta B(a,ε)={x∈R : |x−a|<ε}.
7. **07_Observaciones_bola_abierta_y_notacion_X_prima** — B(a,ε) en R (intervalo), R² (disco sin borde), R³ (esfera sin cáscara). Notación X′ = conjunto de puntos de acumulación de X.
8. **08_Ejemplo_X_prima_y_def_Punto_aislado** — Ejemplo: X=[3,4] ⇒ X′=[3,4]. Def punto aislado: (B(a,ε)−{a}) ∩ X = ∅.

## Bloque D — Límites de funciones vectoriales

9. **09_Limites_definicion** — Def lim_{x→a} f(x)=L con criterio ε–δ: ‖f(x)−L‖<ε. Observación: lim f(x)=L ⟺ lim ‖f(x)−L‖=0.
10. **10_Teorema_limite_por_coordenadas_demo_parte1** — Teorema: lim f(t)=L ⟺ ∀i lim fᵢ(t)=Lᵢ. Demostración (⟹): dado ε>0, existe δ₁>0 tal que ‖f(t)−L‖<ε ⇒ √Σ(fᵢ(t)−Lᵢ)² < ε.
11. **11_Teorema_limite_por_coordenadas_demo_parte2** — Continuación demostración: |fᵢ(t)−Lᵢ| ≤ ‖f(t)−L‖ < ε, basta tomar δ=δ₁.
