# FORMULARIO — CM2A1 (PD1 + PD2)

> Terminología y fórmulas tal cual están en tu cuaderno (Clases #1, #2, #3) + Sesión 04–06.

---

## 1. Funciones vectoriales — conceptos básicos

- **Def**: $f\colon X\subset \mathbb{R}\to \mathbb{R}^{n}$, $f(t)=(f_1(t),\dots,f_n(t))$, $f_i$ **funciones coordenadas**.
- **Traza**: $\operatorname{tra}(f)=\operatorname{Im}(f)=\{f(x):x\in X\}$.
- **Dominio**: $\operatorname{Dom} f = \bigcap_{i=1}^{n}\operatorname{Dom} f_i$.
- **Gráfica**: $\operatorname{graf}(f)=\{(t,f(t)):t\in X\}\subset \mathbb{R}\times \mathbb{R}^{n}\cong \mathbb{R}^{n+1}$.
- **Operaciones**: $(f\pm g)$ con $\operatorname{Dom}(f\pm g)=\operatorname{Dom} f\cap \operatorname{Dom} g$. **Producto interno euclídeo**: $\langle f,g\rangle = \sum_i f_i g_i$.

---

## 2. Topología en $\mathbb{R}$ (preparación para límites)

- **Bola abierta**: $B(a,\varepsilon)=\{x\in \mathbb{R}:|x-a|<\varepsilon\}$.
- **Punto de acumulación** de $X\subset \mathbb{R}$: $a$ tal que $\forall \varepsilon>0,\ (B(a,\varepsilon)-\{a\})\cap X\neq \emptyset$.
- **Punto aislado** de $X$: $\exists\,\varepsilon>0$ tal que $(B(a,\varepsilon)-\{a\})\cap X = \emptyset$.
- **Notación**: $X' = $ conjunto de puntos de acumulación de $X$.

---

## 3. Límites

- **Definición** $\varepsilon$–$\delta$:
$$
\lim_{t\to a} f(t)=L \;\Longleftrightarrow\; \forall \varepsilon>0\ \exists\,\delta>0\ :\ 0<|t-a|<\delta\ \land\ t\in\operatorname{Dom} f \Rightarrow \|f(t)-L\|<\varepsilon.
$$

- **Teorema (límite por coordenadas)**:
$$
\lim_{t\to a} f(t)=L \;\Longleftrightarrow\; \forall i:\ \lim_{t\to a} f_i(t)=L_i.
$$

- **Álgebra**: si $\lim f = L$ y $\lim g = M$:
  - $\lim(f\pm g)=L\pm M$
  - $\lim\langle f,g\rangle = \langle L,M\rangle$
  - $\lim(f\times g) = L\times M$ (en $\mathbb{R}^3$)
  - $\lim(\varphi\cdot f) = (\lim\varphi)\cdot(\lim f)$ cuando $\varphi$ es escalar.

---

## 4. Continuidad

- **Definición**: $f$ continua en $a \Longleftrightarrow \forall \varepsilon>0\ \exists\,\delta>0:\ |t-a|<\delta \Rightarrow \|f(t)-f(a)\|<\varepsilon$.
- **Por coordenadas**: $f$ continua en $a \Longleftrightarrow$ cada $f_i$ continua en $a$.
- Si $a$ es punto de acumulación: $f$ continua en $a \Longleftrightarrow \lim_{t\to a} f(t)=f(a)$.
- **Observación**: en puntos aislados toda $f$ es continua (trivialmente).
- **Desigualdad triangular inversa**: $\bigl|\,\|f(t)\| - \|f(a)\|\,\bigr| \leq \|f(t)-f(a)\|$.

---

## 5. Diferenciabilidad

### Definición como límite (Clase #2)

$$
V = f'(t) = \lim_{h\to 0} \frac{f(t+h) - f(t)}{h} \in \mathbb{R}^n.
$$

### Definición como aproximación lineal (Clase #3)

$f$ es **diferenciable** en $t$ si existe $L\colon \mathbb{R}\to \mathbb{R}^n$ transformación lineal tal que

$$
f(t+h)=f(t)+L\cdot h + \mu(h), \quad \lim_{h\to 0}\frac{\mu(h)}{h}=0.
$$

**Equivalencia**: $L = Df(t) = f'(t)$.

### Interpretación física

- $f(t)$ posición $\Rightarrow f'(t)$ **velocidad**.
- **Rapidez**: $r(t)=\|f'(t)\|$.
- **Recta tangente** en $f(t_0)$: $P(s)=f(t_0)+s\,f'(t_0),\ s\in\mathbb{R}$.

### Teorema

**Diferenciable en $t \Rightarrow$ continua en $t$** (el recíproco es **falso**).

### Álgebra de derivadas

- $(f\pm g)' = f' \pm g'$
- $(\alpha\cdot f)' = \alpha'\cdot f + \alpha\cdot f'$ ($\alpha$ escalar)
- $\langle f, g\rangle' = \langle f', g\rangle + \langle f, g'\rangle$
- $(f\times g)' = f'\times g + f\times g'$ (en $\mathbb{R}^3$)
- $(\|f\|)' = \dfrac{\langle f, f'\rangle}{\|f\|}\quad$ (cuando $f\neq 0$)

