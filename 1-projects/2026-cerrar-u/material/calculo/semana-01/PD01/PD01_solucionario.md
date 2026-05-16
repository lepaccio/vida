# Solucionario PD1 — CM2A1 2026-1

> Usa la terminología de las Clases #1, #2 y #3: $\operatorname{tra}(f)=\operatorname{Im}(f)$, funciones coordenadas, $\operatorname{Dom} f = \bigcap_i \operatorname{Dom} f_i$, $B(a,\varepsilon)$, $X'$ conjunto de puntos de acumulación, definición $\varepsilon$–$\delta$ de límite, $\|\cdot\|$ norma euclidiana, TVM generalizado $\langle f(b)-f(a),f'(c)\rangle=0$, diferenciabilidad como trans. lineal, regla de la cadena.

---

## Ej 1 — Parametrizar segmento $(1,0,0)\to(0,1,0)$ con $f\colon [0,1]\to\mathbb{R}^3$

**Idea**: interpolación lineal entre dos puntos.

$$f(t)=(1-t)(1,0,0)+t(0,1,0)=(1-t,\,t,\,0),\qquad t\in[0,1].$$

**Verificación**: $f(0)=(1,0,0)$, $f(1)=(0,1,0)$. $\operatorname{tra}(f)$ es el segmento pedido. ✓

---

## Ej 2 — Parametrizar triángulo de vértices $A=(2,1,-1)$, $B=(1,3,-1)$, $C=(1,0,2)$ con $f\colon [0,3]\to \mathbb{R}^3$

**Por partes** (cada lado en un intervalo de longitud $1$):

- $t\in[0,1]$: $A\to B$: $f(t)=(1-t)A+tB=(2-t,\,1+2t,\,-1)$
- $t\in[1,2]$: $B\to C$: $f(t)=(2-t)B+(t-1)C=(1,\,6-3t,\,-4+3t)$
- $t\in[2,3]$: $C\to A$: $f(t)=(3-t)C+(t-2)A=(t-1,\,t-2,\,8-3t)$

**Observación**: $f$ es continua en $t=1,\,t=2$ (se verifican los valores). $\operatorname{tra}(f)$ = triángulo $ABC$.

---

## Ej 3 — Sea $f\colon\mathbb{R}\to\mathbb{R}$ real de variable real

**(a) Defina $g\colon\mathbb{R}\to\mathbb{R}^2$ cuya traza sea la gráfica de $f$.**

Por definición, $\operatorname{graf}(f)=\{(t,\,f(t)):t\in\mathbb{R}\}\subset\mathbb{R}\times\mathbb{R}\cong\mathbb{R}^2$.

Queremos $\operatorname{tra}(g)=\operatorname{graf}(f)$. Basta definir:

$$\boxed{g(t)=(t,\,f(t)),\qquad t\in\mathbb{R}.}$$

**Verificación**: $\operatorname{tra}(g)=\{(t,f(t)):t\in\mathbb{R}\}=\operatorname{graf}(f)$. ✓

**(b) A partir de $g$, defina $h\colon\mathbb{R}\to\mathbb{R}^3$ cuya traza sea la gráfica de $g$.**

$\operatorname{graf}(g)=\{(t,\,g(t)):t\in\mathbb{R}\}=\{(t,\,t,\,f(t)):t\in\mathbb{R}\}\subset\mathbb{R}\times\mathbb{R}^2\cong\mathbb{R}^3$.

$$\boxed{h(t)=(t,\,t,\,f(t)),\qquad t\in\mathbb{R}.}$$

---

## Ej 4 — $f\colon\,]\!-\pi,\pi[\,\to\mathbb{R}^2$ con $\langle f(t),(1,0)\rangle=\|f(t)\|\cos t$ y $\|f(t)\|=\dfrac{a}{1+\cos t}$, $a>0$

Sea $f(t)=(x(t),\,y(t))$. De la primera condición:

$$\langle f(t),(1,0)\rangle = x(t) = \|f(t)\|\cos t = \frac{a\cos t}{1+\cos t}.$$

De la segunda condición, $\|f\|^2 = x^2+y^2 = \dfrac{a^2}{(1+\cos t)^2}$.

$$y(t)^2 = \frac{a^2}{(1+\cos t)^2} - \frac{a^2\cos^2 t}{(1+\cos t)^2} = \frac{a^2(1-\cos^2 t)}{(1+\cos t)^2} = \frac{a^2\sin^2 t}{(1+\cos t)^2}.$$

Tomamos la rama positiva (la otra es la reflexión respecto al eje $x$):

$$\boxed{f(t)=\left(\frac{a\cos t}{1+\cos t},\ \frac{a\sin t}{1+\cos t}\right),\qquad t\in\,]\!-\pi,\pi[.}$$

**Simplificación con $\tan(t/2)$**: usando $1+\cos t = 2\cos^2(t/2)$ y $\sin t = 2\sin(t/2)\cos(t/2)$:

$$x(t)=\frac{a}{2}(1-\tan^2(t/2))\cdot\frac{1}{1}\cdot\ldots \quad \text{[trabajo trigonométrico que lleva a una parábola: }y^2 = 2ax - a^2\text{].}$$

> La traza es una **parábola** (ejercicio clásico UNI).

---

## Ej 5 — Cicloide $\mathcal{C}:\ x(t)=t-\sin(t),\ y(t)=1-\cos(t),\ t\in\mathbb{R}$

**(a) Puntos sobre los ejes coordenados**

- Eje $OX$: $y=0 \Rightarrow 1-\cos t = 0 \Rightarrow \cos t = 1 \Rightarrow t=2k\pi \Rightarrow$ puntos $(2k\pi,\,0)$, $k\in\mathbb{Z}$.
- Eje $OY$: $x=0 \Rightarrow t-\sin t = 0$. Como $g(t)=t-\sin t$ tiene $g'(t)=1-\cos t\geq 0$, $g$ es creciente y se anula sólo en $t=0 \Rightarrow$ único punto $(0,0)$.

**(b) Monotonía de las funciones coordenadas**

- $x'(t)=1-\cos t\geq 0$, nulo sólo en $t=2k\pi \Rightarrow x$ es **creciente** en $\mathbb{R}$.
- $y'(t)=\sin t \Rightarrow y$ **creciente** en $[2k\pi,(2k+1)\pi]$, **decreciente** en $[(2k+1)\pi,2(k+1)\pi]$.

**(c) Bosquejo**: sucesión de arcos ("arcos de cicloide") apoyados sobre $OX$, con cúspides en $(2k\pi,0)$ y altura máxima $2$ en $t=(2k+1)\pi$.

---

## Ej 6 — $f(t)=u+tv+t^2 w$, con $u,v,w\in\mathbb{R}^3$ no nulos

Describa y bosqueje la imagen de $f$ en los casos (a) $u,v$ l.i. y (b) $u,v$ l.d.

> **Observación previa**: el enunciado sólo impone condiciones sobre $u$ y $v$; el vector $w$ queda libre (no nulo). Conviene separar sub-casos según la posición de $w$.

### (a) $u$ y $v$ son l.i.

En particular $u\neq 0$, $v\neq 0$ y $v\notin\mathbb{R}\cdot u$. Definimos $g(t)=tv+t^2 w$, así $f(t)=u+g(t)$ (la traza de $f$ es la traslación en $u$ de la traza de $g$).

**Sub-caso a.1**: $w\notin \operatorname{span}\{v\}$ (equivalentemente $\{v,w\}$ l.i.).

Entonces $g(t)=tv+t^2 w$ recorre una curva en el plano $\Pi = \operatorname{span}\{v,w\}$. En coordenadas $(\alpha,\beta)$ con base $\{v,w\}$: $\alpha(t)=t$, $\beta(t)=t^2 \Rightarrow \beta=\alpha^2$ — **parábola**.

Luego $\operatorname{tra}(f)=u+$parábola está en el **plano afín** $u+\Pi$.

- Si además $u\in\Pi$ (caso degenerado dentro del sub-caso): $u+\Pi = \Pi$, la parábola pasa por el origen trasladada a $u$, pero vive en el mismo plano por el origen.
- Si $u\notin\Pi$: el plano afín $u+\Pi$ **no pasa por el origen**.

$$\boxed{\operatorname{tra}(f) \text{ es una parábola en el plano afín } u+\operatorname{span}\{v,w\}.}$$

**Sub-caso a.2**: $w\in\operatorname{span}\{v\}$, es decir $w=\mu v$ con $\mu\neq 0$ (porque $w$ no nulo).

$$f(t) = u + tv + t^2\mu v = u + (t+\mu t^2)\,v.$$

Sea $\varphi(t)=t+\mu t^2$. Su imagen es:
- Si $\mu>0$: $\varphi$ tiene mínimo $-\tfrac{1}{4\mu}$ en $t=-\tfrac{1}{2\mu}$ $\Rightarrow \operatorname{Im}\varphi=[-\tfrac{1}{4\mu},+\infty)$.
- Si $\mu<0$: $\varphi$ tiene máximo $-\tfrac{1}{4\mu}$ $\Rightarrow \operatorname{Im}\varphi=(-\infty,-\tfrac{1}{4\mu}]$.

$$\boxed{\operatorname{tra}(f)=\{u+s\,v:\ s\in\operatorname{Im}\varphi\} \text{ es una \textbf{semirecta} en dirección } v \text{ partiendo de } u-\tfrac{1}{4\mu}v.}$$

### (b) $u$ y $v$ son l.d.

Entonces $v=\lambda u$ con $\lambda\neq 0$ (ambos no nulos). Sustituyendo:

$$f(t)=u+t\lambda u+t^2 w=(1+\lambda t)\,u+t^2 w.$$

