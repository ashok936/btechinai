# #Differential Calculus

## #Average rate of change
It needs two points f(a) and f(a + x) that does not take limit. x is change in a. 
- it is denoted by $\frac{\Delta y}{\Delta x}$

## #Concept of Derivative

The Differential calculus(derivative) helps to find instantaneous(Exact) rate of change at a point.
- It is denoted by $\frac{dy}{dx}$

But you think, how is it possible to change at a point, change needs two points. 



You think right but In differential calculus, It uses concept of derivative $\frac{dy}{dx}$.

Example:-$$
\frac{d f(x)}{dx} = \lim_{h \to 0} \frac{f(x+h)-f(x)}{h}
$$

Where $h$ = small change in $x$
and $h$ is shrinking toward zero but never become zero ($h \neq 0$).

Suppose, $$
y=f(x) = x^2
$$

Here,
$f(x)$ depends on $x$ if we increase or decrease $x$ it directly affects to $y=f(x)$

If we want to calculate instantaneous rate of change $\frac{d f(x)}{dx}=\frac{dy}{dx}$

so,

$$
\frac{d f(x)}{dx}=\frac{d x^2}{dx}$$

Then, Increase slightly $h$ in $x$

$$
\frac{d x^2}{dx}=\lim_{h \to 0} \frac{(x + h)^2 - x^2}{h}
$$

$$
or, \frac{d x^2}{dx}=\lim_{h \to 0}\frac{x^2 + 2xh + h^2-x^2}{h}
$$

$$
or, \frac{d x^2}{dx}= \lim_{h \to 0}\frac{h(2x+h)}{h}
$$

$$
or, \frac{d x^2}{dx}=\lim_{h \to 0}(2x+h)
$$

now, Substitute h = 0

$$
Ans=\frac{d x^2}{dx}=2x
$$

## #Basic formulae of Derivative

### $1.\frac{dx^n}{dx}=nx^{n-1}\hspace{25mm}2.\frac{d \sqrt{x}}{dx}=\frac{1}{2}x^{\frac{1}{2}}$ 

### $3.\frac{de^{ax}}{dx}=ae^{ax}\hspace{27mm}4.\frac{de^x}{dx}=e^x$

### $5.\frac{da^x}{dx}=a^xlna\hspace{26mm}6.\frac{dlnx}{dx}=\frac{1}{x}$

### $7.\frac{dlog_a^x}{dx}=\frac{1}{xlna}\hspace{27mm}8.\frac{d[f(x)]^n}{dx}=n[f(x)]^{n-1}$

### $9.\frac{dsinx}{dx}={cosx}\hspace{25mm}10.\frac{dtanx}{dx}=sec^2x$

### $11.\frac{dsecx}{dx}=secx.tanx\hspace{15mm}12.\frac{dcosx}{dx}=-sinx$

### $13.\frac{dcotx}{dx}=-cosec^2x\hspace{16mm}14.\frac{dcosecx}{dx}=-cosecx.cotx$

### $15.\frac{dsin^{-1}x}{dx}=\frac{1}{\sqrt{1-x^2}}\hspace{19mm}16.\frac{dtan^{-1}x}{dx}=\frac{1}{1+x^2}$

### $17.\frac{dsec^{-1}x}{dx}=\frac{1}{x\sqrt{x^2-1}}\hspace{18mm}18.\frac{dcos^{-1}x}{dx}=-\frac{1}{\sqrt{1-x^2}}$

### $19.\frac{dcot^{-1}x}{dx}=-\frac{1}{1+x^2}\hspace{19mm}20.\frac{dcosec^{-1}x}{dx}=-\frac{1}{x\sqrt{x^2-1}}$

### $21.\frac{d(u.v)}{dx}=v.\frac{du}{dx}+u.\frac{dv}{dx}\hspace{13mm}22.\frac{d(\frac{u}{v})}{dx}=\frac{v.\frac{du}{dx}-u\frac{dv}{dx}}{v^2}$

### $23.\frac{dc}{dx}=0\hspace{32mm}24.\frac{dcf(x)}{dx}=c.\frac{df(x)}{dx}$

### $25.ln(a*b)=lna+lnb\hspace{11mm}26.ln(\frac{a}{b})=lna-lnb$

### $27.log_b^a=\frac{lna}{lnb}$