### Regla de la cadena

Si $\varphi\colon J\to I$ (real) y $f\colon I\to \mathbb{R}^n$ son diferenciables:

$$
(f\circ\varphi)'(a) = f'(\varphi(a))\cdot \varphi'(a) = Df(\varphi(a))\cdot \varphi'(a).
$$

---

## 6. Teorema del Valor Medio

- **TVM clásico NO se generaliza a $\mathbb{R}^n$**: $\dfrac{f(b)-f(a)}{b-a}\neq f'(c)$ en general.
- **TVM por coordenadas**: $\exists\,c_1,\dots,c_n\in(a,b)$ tales que $f(b)-f(a)=(b-a)\,(f_1'(c_1),\dots,f_n'(c_n))$.
- **TVM generalizado (versión $\mathbb{R}^n$)**: si $f$ continua en $[a,b]$ y diferenciable en $(a,b)$, entonces $\exists\,c\in(a,b)$ con
$$
\boxed{\langle f(b)-f(a),\, f'(c)\rangle = 0.}
$$

**Corolario importante**: si $\|f(t)\|$ es constante $\Rightarrow \langle f(t), f'(t)\rangle = 0$.

---

## 7. Integración (Clase #3 al final + Sesión 04)

### Partición y puntillación

- **Partición** de $[a,b]$: $P=\{t_0,t_1,\dots,t_n\}$ con $t_0=a<t_1<\cdots<t_n=b$.
- **Norma**: $|P|=\max_i |t_i - t_{i-1}|$.
- **Puntillación**: $\Xi=\{P_1,\dots,P_n\}$ con $P_i\in[t_{i-1},t_i]$.

### Integral

$$
\int_a^b f(t)\,dt = \left(\int_a^b f_1(t)\,dt,\,\dots,\,\int_a^b f_n(t)\,dt\right).
$$

### Propiedades

- Linealidad: $\int(\alpha f + \beta g) = \alpha\!\int f + \beta\!\int g$.
- $\langle \int f, v\rangle = \int \langle f, v\rangle\ $ (si $v$ vector fijo).
- $\left\|\int_a^b f\,dt\right\| \leq \int_a^b \|f\|\,dt$.
- **Teorema fundamental**: $F(t)=\int_a^t f(u)\,du \Rightarrow F'(t)=f(t)$.

---

## 8. Longitud de arco

- **Longitud**: $L=\int_a^b \|f'(t)\|\,dt$.
- **Función longitud**: $s(t)=\int_{t_0}^{t}\|f'(u)\|\,du \Rightarrow s'(t)=\|f'(t)\|\geq 0$.
- **Curva rectificable**: $L$ finita.
- **Curva regular**: $f'(t)\neq 0\ \forall t$.

### Parametrización por longitud de arco (reparametrización)

1. Calcular $s(t)=\int \|f'(u)\|\,du$.
2. Invertir $t=t(s)$.
3. $\alpha(s)=f(t(s))$. Propiedad: $\|\alpha'(s)\|=1$.

**Consecuencia clave**: si $\alpha$ está parametrizada por arco, entonces $\alpha'(s)\perp\alpha''(s)$ (porque $\|\alpha'\|^2=1$ constante).

---

## 9. Triedro de Frenet