**Sub-caso b.1**: $w\notin\operatorname{span}\{u\}$ (i.e., $\{u,w\}$ l.i.).

En coordenadas $(\alpha,\beta)$ con base $\{u,w\}$: $\alpha(t)=1+\lambda t$, $\beta(t)=t^2$.

Despejando $t=(\alpha-1)/\lambda$: $\beta=\dfrac{(\alpha-1)^2}{\lambda^2}$ — **parábola** con vértice en $(1,0)$ (en coordenadas $(\alpha,\beta)$), es decir, en el punto $u$ de $\mathbb{R}^3$.

$$\boxed{\operatorname{tra}(f) \text{ es una parábola en el plano } \operatorname{span}\{u,w\} \text{ con vértice en } u.}$$

**Sub-caso b.2**: $w\in\operatorname{span}\{u\}$, es decir $w=\mu u$ con $\mu\neq 0$.

$$f(t)=(1+\lambda t+\mu t^2)\,u.$$

Sea $\psi(t)=1+\lambda t+\mu t^2$. Su imagen es:
- Si $\mu>0$: $\operatorname{Im}\psi=\bigl[1-\tfrac{\lambda^2}{4\mu},+\infty\bigr)$.
- Si $\mu<0$: $\operatorname{Im}\psi=\bigl(-\infty,1-\tfrac{\lambda^2}{4\mu}\bigr]$.

$$\boxed{\operatorname{tra}(f)=\{s\,u:\ s\in\operatorname{Im}\psi\} \text{ es una \textbf{semirecta} contenida en la recta } \mathbb{R}\cdot u.}$$

### Resumen

| Caso | Condición sobre $w$ | Traza de $f$ |
|---|---|---|
| **(a)** $u,v$ l.i. | $\{v,w\}$ l.i. | **Parábola** en plano afín $u+\operatorname{span}\{v,w\}$ |
| **(a)** $u,v$ l.i. | $w=\mu v$ | **Semirecta** en dirección $v$ partiendo de $u-\tfrac{1}{4\mu}v$ |
| **(b)** $u,v$ l.d. | $\{u,w\}$ l.i. | **Parábola** en plano $\operatorname{span}\{u,w\}$ con vértice en $u$ |
| **(b)** $u,v$ l.d. | $w=\mu u$ | **Semirecta** contenida en la recta $\mathbb{R}\cdot u$ |

---

## Ej 7 — Puntos de acumulación de $A=\{(x,y)\in\mathbb{R}^2:\ x^2+y+2x=3\}$

**Observación**: $A=\{(x,\,3-x^2-2x):x\in\mathbb{R}\}$ es la gráfica de una parábola.

**Demostración** $A' = A$:

