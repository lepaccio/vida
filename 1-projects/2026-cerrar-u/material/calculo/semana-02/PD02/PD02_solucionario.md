# Solucionario PD2 — CM2A1 2026-1

> Temas: integración vectorial, longitud de arco, parametrización por longitud de arco, triedro de Frenet $\{T,N,B\}$, curvatura $\kappa$, torsión $\tau$.
> Notación de clase: $v(t)=\|f'(t)\|$ (rapidez), $T=f'/\|f'\|$, $N=T'/\|T'\|$, $B=T\times N$, $\kappa=\|f'\times f''\|/\|f'\|^3$, $\tau=\langle f'\times f'', f'''\rangle/\|f'\times f''\|^2$.

---

## Ej 1 — Integrales de funciones vectoriales

**Definición** (Clase #3, apertura):

$$\int_a^b f(t)\,dt = \left(\int_a^b f_1(t)\,dt,\,\dots,\,\int_a^b f_n(t)\,dt\right).$$

**(a)** $\displaystyle\int_0^1 (t,\,\sqrt{t},\,e^t)\,dt$:

- $\int_0^1 t\,dt = \tfrac{1}{2}$
- $\int_0^1 \sqrt{t}\,dt = \bigl[\tfrac{2}{3}t^{3/2}\bigr]_0^1 = \tfrac{2}{3}$
- $\int_0^1 e^t\,dt = e-1$

$$\boxed{\text{Resultado: }(1/2,\,2/3,\,e-1).}$$

**(b)** $\displaystyle\int_0^1 \left(\tfrac{e^t}{1+e^t},\,\tfrac{1}{1+e^t}\right)\,dt$:

- $\int_0^1 \tfrac{e^t}{1+e^t}\,dt = \bigl[\ln(1+e^t)\bigr]_0^1 = \ln(1+e) - \ln 2 = \ln\!\left(\tfrac{1+e}{2}\right)$.
- $\int_0^1 \tfrac{1}{1+e^t}\,dt$: usa $\tfrac{1}{1+e^t} = 1 - \tfrac{e^t}{1+e^t}$:

$$\int_0^1 = \bigl[t-\ln(1+e^t)\bigr]_0^1 = 1 - \ln(1+e) + \ln 2 = 1 + \ln\!\left(\tfrac{2}{1+e}\right).$$

---

## Ej 2 — Dado $f'(t)=(\sin^2 t,\,2\cos^2 t)$, $f(\pi)=(0,0)$, hallar $f(t)$

$$f(t)=f(\pi)+\int_\pi^t f'(u)\,du.$$

- $\int \sin^2 u\,du = \tfrac{u}{2}-\tfrac{\sin(2u)}{4}$
- $\int 2\cos^2 u\,du = u+\tfrac{\sin(2u)}{2}$

Evaluando y usando $f(\pi)=(0,0)$:

$$\boxed{f(t)=\left(\tfrac{t}{2}-\tfrac{\sin(2t)}{4}-\tfrac{\pi}{2},\ t+\tfrac{\sin(2t)}{2}-\pi\right).}$$

---

## Ej 5 — Longitud de la trayectoria

**Definición**: $\displaystyle L=\int_a^b \|f'(t)\|\,dt$.

**(a)** $f(t)=(t^2,\,t\sin t,\,t\cos t)$, $t\in[0,1]$.

$$f'(t)=(2t,\,\sin t+t\cos t,\,\cos t - t\sin t).$$

$$\|f'\|^2 = 4t^2 + \sin^2 t + 2t\sin t\cos t + t^2\cos^2 t + \cos^2 t - 2t\sin t\cos t + t^2\sin^2 t = 1+5t^2.$$

$$L=\int_0^1 \sqrt{1+5t^2}\,dt.$$

Usando $\int\sqrt{a^2+u^2}\,du = \tfrac{u}{2}\sqrt{a^2+u^2}+\tfrac{a^2}{2}\ln|u+\sqrt{a^2+u^2}|$ con sustitución $u=\sqrt{5}t$:

$$\boxed{L=\tfrac{\sqrt{6}}{2}+\tfrac{1}{2\sqrt{5}}\ln(\sqrt{5}+\sqrt{6}).}$$

**(b)** $f(t)=(e^t\cos t,\,e^t\sin t,\,e^t)$, $t\in[0,2\pi]$ *(hélice exponencial)*.

$$f'(t)=e^t(\cos t-\sin t,\,\sin t+\cos t,\,1).$$

$$\|f'\|^2 = e^{2t}[(\cos t-\sin t)^2+(\sin t+\cos t)^2+1] = 3e^{2t} \Rightarrow \|f'\|=\sqrt{3}\,e^t.$$

$$\boxed{L=\int_0^{2\pi}\sqrt{3}\,e^t\,dt = \sqrt{3}(e^{2\pi}-1).}$$

---

## Ej 4 — Parametrizar por longitud de arco

**Método general**:

1. Calcular $s(t)=\int_{t_0}^{t}\|f'(u)\|\,du$.
2. Invertir $t=t(s)$.
3. Definir $\alpha(s)=f(t(s))$. Se verifica $\|\alpha'(s)\|=1$.

**(c)** $f(t)=(a\cos t,\,a\sin t,\,a\ln(\cos t))$, desde $t=0$ hasta $t=\pi/4$.

$$f'(t)=(-a\sin t,\,a\cos t,\,-a\tan t).$$

$$\|f'\|^2 = a^2(\sin^2 t+\cos^2 t+\tan^2 t) = a^2(1+\tan^2 t) = a^2\sec^2 t \Rightarrow \|f'\|=a\sec t.$$

$$s(t)=\int_0^t a\sec u\,du = a\ln(\sec t + \tan t).$$

**Invertir**: sea $\sigma=s/a$. Entonces $\sec t+\tan t = e^\sigma$. Usando la identidad $(\sec t+\tan t)(\sec t-\tan t)=1$:

$$\cos t = \frac{2e^\sigma}{e^{2\sigma}+1}=\operatorname{sech}(\sigma),\quad \sin t = \tanh(\sigma),\quad \ln(\cos t)=-\ln(\cosh\sigma).$$

$$\boxed{\alpha(s)=\bigl(a\operatorname{sech}(s/a),\,a\tanh(s/a),\,-a\ln(\cosh(s/a))\bigr),\ s\in[0,\,a\ln(1+\sqrt{2})].}$$

---

## Ej 6 — Parametrizar por arco: $f(t)=(a\cos t,\,a\sin t,\,c)$ *(círculo en plano $z=c$)*

*Asumimos $a>0$ constante (si fuera $b\neq a$ sería elipse $\Rightarrow$ integral elíptica, sin forma cerrada).*

$$f'(t)=(-a\sin t,\,a\cos t,\,0) \Rightarrow \|f'\|=a \text{ (constante)}.$$

$$s(t)=at \Rightarrow t=s/a.$$

$$\boxed{\alpha(s)=(a\cos(s/a),\,a\sin(s/a),\,c),\ s\in[0,\,2\pi a].}$$

---

## Ej 8 — Verificar parametrización por arco y ortogonalidad $f''\perp f'$

$f(s)=(\alpha\cos(ks),\,\alpha\sin(ks),\,\beta s\,k)$ donde $k=1/\sqrt{\alpha^2+\beta^2}$.

$$f'(s)=(-\alpha k\sin(ks),\,\alpha k\cos(ks),\,\beta k).$$

$$\|f'\|^2 = k^2(\alpha^2\sin^2+\alpha^2\cos^2+\beta^2) = k^2(\alpha^2+\beta^2) = 1 \quad ✓ \text{ parametrización por arco.}$$

$$f''(s) = (-\alpha k^2\cos(ks),\,-\alpha k^2\sin(ks),\,0) \Rightarrow \|f''\|=\alpha k^2 = \frac{\alpha}{\alpha^2+\beta^2}.$$

$$\langle f',f''\rangle = \alpha^2 k^3\sin\cos - \alpha^2 k^3\sin\cos + 0 = 0 \quad ✓ \text{ ortogonales.}$$

---

## Ej 9 — Prueba: en parametrización por arco, $f''(s)\perp f'(s)$

**Hipótesis**: $\|f'(s)\|=1 \Rightarrow \langle f',f'\rangle = 1$ (constante).

**Derivando** respecto a $s$ (regla del producto interno, PD1 ej 18c):

$$2\langle f'(s),\,f''(s)\rangle = 0 \Rightarrow \langle f',f''\rangle = 0 \Rightarrow f''\perp f'. \quad \blacksquare$$

---

## Ej 10 — Recta normal a $f(t)=(2\cos t,\,1+2\sin t)$ en $P=(\sqrt{3},\,2)$

**Encontrar $t_0$**: $2\cos t=\sqrt{3}\ \land\ 1+2\sin t=2 \Rightarrow \cos t=\tfrac{\sqrt{3}}{2},\,\sin t=\tfrac{1}{2} \Rightarrow t_0=\pi/6$.

**Vector tangente**: $f'(t)=(-2\sin t,\,2\cos t) \Rightarrow f'(\pi/6)=(-1,\,\sqrt{3})$.

**Vector normal** (perpendicular a $f'(\pi/6)$ en $\mathbb{R}^2$): rotar $90°$ $\Rightarrow \mathbf{n}=(\sqrt{3},\,1)$.

**Recta normal** (parametrizada):

$$\boxed{r(s)=(\sqrt{3},\,2)+s\cdot(\sqrt{3},\,1),\ s\in\mathbb{R}.}$$

Ecuación cartesiana: $y=\tfrac{x}{\sqrt{3}}+1$, equivalentemente $x-\sqrt{3}y+\sqrt{3}=0$.

---

## Ej 11 — Prueba: $(f\times g)' = f'\times g + f\times g'$

$f,g\colon I\to\mathbb{R}^3$ diferenciables. Sean $f=(f_1,f_2,f_3)$, $g=(g_1,g_2,g_3)$.

$$f\times g = (f_2 g_3 - f_3 g_2,\ f_3 g_1 - f_1 g_3,\ f_1 g_2 - f_2 g_1).$$

Derivando cada coordenada con regla del producto en $\mathbb{R}$:

$$(f_2 g_3 - f_3 g_2)' = f_2' g_3 + f_2 g_3' - f_3' g_2 - f_3 g_2' = (f'\times g)_1 + (f\times g')_1.$$

Análogo para las otras dos. Reensamblando:

$$\boxed{(f\times g)'(t) = f'(t)\times g(t) + f(t)\times g'(t).}\quad \blacksquare$$

---

## Ej 12 — Triedro $T(t)=f'/\|f'\|$, $N(t)=T'/\|T'\|$, $B(t)=T\times N$

**(a) Unitarios y ortogonales**:

- $\|T\|=\|N\|=1$ por construcción.
- **$T\perp N$**: $\langle T,T\rangle=1 \Rightarrow$ derivando $\langle T',T\rangle=0$. Como $N\parallel T'$, entonces $T\perp N$.
- **$B\perp T$ y $B\perp N$**: propiedad del producto vectorial.
- $\|B\| = \|T\|\cdot\|N\|\cdot|\sin\angle(T,N)| = 1\cdot 1\cdot 1 = 1$ (ángulo recto).

**(b) $B'=T\times N'$**:

Por ejercicio 11:

$$B' = (T\times N)' = T'\times N + T\times N'.$$

Pero $T'=\|T'\|\cdot N$ (definición de $N$). Entonces $T'\times N = \|T'\|(N\times N)=0$.

$$\boxed{B' = T\times N'.} \quad \blacksquare$$

**(c) $B'(t)\parallel N(t)$**:

- $B'\perp B$ (pues $\|B\|^2=1 \Rightarrow \langle B,B'\rangle=0$).
- $B'=T\times N' \Rightarrow B'\perp T$.

Como $B'$ es ortogonal a $T$ y a $B$, y estamos en $\mathbb{R}^3$, $B'$ debe ser paralelo a $N$. Por tanto existe $\nu(t)$ escalar tal que $B'(t)=\nu(t)\cdot N(t)$. $\blacksquare$

> **Nota**: $\nu(t)$ se llama **torsión** (también escrita $\tau=-\nu$ según convención).

---

## Ej 13 — Curva $\mathcal{C}:\ x^2+y^2=1\ \cap\ 2x+3y+z=3$

**(a) Parametrización regular**

El círculo $x^2+y^2=1$ se parametriza con $x=\cos t,\,y=\sin t$, y $z$ queda determinada por el plano:

$$\lambda(t)=(\cos t,\,\sin t,\,3-2\cos t - 3\sin t),\quad t\in[0,2\pi].$$

**Regular**: $\lambda'(t)=(-\sin t,\,\cos t,\,2\sin t - 3\cos t)$. Siempre $\neq(0,0,0)$ porque $(-\sin t,\cos t)$ nunca es $(0,0)$. ✓

**(b) Descomposición** $\lambda''(t)=f(t)T(t)+g(t)N(t)$

**Clave**: si $v(t)=\|\lambda'(t)\|$ es la rapidez, entonces $\lambda'=v\cdot T$ y por tanto:

$$\lambda'' = v'\,T + v\,T' = v'\,T + v^2\kappa\,N.$$

Luego $\boxed{f(t)=v'(t),\quad g(t)=v(t)^2\kappa(t).}$

**Cálculos**:

$$v^2 = \|\lambda'\|^2 = 1+(2\sin t - 3\cos t)^2 = 5+5\cos^2 t - 6\sin(2t).$$

$$\lambda'\times\lambda'' = (2,\,3,\,1) \text{ constante}.$$

*(Los detalles: $i$: $\cos t(2\cos t+3\sin t) - (2\sin t-3\cos t)(-\sin t) = 2$; $j$: $3$; $k$: $\sin^2 t+\cos^2 t=1$.)*

$$\|\lambda'\times\lambda''\| = \sqrt{14}.$$

$$\kappa(t)=\frac{\sqrt{14}}{v(t)^3} \Rightarrow g(t)=v^2\kappa = \frac{\sqrt{14}}{v(t)}.$$

$$f(t)=v'(t) \text{ (usar cadena en } v=\sqrt{5+5\cos^2 t - 6\sin 2t}\text{)}.$$

**(c) Plano osculador en $P=(1,0,1)$**

Corresponde a $t=0$ ($\cos 0=1$, $\sin 0=0$, $z=3-2=1$). ✓

Normal al plano osculador $=\lambda'\times\lambda''=(2,3,1)$.

$$\boxed{\text{Plano osculador: } 2(x-1)+3y+(z-1)=0 \Rightarrow 2x+3y+z=3.}$$

> **Observación clave**: el plano osculador coincide con el plano original $2x+3y+z=3$. Esto ocurre porque **la curva está contenida en ese plano** (curva plana) y por tanto el plano osculador es constante. Consecuencia: **torsión $\tau\equiv 0$**.

---

## Ej 15 — $f(t)=(e^t\cos t,\,e^t\sin t,\,e^t)$. Calcular $T$, $N$, $B$, $\kappa$, $\tau$

$$f'(t)=e^t(\cos t-\sin t,\,\sin t+\cos t,\,1),\quad \|f'\|=\sqrt{3}\,e^t.$$

$$\boxed{T(t)=\frac{1}{\sqrt{3}}(\cos t-\sin t,\,\sin t+\cos t,\,1).}$$

$$f''(t)=e^t(-2\sin t,\,2\cos t,\,1).$$

$$f'\times f'' = e^{2t}(\sin t-\cos t,\,-\sin t-\cos t,\,2),\quad \|f'\times f''\|=\sqrt{6}\,e^{2t}.$$

$$\boxed{B(t)=\frac{1}{\sqrt{6}}(\sin t-\cos t,\,-\sin t-\cos t,\,2).}$$

$$\boxed{\kappa(t)=\frac{\|f'\times f''\|}{\|f'\|^3}=\frac{\sqrt{6}\,e^{2t}}{3\sqrt{3}\,e^{3t}}=\frac{\sqrt{2}}{3e^t}.}$$

$$\boxed{N(t)=B\times T=\frac{1}{\sqrt{2}}(-(\sin t+\cos t),\,\cos t-\sin t,\,0).}$$

*(Verificación $\|N\|=1$.)*

$$f'''(t)=e^t(-2\sin t-2\cos t,\,2\cos t-2\sin t,\,1).$$