Curva **regular** y con $f'\times f''\neq 0$ ("birregular").

| Elemento | Fórmula general | En param. por arco |
|---|---|---|
| **Tangente** $T(t)$ | $\dfrac{f'(t)}{\|f'(t)\|}$ | $\alpha'(s)$ |
| **Normal** $N(t)$ | $\dfrac{T'(t)}{\|T'(t)\|}$ | $\dfrac{\alpha''(s)}{\|\alpha''(s)\|}$ |
| **Binormal** $B(t)$ | $T(t)\times N(t) = \dfrac{f'\times f''}{\|f'\times f''\|}$ | $T(s)\times N(s)$ |

### Curvatura

$$
\kappa(t) = \frac{\|f'(t)\times f''(t)\|}{\|f'(t)\|^3}.
$$

En parametrización por arco: $\kappa(s) = \|\alpha''(s)\|$.

### Torsión

$$
\tau(t) = \frac{\langle f'(t)\times f''(t),\ f'''(t)\rangle}{\|f'(t)\times f''(t)\|^2}.
$$

### Fórmulas de Frenet (param. por arco)

$$
T' = \kappa\, N,\qquad N' = -\kappa\, T + \tau\, B,\qquad B' = -\tau\, N.
$$

### Descomposición de $f''$

$$
\boxed{f''(t) = v'(t)\,T(t) + v(t)^2\,\kappa(t)\,N(t)}, \qquad v(t)=\|f'(t)\|.
$$

- Componente tangencial: $v'(t)$.
- Componente normal (centrípeta): $v^2\kappa$.

---

## 10. Planos asociados a la curva

En cada punto $f(t_0)$:

| Plano | Generado por | Normal al plano |
|---|---|---|
| **Osculador** | $T$ y $N$ | $B$ (o $f'\times f''$) |
| **Normal** | $N$ y $B$ | $T$ (o $f'$) |
| **Rectificante** | $T$ y $B$ | $N$ |

---

## 11. Criterios útiles

- **Curva plana** $\Longleftrightarrow \tau\equiv 0 \Longleftrightarrow$ el plano osculador es constante.
  - Para demostrarlo: expresar $f(t)$ como combinación lineal de vectores fijos ($+$ punto base), o encontrar $\langle n, f(t)\rangle = d$ para todo $t$.
- **Recta** $\Longleftrightarrow \kappa\equiv 0$.
- En param. por arco, la **regularidad** es automática: $\alpha'(s)=T(s)\neq 0$.

---

## 12. Estrategia de examen

1. **Lee la consigna entera antes de empezar**.
2. **Cita los teoremas** que usas. "Por el teorema de límites por coordenadas…", "Por $\kappa=\|f'\times f''\|/\|f'\|^3$…".
3. **Deriva por coordenadas** cuando la fórmula general sea complicada.
4. **Usa productos notables** en $\|f'\|^2$: suma de cuadrados de $\sin/\cos$ siempre simplifica.
5. **Si algo no sale en forma cerrada** (p.ej. integral elíptica), deja la parametrización expresada implícitamente y señala que es la integral de longitud de arco.
6. **Dibuja dominios, curvas, superficies** siempre que involucre geometría — la profe espera esto.
7. **Argumentos para reclamo**: fundamenta con definición/teorema $+$ cita bibliográfica (Lima vol 2, Marsden–Tromba).

---

## 13. Errores clásicos a evitar

- **NO** escribas $\dfrac{f(b)-f(a)}{b-a}=f'(c)$ para $f\colon \mathbb{R}\to \mathbb{R}^n$. ¡NO es válido!
- Cuidado con **dominios**: $\sqrt{t}$ requiere $t\geq 0$; $\ln(x)$ requiere $x>0$; $1/x$ requiere $x\neq 0$.
- La derivada por coordenadas **requiere diferenciabilidad** (no sólo continuidad).
- $N$ no es paralelo a $f''$, salvo en **parametrización por arco**. En general $N = B\times T$.
- La **traza** de una parametrización es sólo el "camino", no incluye velocidad. Dos parametrizaciones distintas pueden tener la misma traza.
- $\|f\|$ continua $\not\Rightarrow f$ continua (contraejemplo: $f=(\operatorname{sgn}(t),0)$).