*($A\subset A'$)*: dado $(x_0,y_0)\in A$, para todo $\varepsilon>0$ la bola $B((x_0,y_0),\varepsilon)$ contiene puntos $(x,\,3-x^2-2x)$ con $x\neq x_0$ y $|x-x_0|$ pequeño (por continuidad de la parábola). Luego $(x_0,y_0)\in A'$.

*($A'\subset A$)*: $A$ es cerrado en $\mathbb{R}^2$ por ser preimagen de $\{3\}$ bajo la función continua $\varphi(x,y)=x^2+y+2x$. Como $A$ es cerrado $\Rightarrow A'\subset A$.

$$\boxed{A'=A.}$$

---

## Ej 8 — Límites

**(a)** $\displaystyle\lim_{t\to 0}\bigl(1+3t,\ \sin(t),\ t^2-e^{-2t}\bigr)$

Por **teorema de límites por coordenadas** (Clase #1):

$$\lim = \bigl(\lim(1+3t),\ \lim \sin t,\ \lim(t^2-e^{-2t})\bigr) = (1,\,0,\,-1).$$

**(b)** $\displaystyle\lim_{t\to 2}(t-2)\cdot\bigl(\sin t,\ \ln(t^2+4t-1),\ \tfrac{\sin t}{t^2+1}\bigr)$

Producto de escalar $\varphi(t)=t-2$ por vectorial. Por **teorema de escalar–vectorial** (Clase #2):

$$\lim \varphi\cdot f = (\lim \varphi)\cdot(\lim f) = 0\cdot (\sin 2,\,\ln 11,\,\tfrac{\sin 2}{5}) = (0,0,0).$$

---

## Ej 9 bis — Demostración formal de $\lim_{t\to 2}(t,\,t^3)=(2,8)$

**PP**: dado $\varepsilon>0$, hallar $\delta>0$ tq $0<|t-2|<\delta \Rightarrow \|f(t)-L\|<\varepsilon$.

$$\|f(t)-L\|=\sqrt{(t-2)^2+(t^3-8)^2}.$$

Factor $t^3-8=(t-2)(t^2+2t+4)$:

$$\|f(t)-L\| = |t-2|\sqrt{1+(t^2+2t+4)^2}.$$

Si $|t-2|<1 \Rightarrow 1<t<3 \Rightarrow 0<t^2+2t+4<3^2+2\cdot 3+4=19$.

Luego $\sqrt{1+(t^2+2t+4)^2}<\sqrt{1+361}=\sqrt{362}$.

**Tomamos** $\delta=\min\{1,\,\varepsilon/\sqrt{362}\}$. $\blacksquare$

---

## Ej 9 — Límites con demostración formal

**(c)** Pruebe $\displaystyle\lim_{t\to 1}(t-1,\ t^2-1)=(0,0)$ con definición $\varepsilon$–$\delta$.

**PP**: dado $\varepsilon>0$, hallar $\delta>0$ tal que $0<|t-1|<\delta \Rightarrow \|f(t)-L\|<\varepsilon$.

$$\|f(t)-L\|=\sqrt{(t-1)^2+(t^2-1)^2}=\sqrt{(t-1)^2+(t-1)^2(t+1)^2}=|t-1|\sqrt{1+(t+1)^2}.$$

**Acotamos**: si $|t-1|<1 \Rightarrow 0<t<2 \Rightarrow |t+1|<3 \Rightarrow \sqrt{1+(t+1)^2}<\sqrt{10}$.

**Tomamos** $\delta=\min\{1,\,\varepsilon/\sqrt{10}\}$. Entonces $0<|t-1|<\delta \Rightarrow \|f(t)-L\|<\delta\sqrt{10}\leq \varepsilon$. $\blacksquare$

---

## Ej 10 — Analice la existencia de los siguientes límites

**(a)** $\displaystyle\lim_{t\to 3}\left(\sqrt{t^2-1},\ 5t+\tfrac{1}{2}-t,\ 1-\sqrt{t}\right)$.

**Dominios de las coordenadas**:
- $\sqrt{t^2-1}$: requiere $t^2\geq 1$, i.e., $t\in(-\infty,-1]\cup[1,+\infty)$. En $t=3$, está definida.
- $5t+\tfrac{1}{2}-t = 4t+\tfrac{1}{2}$: polinomio, definido en $\mathbb{R}$.
- $1-\sqrt{t}$: requiere $t\geq 0$. Está definida en $t=3$.

Todas las coordenadas son **continuas** en un entorno de $t=3$. Por teorema de límites por coordenadas, el límite existe y es el valor de la función:

$$\boxed{\lim_{t\to 3} = \left(\sqrt{8},\ \tfrac{25}{2},\ 1-\sqrt{3}\right)=\left(2\sqrt{2},\ \tfrac{25}{2},\ 1-\sqrt{3}\right).}$$

**(b)** $\displaystyle\lim_{t\to\pi/2}\left(\frac{1-\sin t}{\cos t},\ \frac{1+\cos 2t}{t-\pi/2}\right)$.

*Primera coordenada*: en $t=\pi/2$, $1-\sin t=0$ y $\cos t=0$ (indeterminación $0/0$).

Multiplicamos por el conjugado:

$$\frac{1-\sin t}{\cos t}\cdot\frac{1+\sin t}{1+\sin t} = \frac{1-\sin^2 t}{\cos t(1+\sin t)} = \frac{\cos^2 t}{\cos t(1+\sin t)} = \frac{\cos t}{1+\sin t}.$$

$$\lim_{t\to\pi/2}\frac{\cos t}{1+\sin t} = \frac{0}{2} = 0.$$

*Segunda coordenada*: $1+\cos 2t = 2\cos^2 t$. En $t=\pi/2$: $2\cdot 0 = 0$; denominador también $0$.

$$\frac{2\cos^2 t}{t-\pi/2}.$$

Por L'Hôpital: $\displaystyle\lim_{t\to\pi/2}\frac{2\cos^2 t}{t-\pi/2}=\lim\frac{-4\cos t\sin t}{1}=0$.

Por teorema de límites por coordenadas:

$$\boxed{\lim_{t\to\pi/2} = (0,\,0).}$$

---

## Ej 11 — Si $f\colon I\to\mathbb{R}^n$ continua en $a$, entonces $\|f\|\colon I\to\mathbb{R}$ continua en $a$. Recíproco falso.

**(a) Prueba**: usamos la desigualdad triangular inversa

$$\bigl|\,\|f(t)\|-\|f(a)\|\,\bigr|\leq \|f(t)-f(a)\|.$$

Dado $\varepsilon>0$, por continuidad de $f$ en $a$ (Clase #2) existe $\delta>0$ tq $|t-a|<\delta \Rightarrow \|f(t)-f(a)\|<\varepsilon$. Entonces $\bigl|\|f(t)\|-\|f(a)\|\bigr|<\varepsilon$. $\blacksquare$

**(b) Contraejemplo al recíproco**: sea $f\colon\mathbb{R}\to\mathbb{R}^2$ definida por

$$f(t)=\begin{cases}(1,0), & t\geq 0\\ (-1,0), & t<0.\end{cases}$$

Entonces $\|f(t)\|=1$ para todo $t$ (constante, continua), pero $f$ tiene salto en $t=0$:

$$\lim_{t\to 0^-} f(t)=(-1,0)\neq (1,0)=\lim_{t\to 0^+}f(t).$$

Luego $f$ no es continua en $0$ pese a que $\|f\|$ sí lo es.

---

## Ej 12 — Dominio natural y continuidad

### (a) $f(1)=(1,1,0)$ y $f(t)=\left(\dfrac{\sin(t-1)}{t-1},\ \dfrac{t^2-1}{2(t-1)},\ (t-1)\ln|t-1|\right)$ para $t\neq 1$

**Dominio**: cada coordenada está definida para $t\neq 1$. En $t=1$ está definida por el valor $(1,1,0)$. Entonces $\operatorname{Dom} f = \mathbb{R}$.

**Continuidad en $t\neq 1$**: por coordenadas (elementales, composiciones).

**Continuidad en $t=1$**: analizamos $\lim_{t\to 1}f(t)$.
- $\lim\dfrac{\sin(t-1)}{t-1}=1$ (límite fundamental con $u=t-1$)
- $\dfrac{t^2-1}{2(t-1)}=\dfrac{t+1}{2}$ para $t\neq 1 \Rightarrow \lim = 1$
- $\lim(t-1)\ln|t-1|=0$ (pues $u\ln|u|\to 0$ cuando $u\to 0$)

$$\lim_{t\to 1}f(t) = (1,\,1,\,0) = f(1) \Rightarrow f \text{ es continua en } 1.$$

$$\boxed{\operatorname{Dom} f = \mathbb{R},\quad f \text{ es continua en todo } \mathbb{R}.}$$

### (b) $f(0)=(e,e,e)$ y $f(t)=\left((1+t)^{1/t},\ e^{1+t},\ \dfrac{e^{1-t}}{1-t}\right)$ para $t\neq 0$

**Dominio de cada coordenada**:
- $(1+t)^{1/t}$: requiere $1+t>0$ (para potencia real) y $t\neq 0$, es decir $t>-1,\,t\neq 0$. En $t=0$ se define aparte.
- $e^{1+t}$: $\mathbb{R}$.
- $\dfrac{e^{1-t}}{1-t}$: $t\neq 1$.

$$\boxed{\operatorname{Dom} f = (-1,\,1)\cup(1,+\infty) \text{ (incluye } t=0\text{).}}$$

**Continuidad en $t=0$**: límites
- $\lim_{t\to 0}(1+t)^{1/t}=e$ (límite fundamental)
- $\lim e^{1+t}=e$
- $\lim\dfrac{e^{1-t}}{1-t}=\dfrac{e}{1}=e$

$\lim f = (e,e,e) = f(0) \Rightarrow$ continua en $0$.

**Continuidad en $t\neq 0,\,t\neq 1$**: por coordenadas (continuas).

$$\boxed{f \text{ es continua en } \operatorname{Dom} f.}$$

### (c) $f(t)=\left(\dfrac{1}{t-|\lfloor t\rfloor|},\ \sqrt{|t|-3},\ t^3\right)$

**Dominio**:
- $\sqrt{|t|-3}$: requiere $|t|\geq 3 \Rightarrow t\in(-\infty,-3]\cup[3,+\infty)$.
- $\dfrac{1}{t-|\lfloor t\rfloor|}$: requiere $t\neq|\lfloor t\rfloor|$.
- $t^3$: todo $\mathbb{R}$.

*Análisis para $t\geq 3$*: $|\lfloor t\rfloor|=\lfloor t\rfloor$ (entero positivo). $t-\lfloor t\rfloor = \{t\}$ (parte fraccionaria). Se anula $\Leftrightarrow t\in\mathbb{Z}$. Luego se excluyen $t=3,4,5,\ldots$

*Análisis para $t\leq -3$*: $\lfloor t\rfloor\leq -3$, $|\lfloor t\rfloor| = -\lfloor t\rfloor\geq 3$. $t-|\lfloor t\rfloor| = t+\lfloor t\rfloor$. Como $t<0$ y $\lfloor t\rfloor<0$, la suma es $<0$, nunca $0$. Todos los $t\leq -3$ sirven.

$$\boxed{\operatorname{Dom} f = (-\infty,\,-3]\ \cup\ \bigcup_{k=3}^{\infty}(k,\,k+1).}$$

**Continuidad**: en $\operatorname{Dom} f$, cada coordenada es continua (las discontinuidades de $\lfloor \cdot \rfloor$ están excluidas del dominio). $\Rightarrow f$ es continua en $\operatorname{Dom} f$.

### (d) $g(t)=\left(\arcsin(t),\ \sqrt{t},\ \dfrac{1}{t-\pi/2}\right)$

**Dominios**:
- $\arcsin(t)$: $[-1,1]$.
- $\sqrt{t}$: $[0,+\infty)$.
- $\dfrac{1}{t-\pi/2}$: $\mathbb{R}\setminus\{\pi/2\}$.

Intersección: $[0,1]\cap(\mathbb{R}\setminus\{\pi/2\})=[0,1]$ (pues $\pi/2\approx 1.57>1$, no está en $[0,1]$).

$$\boxed{\operatorname{Dom} g = [0,\,1],\quad g \text{ es continua en } [0,1].}$$

---

## Ej 13 — Continuidad por partes de $f$

$$f(t)=\begin{cases}(t,\,0,\,e^{-1/t^2}), & t>0\\ (t,\,e^{-1/t^2},\,0), & t<0\\ (0,0,0), & t=0.\end{cases}$$

**En $t\neq 0$**: cada coordenada es continua (composición/producto de elementales) $\Rightarrow f$ continua por **continuidad por coordenadas** (Clase #2).

**En $t=0$**: $f(0)=(0,0,0)$. Analizamos límites laterales:

$$\lim_{t\to 0^+} f(t)=(0,\,0,\,\lim_{t\to 0^+} e^{-1/t^2})=(0,0,0),\quad \text{pues } e^{-1/t^2}\to 0.$$

$$\lim_{t\to 0^-} f(t)=(0,\,\lim e^{-1/t^2},\,0)=(0,0,0) \text{ por el mismo motivo}.$$

Ambos coinciden con $f(0) \Rightarrow f$ es continua en $0 \Rightarrow$ **$f$ es continua en todo $\mathbb{R}$**.

---

## Ej 14 — Camino diferenciable $f\colon\mathbb{R}\to\mathbb{R}^2$ con $f(\mathbb{R})=G=\{(x,y):y=|x|\}$ y $f(0)=(0,0)$

**Problema**: $y=|x|$ tiene una esquina en el origen, así que $(x,|x|)$ no es diferenciable en $t=0$.

**Idea**: componer con una función que "aplana" la esquina, como $x=t^3$. Como $t^3$ cubre todo $\mathbb{R}$ (es biyectiva y suave), obtenemos:

$$f(t)=(t^3,\,|t^3|)=(t^3,\,|t|^3).$$

**Diferenciabilidad**:
- Para $t>0$: $|t|^3=t^3 \Rightarrow f(t)=(t^3,t^3)$, $f'(t)=(3t^2,3t^2)$.
- Para $t<0$: $|t|^3=-t^3 \Rightarrow f(t)=(t^3,-t^3)$, $f'(t)=(3t^2,-3t^2)$.
- En $t=0$: $\lim_{h\to 0^\pm}\dfrac{f(h)-f(0)}{h}=\lim\dfrac{(h^3,|h|^3)}{h}=\lim(h^2,\,h\cdot|h|\cdot\operatorname{sgn}(h)^?)=(0,0)$.

De hecho, $|t|^3=(t^2)^{3/2}$, y derivando: $\dfrac{d}{dt}(t^2)^{3/2}=\tfrac{3}{2}(t^2)^{1/2}\cdot 2t=3t|t|$. Es **continua en $\mathbb{R}$** y en $t=0$ vale $0$.

$$\boxed{f(t)=(t^3,\,|t|^3),\ t\in\mathbb{R}.\quad f \text{ es diferenciable en todo } \mathbb{R}.}$$

**Verificación**:
- $f(0)=(0,0)$ ✓
- $f(\mathbb{R})=\{(t^3,|t|^3):t\in\mathbb{R}\}=\{(x,|x|):x\in\mathbb{R}\}=G$ ✓
- $f'(0)=(0,0)$ (nota: el vector tangente es cero en el origen, pero sigue siendo **diferenciable**; no es **regular** ahí, pero sí diferenciable).

> **Observación clave**: diferenciabilidad $\not\Leftrightarrow$ regularidad. Una curva puede ser diferenciable y tener $f'=0$ en algún punto, permitiendo "esquinas geométricas" pese a parametrizarse suavemente.

---

## Ej 15 — $\alpha(t)=(t+1,\,t^2-1,\,t^3)$. Recta tangente paralela al plano $\mathcal{P}\colon x+2y+z=1$

**Condición**: recta tangente paralela a $\mathcal{P} \Longleftrightarrow \alpha'(t)$ es perpendicular al vector normal del plano $\mathbf{n}=(1,2,1)$.

$$\alpha'(t)=(1,\,2t,\,3t^2).$$

$$\langle \alpha'(t),\mathbf{n}\rangle = 1+4t+3t^2=0 \Rightarrow t=-1\ \text{ó}\ t=-\tfrac{1}{3}.$$

**Puntos**:

- $t=-1$: $\alpha(-1)=\boxed{(0,\,0,\,-1)}$
- $t=-\tfrac{1}{3}$: $\alpha(-\tfrac{1}{3})=\boxed{(2/3,\,-8/9,\,-1/27)}$

---

## Ej 16 — Diferenciabilidad de $f$ del ejercicio 13

**En $t\neq 0$**: $f$ diferenciable por coordenadas.

**En $t=0$**: derivadas laterales:

$$f'(0^+)=\lim_{h\to 0^+}\frac{f(h)-f(0)}{h}=\lim \frac{(h,\,0,\,e^{-1/h^2})}{h}=\left(1,\,0,\,\lim\frac{e^{-1/h^2}}{h}\right)=(1,0,0).$$

(porque $e^{-1/h^2}$ decae a $0$ más rápido que cualquier potencia)

$$f'(0^-)=\lim_{h\to 0^-}\frac{(h,\,e^{-1/h^2},\,0)}{h}=(1,0,0) \text{ por análogo.}$$

Ambos coinciden $\Rightarrow$ **$f$ es diferenciable en $0$** con $f'(0)=(1,0,0)$.

**Conclusión**: $f$ diferenciable en todo $\mathbb{R}$.

---

## Ej 17 — $f(t)=(t^2\sin(1/t),\,|t|^{5/2}\sin(1/t))$ si $t\neq 0$; $(0,0)$ si $t=0$. Halle $f'(0)$.

Por definición (Clase #2):

$$f'(0)=\lim_{h\to 0}\frac{f(h)-f(0)}{h}=\lim_{h\to 0}\bigl(h\sin(1/h),\ |h|^{3/2}\sin(1/h)\bigr).$$

Por **acotación** ($|\sin(1/h)|\leq 1$):

- $|h\sin(1/h)|\leq |h|\to 0$
- $|h|^{3/2}|\sin(1/h)|\leq |h|^{3/2}\to 0$

Por teorema de límites por coordenadas:

$$\boxed{f'(0)=(0,0).}$$

---

## Ej 18 — Reglas de derivación

Sean $f,g\colon I\to \mathbb{R}^n$ y $\alpha\colon I\to\mathbb{R}$ diferenciables. Todas se prueban **por coordenadas** y regla del producto en $\mathbb{R}$.

**(a)** $(f+g)'(t)=f'(t)+g'(t)$

*Prueba*: por coordenadas, $(f+g)_i=f_i+g_i$ y $(f_i+g_i)'=f_i'+g_i'$ en $\mathbb{R}$. Se reensambla. $\blacksquare$

**(b)** $(\alpha\cdot f)'(t)=\alpha'(t)f(t)+\alpha(t)f'(t)$

*Prueba*: $(\alpha f)_i=\alpha f_i \Rightarrow (\alpha f_i)'=\alpha' f_i + \alpha f_i'$ en $\mathbb{R}$. $\blacksquare$

**(c)** $\langle f,g\rangle'(t)=\langle f'(t),g(t)\rangle + \langle f(t),g'(t)\rangle$

*Prueba*: $\langle f,g\rangle = \sum f_i g_i$. Derivando: $\sum(f_i' g_i + f_i g_i')=\langle f',g\rangle + \langle f,g'\rangle$. $\blacksquare$

**(d)** Si $f(t)\neq 0$: $(\|f(t)\|)' = \dfrac{\langle f(t),f'(t)\rangle}{\|f(t)\|}$

*Prueba*: $\|f\|^2=\langle f,f\rangle$. Derivando con (c):

$$2\|f\|\cdot(\|f\|)' = 2\langle f,f'\rangle \Rightarrow (\|f\|)' = \frac{\langle f,f'\rangle}{\|f\|}.\quad \blacksquare$$

---

## Ej 19 — $f(t)\neq 0$ y $f'(t)\parallel f(t)$ para todo $t$. Probar que $g(t)=f(t)/\|f(t)\|$ es constante.

> *(Asumimos el denominador es $\|f(t)\|$; si dice $\|\alpha(t)\|$ es errata tipográfica.)*

**Hipótesis**: $f'(t)=\lambda(t)\cdot f(t)$ para alguna función escalar $\lambda$.

**Calculamos** $g'(t)$ usando regla del cociente y (d) del ejercicio 18:

$$g' = \frac{f'\cdot\|f\| - f\cdot(\|f\|)'}{\|f\|^2}.$$

Como $f'=\lambda f$: $\langle f,f'\rangle = \lambda\|f\|^2 \Rightarrow (\|f\|)'=\lambda\|f\|$.

Sustituyendo:

$$g' = \frac{\lambda f\cdot \|f\| - f\cdot \lambda\|f\|}{\|f\|^2} = 0.$$

Luego **$g$ es constante**. $\blacksquare$

---

## Ej 20 — Recta tangente a $\operatorname{tra}(f)$ en el punto donde $\operatorname{tra}(f)\cap\operatorname{tra}(g)\neq\emptyset$

$f(t)=(t+1,\,e^{1+t},\,t+t^2)$, $t\geq 0$; $g(t)=(3/(t+1),\,e^{4t},\,2t+1)$, $t\geq 0$.

**Punto de intersección**: resolver $f(t_1)=g(t_2)$.

- De la 2ª coordenada: $e^{1+t_1}=e^{4t_2} \Rightarrow 1+t_1=4t_2 \Rightarrow t_1=4t_2-1$.
- De la 1ª coordenada: $(t_1+1)(t_2+1)=3 \Rightarrow 4t_2(t_2+1)=3 \Rightarrow 4t_2^2+4t_2-3=0 \Rightarrow t_2=\tfrac{1}{2}$ (descartamos $-\tfrac{3}{2}$). Luego $t_1=1$.
- Verificación 3ª coordenada: $t_1+t_1^2=2$; $2t_2+1=2$. ✓

**Punto**: $f(1)=(2,\,e^2,\,2)$.

**Vector velocidad**: $f'(t)=(1,\,e^{1+t},\,1+2t) \Rightarrow f'(1)=(1,\,e^2,\,3)$.

**Recta tangente** (Clase #2):

$$P(s)=f(1)+s\cdot f'(1) = (2+s,\ e^2(1+s),\ 2+3s),\quad s\in\mathbb{R}.$$

---

## Ej 21 — Regla de la cadena

$\mathbf{r}(t)=(\cos t,\,\sin t,\,t)$, $\mathbf{s}(u)=(u^2,\,e^u,\,\ln(1+u^2))$, $\varphi\colon\mathbb{R}\to\mathbb{R}$ diferenciable.

### (a) $\mathbf{F}(t)=\mathbf{s}(\varphi(t))$. Calcular $\mathbf{F}'(t)$.

Por **regla de la cadena** (Clase #3): $\mathbf{F}'(t)=\mathbf{s}'(\varphi(t))\cdot \varphi'(t)$.

$$\mathbf{s}'(u)=\left(2u,\,e^u,\,\frac{2u}{1+u^2}\right).$$

$$\boxed{\mathbf{F}'(t)=\left(2\varphi(t),\,e^{\varphi(t)},\,\frac{2\varphi(t)}{1+\varphi(t)^2}\right)\cdot \varphi'(t).}$$

### (b) $h(t)=\langle \mathbf{r}(t),\mathbf{s}(t^2)\rangle$. Calcular $h'(t)$.

Por regla del producto interno (ej 18c):

$$h'(t)=\langle \mathbf{r}'(t),\mathbf{s}(t^2)\rangle + \langle \mathbf{r}(t),\tfrac{d}{dt}\mathbf{s}(t^2)\rangle.$$

- $\mathbf{r}'(t)=(-\sin t,\,\cos t,\,1)$
- $\mathbf{s}(t^2)=(t^4,\,e^{t^2},\,\ln(1+t^4))$
- $\tfrac{d}{dt}\mathbf{s}(t^2)=\mathbf{s}'(t^2)\cdot 2t = (4t^3,\,2t\,e^{t^2},\,\tfrac{4t^3}{1+t^4})$

$$h'(t)=-t^4\sin t + e^{t^2}\cos t + \ln(1+t^4) + 4t^3\cos t + 2t\,e^{t^2}\sin t + \frac{4t^4}{1+t^4}.$$

### (c) $G(t)=\|\mathbf{r}(\sin t)\|^2$. Calcular $G'(t)$.

**Truco**: $\|\mathbf{r}(u)\|^2 = \cos^2 u+\sin^2 u+u^2 = 1+u^2$. Luego $G(t)=1+\sin^2 t$.

$$\boxed{G'(t)=2\sin t\cos t=\sin(2t).}$$

*(Alternativa con cadena: $G(t)=\langle \mathbf{r}(\sin t),\mathbf{r}(\sin t)\rangle$, $G'(t)=2\langle \mathbf{r},\mathbf{r}'\rangle \cos t = 2\sin t\cos t$.)*

---

## Notas para el examen

1. **Cita siempre el teorema** que estás usando. Los profesores de UNI valoran la fundamentación: *"Por el teorema de límites por coordenadas (Clase #1)..."*, *"Por continuidad por coordenadas..."*, *"Por el TVM generalizado en $\mathbb{R}^n$..."*.
2. Si una prueba $\varepsilon$–$\delta$ se vuelve engorrosa, **reduce al caso real por coordenadas** (teorema: $\lim f = L \Leftrightarrow \lim f_i = L_i$).
3. **TVM clásico no vale en $\mathbb{R}^n$**: no escribas $\tfrac{f(b)-f(a)}{b-a}=f'(c)$. Usa TVM por coordenadas (con $c_1,\dots,c_n$ distintos) o la versión $\langle f(b)-f(a),\,f'(c)\rangle = 0$.
4. **Diferenciabilidad $\Rightarrow$ continuidad**, pero no al revés.
5. Si te piden diferenciabilidad en punto frontera, calcula **derivadas laterales** y verifica que coinciden.
6. **Dibuja siempre** dominios, trayectorias y trazas — la profe espera esto.