$$\langle f'\times f'',f'''\rangle = 2e^{3t} \text{ (los términos cruzados cancelan)}.$$

$$\boxed{\tau(t)=\frac{\langle f'\times f'',f'''\rangle}{\|f'\times f''\|^2}=\frac{2e^{3t}}{6e^{4t}}=\frac{1}{3e^t}.}$$

---

## Ej 16 — Planos osculador, rectificante y normal

**Definiciones**:

- **Plano osculador** en $f(t_0)$: generado por $T(t_0)$ y $N(t_0)$. Normal $=B(t_0)$.
- **Plano rectificante**: generado por $T$ y $B$. Normal $=N$.
- **Plano normal**: generado por $N$ y $B$. Normal $=T$ (o $f'$).

**(a)** $f(t)=(e^t\cos t,\,e^t\sin t,\,e^t)$, $t=0$.

$f(0)=(1,0,1)$. Del ejercicio 15:

- $T(0)=\tfrac{1}{\sqrt{3}}(1,1,1)$ (normal al plano normal)
- $N(0)=\tfrac{1}{\sqrt{2}}(-1,1,0)$ (normal al plano rectificante)
- $B(0)\propto f'(0)\times f''(0)=(-1,-1,2)$ (normal al plano osculador)

$$\boxed{\text{Plano normal: } x+y+z=2.}$$

$$\boxed{\text{Plano rectificante: } x-y=1.}$$

$$\boxed{\text{Plano osculador: } -(x-1)-y+2(z-1)=0 \Rightarrow x+y-2z+1=0.}$$

**(b)** $f(t)=(1,\,t^2/2,\,t^3/3)$, $t=1$.

$f(1)=(1,\,1/2,\,1/3)$. $f'(1)=(0,1,1)$. $f''(1)=(0,1,2)$.

$$f'\times f''=(2-1,\,0-0,\,0-0)=(1,0,0).$$

$$\boxed{\text{Plano normal (}n=f'\text{): } y+z=\tfrac{5}{6}.}$$

$$\boxed{\text{Plano osculador (}n=(1,0,0)\text{): } x=1.}$$

**Rectificante**: normal $N\propto(f'\times f'')\times f' = (1,0,0)\times(0,1,1)=(0,-1,1)$.

$$\boxed{\text{Plano rectificante: } -(y-\tfrac{1}{2})+(z-\tfrac{1}{3})=0 \Rightarrow y-z=\tfrac{1}{6}.}$$

**(c)** $f(t)=(2\cos t,\,2\sin t,\,t)$, $t=\pi/2$.

$f(\pi/2)=(0,2,\pi/2)$. $f'(\pi/2)=(-2,0,1)$. $f''(\pi/2)=(0,-2,0)$.

$$f'\times f''=(2,0,4)\propto (1,0,2).$$

$$\boxed{\text{Plano normal: } -2x+(z-\tfrac{\pi}{2})=0 \Rightarrow -2x+z=\tfrac{\pi}{2}.}$$

$$\boxed{\text{Plano osculador: } x+2(z-\tfrac{\pi}{2})=0 \Rightarrow x+2z=\pi.}$$

**Rectificante**: $N\propto(f'\times f'')\times f'=(2,0,4)\times(-2,0,1)=(0,-10,0)\propto(0,1,0)$.

$$\boxed{\text{Plano rectificante: } y=2.}$$

---

## Ej 17 — Pruebe $f(t)=(t,\,(1+t)/t,\,(1-t^2)/t)$ está contenida en un plano

Reescribir: $f(t)=(t,\,1+\tfrac{1}{t},\,\tfrac{1}{t}-t)$.

Buscamos $A,B,C,D$ tal que $A t+B(1+1/t)+C(1/t-t)=D$ para todo $t\in{]}0,\infty[$.

Reagrupando: $(A-C)t + (B+C)(1/t) + B = D$.

Para que sea constante en $t$:

- $A-C=0 \Rightarrow A=C$
- $B+C=0 \Rightarrow B=-C$

Tomando $C=1$: $A=1$, $B=-1 \Rightarrow D=B=-1$.

$$\boxed{\text{Plano: } x-y+z=-1.}$$

*Verificación*: $f(1)=(1,2,0)$: $1-2+0=-1$ ✓. $f(2)=(2,\tfrac{3}{2},-\tfrac{3}{2})$: $2-\tfrac{3}{2}-\tfrac{3}{2}=-1$ ✓.

> Como la curva es plana, su **torsión es $0$** en todo punto.

---

## Ej 19 — $f(t)=(6\sin t,\,4\sin t,\,2\cos t)$ es plana

$$f(t)=\sin(t)\cdot(6,4,0)+\cos(t)\cdot(0,0,2).$$

Combinación lineal de dos vectores **fijos** con coeficientes $\sin$ y $\cos$ $\Rightarrow \operatorname{tra}(f)$ está en el plano generado por $(6,4,0)$ y $(0,0,2)$.

**Normal al plano**: $(6,4,0)\times(0,0,2)=(8,-12,0)\propto(2,-3,0)$.

$$\boxed{\text{Plano: } 2x-3y=0.}$$

**Verificación**: $2\cdot 6\sin t - 3\cdot 4\sin t = 0$ ✓.

> **Curva plana** $\Rightarrow$ **torsión $\equiv 0$**.

---

## Ej 20 — Christian Cueva, penal Rusia 2018

Proyección en plano $XY$: $y=x^2$. Proyección en plano $XZ$: $z=x^3$. Si $x(t)=t$ (parámetro natural):

$$\boxed{f(t)=(t,\,t^2,\,t^3) \text{ (cúbica alabeada / twisted cubic)}.}$$

**(b) Triedro de Frenet en $t=1$**

$$f'(t)=(1,\,2t,\,3t^2) \Rightarrow f'(1)=(1,2,3),\ \|f'(1)\|=\sqrt{14}.$$

$$f''(t)=(0,\,2,\,6t) \Rightarrow f''(1)=(0,2,6).$$

$$f'''(t)=(0,0,6).$$

$$f'\times f'' = (12-6,\,0-6,\,2-0) = (6,\,-6,\,2),\ \|\cdot\|=\sqrt{76}=2\sqrt{19}.$$

$$\boxed{T(1)=\frac{1}{\sqrt{14}}(1,2,3).}$$

$$\boxed{B(1)=\frac{1}{2\sqrt{19}}(6,-6,2)=\frac{1}{\sqrt{19}}(3,-3,1).}$$

$$N(1)=B\times T = \frac{1}{\sqrt{19}\sqrt{14}}(3,-3,1)\times(1,2,3)=\frac{1}{\sqrt{266}}(-11,-8,9).$$

*(Verificación: $\|(-11,-8,9)\|^2 = 121+64+81=266$ ✓.)*

$$\boxed{N(1)=\frac{1}{\sqrt{266}}(-11,-8,9).}$$

**(c) Torsión en $t=1$**

$$\langle f'\times f'',\,f'''\rangle = \langle (6,-6,2),\,(0,0,6)\rangle = 12.$$

$$\boxed{\tau(1)=\frac{12}{76}=\frac{3}{19}.}$$

---

## Notas para el examen

1. **Cheat-sheet mínimo para Frenet** (memorizar!):
   - $T=f'/\|f'\|$
   - $B=(f'\times f'')/\|f'\times f''\|$
   - $N=B\times T$
   - $\kappa=\|f'\times f''\|/\|f'\|^3$
   - $\tau=\langle f'\times f'',\,f'''\rangle/\|f'\times f''\|^2$

2. **Identidad clave**: si $v(t)=\|f'(t)\|$, entonces $f''=v'\,T + v^2\kappa\,N$ (componentes tangencial y normal).

3. **Curva plana $\Leftrightarrow \tau\equiv 0$**. Para demostrar que una curva es plana: expresar $f(t)$ como combinación lineal de vectores fijos $+$ punto base, o hallar $A\cdot f(t)=D$.

4. **En parametrización por arco** ($\|f'(s)\|=1$): $f''=\kappa\,N$, $\|f''\|=\kappa$, y $f''\perp f'$ siempre.

5. Cita siempre: *"por la fórmula $\kappa=\|f'\times f''\|/\|f'\|^3$"*, *"por ser $f'$ unitario, $\langle f',f''\rangle=0$"*, *"por el teorema de invariancia de la parametrización"*...

6. Para **integrales**: integra componente a componente. Condiciones iniciales fijan las constantes de integración.

7. Si la **parametrización por arco** queda con integral no invertible en forma cerrada (p.ej. elíptica), expresa la parametrización implícitamente y no pelees con álgebra imposible.
