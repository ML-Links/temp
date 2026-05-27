### Other Critical Cases. Mathematical Excursion.

§ 521. There is a second critical case in which, without leakage, the formulae for the potential and current reduce to simple form when a condenser and resistance are put in terminally. Say

$$
r=Lv,\qquad 1=2rs\sigma;\qquad \text{then}\qquad m=-1,\quad n=0.
$$

Equations (38) and (44) reduce to

$$
\frac{C}{e}=\frac{e^{-\sigma t}}{2r}(1-a)=\frac{e^{-\sigma t}}{2r}(I_0-I_1)(\sigma t), \tag{60}
$$

$$
\frac{V}{e}=\tfrac12 e^{-\sigma t}(1+a)=\tfrac12 e^{-\sigma t}(I_0+I_1)(\sigma t). \tag{61}
$$

The value of the terminal condensance is one half the value in the first critical case. Being in the practical region, the present case makes a substantial addition to the simply calculable cases possible without employing an infinite series of $I_n$ functions.

If the resistance $r$ is next the cable, and $e$ is on the other side of the condenser, without extra resistance, the potential $V_1$ at the junction of the resistance and condenser is

$$
V_1=V+rC=e\,e^{-\sigma t}I_0(\sigma t), \tag{62}
$$

by the above. Compare with (48). The curve of $V_1$ in this second critical case is the same as the curve of $C$ in the standard case of terminal short-circuit. If, however, $e$ is directly associated with $r$, there is the usual modification of potential distribution, whereas $C$ is the same through the resistance and condenser whichever way they are put, and wherever $e$ is put.

If $r=Lv$, and $s=\infty$, we have a third critical case,

$$
\frac{C}{e}=\frac{e^{-\sigma t}}{2r}(I_0+I_1). \tag{63}
$$

As the condenser is cut out, this curve is of a quite different nature. In fact the curve of $C$ is the same as that of $V$ in the second critical case. The curve of $V$, however, requires an infinite series.

A fourth critical case is worth noticing, though it does not reduce to finite forms. It is that of equal roots of the $a$ equation. Let

$$
m^2+4n=0,\qquad \text{then}\qquad a_1=a_2=2m^{-1}.
$$

We may eliminate $n$, and reduce (38) to

$$
\frac{C}{e}=\frac{e^{-\sigma t}}{r+Lv}\frac{1-a^2}{(1-\tfrac12 ma)^2}=\cdots=(1-a^2)\{1+2(\tfrac12 ma)+3(\tfrac12 ma)^2+\ldots\}. \tag{64}
$$

There do not seem to be any more finite reductions than those described.

Although the method of treating the $a$ fraction similar to (11) ultimately only leads to the result (40), there are some views by the way worth looking at. We have

$$
\frac{1-a^2}{1-ma-na^2}=\frac{1-a^2}{a_2-a_1}\left(\frac{a_2}{1-a/a_2}-\frac{a_1}{1-a/a_1}\right), \tag{65}
$$

where

$$
a_1\;\text{or}\;a_2=-\frac{m}{2n}\pm\sqrt{\frac{m^2}{4n^2}+\frac1n}, \tag{66}
$$

and the question is what electrical problems the two simpler ones represent. We have to find the meaning of

$$
\frac{1}{1-ca}=I_0+cI_1+c^2I_2+c^3I_3+\ldots, \tag{67}
$$

where $c$ is a constant, and of the same multiplied by $1-a^2$. Take (67) first.

Let

$$
Z=\left(\frac{R+Lp}{Sp}\right)^{\tfrac12},\qquad \text{then}\qquad Z^2=L^2v^2\left(1+\frac{2\sigma}{p}\right). \tag{68}
$$

That is, the square of the resistance operator of the cable is the product of the resistance $Lv$, and of $(r+sp)^{-1}$, where $r$ and $s$ have the special values $Lv$ and $(2Lv\sigma)^{-1}$. This is what takes place in the second critical case above described. But in the more general case, we can put $a$ in terms of $p$ by means of

$$
p=\tfrac12\sigma(a+a^{-1}),\qquad \text{or}\qquad a=\frac{\left(\frac{p+\sigma}{p-\sigma}\right)^{\tfrac12}-1}{\left(\frac{p+\sigma}{p-\sigma}\right)^{\tfrac12}+1}. \tag{69}
$$

It follows that

$$
e^{-\sigma t}\frac{1}{1-ca}=\frac{Lv+Z}{1+c}\,\frac1{Z+Z^2\frac{1-c}{Lv(1+c)}}, \tag{70}
$$

To verify this, it may be done the other way. Given the right side, solve it in terms of $I_n$ functions with the exponential factor in the way (38) was obtained. The result is the left side. As regards the meaning, the denominator signifies a cable, resistance and condensance in sequence, with special values of $r$ and $s$, which are positive when $c<1$. The numerator is a constant times the sum of the resistance operator of the cable and of a resistance $Lv$. So the left side of (70) is the sum of two solutions, viz., the potential at the cable terminal due to a steady $e$ of a certain value, and of the current into the cable multiplied by a certain resistance, not the same as $r$. If $c>1$, this problem is electrically impossible, owing to the negativity of $r$ and $s$.

If we turn $c$ to its reciprocal, we obtain

$$
e^{-\sigma t}\frac1{1-c^{-1}a}=\frac{Lv+Z}{1+c^{-1}}\,\frac1{Z-Z^2\frac{1-c}{Lv(1+c)}}, \tag{71}
$$

which is electrically possible when $c>1$.

By uniting (70) and (71) we get

$$
e^{-\sigma t}\left(\frac1{1-ca}+\frac1{1-c^{-1}a}-1\right)=e^{-\sigma t}(I_0+(c+c^{-1})I_1+(c^2+c^{-2})I_2+\ldots), \tag{72}
$$

on the left side; and

$$
\frac{Lv+Z}{1+c}\frac1{Z+Z^2\frac{1-c}{Lv(1+c)}}+\frac{cLv+Z}{1+c}\frac1{Z-Z^2\frac{1-c}{Lv(1+c)}}-\frac{Lv}{Z}, \tag{73}
$$

on the right side. Here note that the $1$ in the $a$ function always means $a^0$, so that $e^{-\sigma t}a^0=Lv/Z$. This expression (73) reduces to

$$
\frac{1-x^2}{1-x^2\left(1+\frac{2\sigma}{p}\right)},\qquad \text{if}\quad x=\frac{1-c}{1+c}. \tag{74}
$$

This can be algebrised at sight, and makes

$$
\frac{\sigma t(1-c)^2}{x\epsilon}=e^{-\sigma t}\times e^{\frac{\sigma t}{x}(\frac{c+1}{c})}. \tag{75}
$$

Comparing with (72), we corroborate a well-known besselian formula.

We can also exhibit it as the difference of two cable problems without condensers, but with resistances only. For the left side of (74) is the same as

$$
\frac{Lv(1-x^2)}{2x}\left\{\frac1{Z+Lv/x}-\frac1{Z-Lv/x}\right\}, \tag{78}
$$

which expresses the difference of the current from a special $e$ into a cable through the resistances $Lv/x$ and $-Lv/x$; one of which, unfortunately, is negative. But that is of no consequence in the momentary application, which is to elucidate the treatment of operators in the solution of differential equations, rational or fractional. This matter has a great future, not merely in electromagnetics, but in all mechanical applications, as academical mathematicians will find out in time, if they live long enough.

In a similar way, it may be shown that

$$
e^{-\sigma t}\frac{1-a^2}{1-ca}=\frac{2Lv}{Z+Lv+\frac{(1-c)Rv}{2p}}, \tag{79}
$$

so the problem represented is that of a cable with terminal resistance and condensance, the first of which has the critical value, but the second neither of the critical values, and moreover $c<1$ for electrical reality. Applying this to (65) above, we get

$$
\frac{C}{e}=\frac{2Lv}{r+Lv}\frac{a_2}{a_2-a_1}\frac1{Lv+Z+\frac{a_1-1}{2a_1}\frac{Rv}{p}}-\frac{2Lv}{r+Lv}\frac{a_1}{a_2-a_1}\frac1{Lv+Z+\frac{a_2-1}{2a_2}\frac{Rv}{p}}. \tag{80}
$$

This exhibits $C$ in the case of any values of $r$ and $s$ in terms of two $C$'s, both with the critical $r=Lv$, but with different $s$'s, which need not be real, however. The impressed forces are also different. I hoped this method might be as illuminating as in the corresponding case when $L=0$, but it is not.

As another example, examine the meaning of

$$
\frac{C}{e}=\frac1{Z+cZ^2},\qquad \text{where}\quad Z=\left(\frac{R+Lp}{K+Sp}\right)^{\tfrac12}. \tag{81}
$$

Here clearly $c$ is a conductance. Put in terms of $\rho$ and $\sigma$, equation (53). Then

$$
\frac{C}{e}=\frac1{Lv\left(\frac{p+\rho+\sigma}{p+\rho-\sigma}\right)^{\tfrac12}+cL^2v^2\left(1+\frac{2\sigma}{p+\rho-\sigma}\right)}. \tag{82}
$$

We therefore have

$$
r=cLv^2,\qquad k+sp=\frac{\rho-\sigma}{2cL^2v^2}\left(1+\frac{p}{p-\sigma}\right). \tag{83}
$$

These show the value of the terminal resistance $r$, and also that the condenser is shunted, or has the conductance $k$; and shows the values of $k$ and $s$.

To develop in terms of $a$, change $p$ to $p-\rho$, at the same time putting on the prefactor $e^{-\rho t}$ and the postfactor $ep\rho t$ or $p/(p-\rho)$; then finally put $\tfrac12\sigma(a+a^{-1})$ for $p$, and put on the postfactor $(1-a^2)/(1+a^2)$, which is the besselian development of unity. The result is

$$
\frac{C}{e}=e^{-\rho t}\frac{(1-a^2)(1-a)^2}{(1+a^2-2\rho\sigma^{-1}a)-Lva\{(1-a^2)+cLv(1+a)^2\}}; \tag{84}
$$

Finally, this may be expanded by division. If $cLv=1$, it simplifies, viz.:--

$$
\frac{C}{e}=e^{-\rho t}\frac{(1-a)^3}{2Lv(1+a^2-2\rho\sigma^{-1})}. \tag{85}
$$

To destroy the leakage $\rho=\sigma$. We then reduce to the case of equation (61) above.

### The Curbing Effect of an Inductance Shunt.

§ 522. That an inductance will curb signals when used as a shunt to the receiving instrument, instead of a condenser in series, is obvious enough. But the inductance and the condenser curves of current in the receiver cannot be quite similar; and it is not easy to say, given an unlimited power of varying the size of the condenser and of the induction coil, which method would be preferable on the whole. I have been informed by Mr. W. Gaye, that in certain cases the inductance shunt has been found to be 12 to 14 per cent. better than the condenser, owing to the better definition of successive dots on the same side. But the working speed is the resultant of so many factors that this estimate should not be extended too far beyond present experience.

We may get some theoretical guidance by comparing the curves of current in the two cases of condenser and inductance under the same circumstances as regards impressed voltage. The condenser with resistance in series has been done. Now do the coil theory.

Let the impressed force $e$ act in the resistance $r$, joined to the beginning of an infinitely long cable, with an inductance coil as shunt. The inductance should be very large, and the resistance of the coil small. The initial current is $e/r$, just as when a condenser is used in series with $r$, instead of the shunt coil. The final current is $e/(r+R_0)$ in the battery and the coil, but zero in the cable. This is again like the action of a condenser, as regards the cable current, though not otherwise. But the course of the current in the cable is not the same in the two cases.

The current in $r$ at any moment is

$$
C_r=\frac{e}{r+ZZ_0/(Z+Z_0)},\qquad Z=\left(\frac{R}{Sp}\right)^{\tfrac12},\qquad Z_0=R_0+L_0p; \tag{1}
$$

and the current entering the cable is

$$
C=C_r\frac{Z_0}{Z_1}=\frac{e}{r+rZ/Z_0}, \tag{2}
$$

by the usual formulae for conductors, but using the resistance operators instead of the resistances.

We must now algebrize this formula. Take $Z_0=L_0p$. The resistance $R_0$ is not material. Then

$$
C=\frac{e}{r\left\{1+\frac{a}{p^{1/2}}\left(1+\frac{b}{p}\right)\right\}},\qquad a=\frac1r\left(\frac RS\right)^{\tfrac12},\qquad b=\frac r{L_0}. \tag{3}
$$

It can be seen at sight that long division will give a convergent solution, which is therefore the solution, and two others of mixed character. Thus, the convergent solution is

$$
C=\frac er\left\{1-\frac a{p^{1/2}}\left(1+\frac bp\right)+\frac{a^2}{p}\left(1+\frac bp\right)^2-\frac{a^3}{p^{3/2}}\left(1+\frac bp\right)^3+\ldots\right\}, \tag{4}
$$

which is to be algebrized by turning $p^{-n}$ to $t^n/n$. Since this solution is in sets of terms alternately $+$ and $-$, this may be the best arrangement for calculation, as it stands. The range of utility with moderate work must be found out. Since $b=r/L_0$, the larger $L_0$ is the easier the work.

The solution may also be regarded as the difference of two power integral powers only, the other fractional only. Thus,

$$
C=\frac er\left\{1+\frac{a^2}{p}\left(1+\frac bp\right)^2+\frac{a^4}{p^2}\left(1+\frac bp\right)^4+\ldots\right\}
$$

$$
-\frac er\left\{\frac a{p^{1/2}}\left(1+\frac bp\right)+\frac{a^3}{p^{3/2}}\left(1+\frac bp\right)^3+\ldots\right\}, \tag{5}
$$

and it is easy, in (4) and (5), to collect the coefficients so as to have any power of $b$ isolated.

The corresponding condenser formula is

$$
C=\frac{e}{r+\frac1{sp}+Z}=\frac e{r\left\{1+\frac a{p^{1/2}}\left(1+\frac c{p^{1/2}}\right)\right\}}, \tag{6}
$$

where $a$ is as before, whilst $c$ is a fresh constant. That is, $c/p$ in the condenser case becomes $b/p^{1/2}$ in the coil case. This suggests more effective curbing, but regular calculation is required to show it.

Since the denominator in (3) is a cubic in $p^{1/2}$, the divergent solution requires special treatment to harmonize with the convergent. This is reserved.

If we shift to the other side of the junction, so as to be in the cable itself, $C$ then represents the current in $r$. That is to say, $C$ is current in the receiver at the end of a very long cable due to a quite special sort of signal, and curbed by the inductance shunt. This may be compared with the corresponding received current with a condenser inserted instead. So that the difference in the curbing action as calculated at the sending end serves to illustrate the same at the receiving end. The actual formula for a practical received signal which has traversed the cable is of course very complicated.

If the inductance shunt is better than the condenser in receiving, it may be expected to be better for sending as well. The proper way is to try it thoroughly. Perhaps earth currents may be detrimental.

### The Transverse Momentum of an Electron.

*[Nature, Aug. 31, 1905, p. 429.]*

§ 523. When Newton's Third Law is applied to an electron it makes

$$
F=\dot M+\dot N, \tag{1}
$$

where $M$ is the "momentum" in the field, or that part of the time integral of the force on the ether which is in the field, or $\Sigma\mathrm{VDB}$, and $N$ is the momentum already wasted, whilst $F$ is the applied force on the electron.

Similarly, Newton's Fourth Law (or the Scholium to the Third) makes

$$
Fu=\dot U+\dot T+W, \tag{2}
$$

if $u$ is the velocity of the electron, $U$ the electric and $T$ the magnetic field energy, and $W$ the rate of waste of energy.

Now, both $W$ and $N$ are known in terms of the velocity and acceleration of the charge at any moment by formulae I gave in *Nature*, Nov. 6, 13, 1902. But when applied to (1), (2), these equations do not let us determine $M$ generally in terms of the velocity and acceleration, on account of the variability of the state of the field, and of the waste of energy and momentum. $M$ is indefinite. But in long-continued forced circular motion of a charge, $\dot U+\dot T=0$. So [p. 163, eq. (18)]

$$
Fu=W=\frac{\mu Q^2A^2}{6\pi v\kappa^5}, \tag{3}
$$

(*loc. cit.*), where $Q$ is the charge, and $A$ the acceleration (or $u^2/R$, if $R$ is the radius of the orbit). Also, $\kappa^2=1-u^2/v^2$. The direct or $u$ component of $F$ is therefore known. We also have (*loc. cit.* [p. 163, eq. (19)],)

$$
\dot N=\frac{u}{v^2}W. \tag{4}
$$

Using these in (1), along with (3), we come to

$$
\kappa^2F_1=\dot M_2,\qquad F_2=\dot M_1, \tag{5}
$$

where $F_1$ is the $u$ component, and $F_2$ the transverse component, towards the centre.

Thus only the part $\kappa^2F_1$ of the direct force is associated with the transverse or centripetal force $F_2$ in keeping up the revolving state; the rest of $F_1$, that is, $(u^2/v^2)F_1$, being the wasted part as regards momentum, although the whole of $F_1$ is concerned in the waste of energy.

Now, $\dot M=VnM$, if $n$ is the angular velocity. That is,

$$
\dot M=\dot M_1u_1+M_1\dot u_1+\dot M_2A_1+M_2\dot A_1, \tag{6}
$$

if $u_1$ and $A_1$ are unit vectors, making

$$
\dot u_1=(u/R)A_1,\qquad \dot A_1=-(u/R)u_1. \tag{7}
$$

Also, $\dot M_1=0$, $\dot M_2=0$, because the motion is steady. So we convert (5) to

$$
\kappa^2F_1=\dot M_2=-M_2(u/R)u_1,\qquad F_2=\dot M_1=M_1(u/R)A_1. \tag{8}
$$

Finally, although we get no formula for $M_1$, we do obtain a complete formula for $M_2$, viz.,

$$
M_2=-\frac{\mu Q^2A}{6\pi v\kappa^3}. \tag{9}
$$

This is the transverse momentum of $Q$ in steady circular motion, without any limitations upon the size of the velocity and acceleration, save the usual ones, $u<v$, and $A$ not excessively great in regard to the diameter of the electron.

It would seem that an integration over the whole field, in which $E$ and $H$ are known (*loc. cit.*) [p. 162], is required to find $M_1$, the direct momentum. If, however, the acceleration is infinitesimal, the known formula for $M_1$ in steady rectilinear motion may be employed, viz., $\tfrac12 M_1u=T$.

Finally, I have pleasure in saying that Mr. G. F. C. Searle, F.R.S., led me to see that my waste formula led to the formula (9) for the transverse momentum, by submitting to me a calculation of $M_2$ in the special case of infinitesimal acceleration and velocity. He made no use of the waste formula, not being aware of it, but since in the circumstances the waste is infinitesimal, it did not matter. In fact, $\tfrac12 M_1u=T$ leads to the reduced special value of the transverse momentum when $u$ and $A$ are infinitesimal. The argument was somewhat obscure by the want of comprehensiveness, but the result agrees with (9).

### Extension to Helical Motion.

§ 524. To pass from a circular to a right helical path, we have merely to add to the circular velocity $u$ a constant rectilinear velocity $w$ perpendicular to the circle. Since the acceleration is unaltered and the waste of energy goes on uniformly, it may be inferred that the formula for the transverse momentum is the same, with allowance made for the changed velocity. But there are some changes otherwise. Thus, let $q=u+w$ be the actual velocity, then $\kappa^2=1-q^2/v^2$ now, and

$$
W=\frac{\mu Q^2A^2}{6\pi v\kappa^4},\qquad \dot N=\frac{q}{v^2}W, \tag{10}
$$

represent the rate of waste of energy and momentum. Here $A=u^2/R$, as before, but now $\dot N$ has an axial component.

Let $M=M_1+M_2+M_3$, where $M_1$ is the circular component, $M_2$ the radial component inward, and $M_3$ the axial component. We have $M_3=\text{constant}$, because its direction is constant, and the symmetry makes its size constant. So the equation

$$
F=\dot M+\dot N
$$

splits up into

$$
F_1=\dot M_2+(u/v^2)W=-M_2(u/R)u_1+(u/v^2)W, \tag{11}
$$

$$
F_2=\dot M_1=M_1(u/R)A_1,\qquad F_3=(w/v^2)W. \tag{12}
$$

Also, the activity equation becomes, by (11) and (12),

$$
W=Fq=F_1u+F_3w=-M_2A+(q^2/v^2)W, \tag{13}
$$

from which

$$
\kappa^2W=-M_2A, \tag{14}
$$

so that $M_2$, $F_1$ and $F_3$ are all known in terms of $W$; thus,

$$
M_2=-\frac{\kappa^2}{A}W,\qquad F_3=\frac{w}{v^2}W,\qquad F_1=\frac{W}{u}\left(1-\frac{w^2}{v^2}\right) \tag{15}
$$

where $W$ is given in (10). But $F_2$, $M_1$, and $M_3$ require further work.

The transverse momentum is increased by the axial motion added to the circular (supposed unchanged) by reason of the changed value of the velocity and therefore of $\kappa^2$. It may be largely multiplied in this way. $F_1$ is also increased. The new force $F_3$ also mounts up with $w$. It would be zero, if the motion were strictly rectilinear at constant speed.

But if it is the actual speed $q$ in the helical path that is kept constant, then $M_2$ and $F_1$ fall off as $w$ increases, whilst $F_3$ first increases and then falls off.

### Deep Water Waves.

§ 525. This subject turned up in §520 very strangely in the theory of a condenser and resistance placed in series with a cable. But some time before that, in Lord Kelvin's "Baltimore Lectures," my attention was directed to the water waves by the remark that a certain definite integral was "irreducible." This meant, I supposed, that it had not been algebrised. Whether so or not, I found that it was readily algebrisable operationally to a convergent series, which also showed the necessity of a second form, divergent, for purposes of calculation. I make no pretence of writing about deep water waves of various types from the practical point of view. What follows is to illustrate operational methods.

Let

$$
D=\frac{D_0}{\pi}\int_0^\infty \cos qx\cos qvt\,dq, \tag{1}
$$

What does $D$ mean? Put $t=0$. Then $D=0$ everywhere save at $x=0$, where $\int D\,dx=D_0$. That is, $D$ at time $t$ results from the amount of $D$ represented by $D_0$ condensed at the origin initially, and made to spread right and left in a manner controlled by the partial characteristic of $D$, modified also by the similar spreading of the initial states of $\dot D$, $\ddot D$, &c., so far as they are concerned.

Say $v=aq^n$, or $v\propto \lambda^{-n}$, if $\lambda$ is the wave length in a train. Then $D$ is equivalently expressed by

$$
D=\frac{D_0}{\pi}\int_0^\infty \frac{\cos qx\,dq}{1+a^2q^{2n+2}/p^2}=\frac{D_0}{\pi}\int_0^\infty \frac{\cos atq^{-n-1}\,dq}{1+q^2/a^2}, \tag{2}
$$

or by

$$
D=\frac{D_0}{\pi}\int_0^\infty \frac{dq}{(1+q^2/\Delta^2)(1+a^2q^{2n+2}/p^2)}. \tag{3}
$$

If any of these forms be integrated, the result is to express $D$ in terms of $D_0$ operationally, with one differentiator concerned in the case of either of (2) and with two differentiators in the case of (3). This may perhaps be done for any value of $n$, though certainly it will be complicated. For special values of $n$, it can easily be done.

If $n=0$, $v$ is constant. This is an easy case. If $n=1$, $v=aq$. This occurs in the theory of lateral vibrations of an elastic rod. If $n=-1$, $v\propto \lambda$, so it is a singular case of stationary vibrations.

If $n=-\tfrac12$, we come to the deep water surface wave theory. Then, selecting the form (3), we have

$$
D=\frac{D_0}{\pi}\int_0^\infty \frac{dq}{(1+q^2/\Delta^2)(1+a^2q/p^2)}. \tag{4}
$$

The indefinite integral is known, thus

$$
\frac{D}{D_0}=\frac1\pi\frac{\Delta^2p^2/a^2}{\Delta^2+p^4/a^4}\left[\log\frac{q+p^2/a^2}{\sqrt{q^2+p^4/a^4}}+\frac{p^2}{a^2\Delta}\tan^{-1}\frac q\Delta\right]_0^\infty. \tag{5}
$$

So, finally,

$$
\frac{D}{D_0}=\frac1\pi\frac{\Delta^2p^2/a^2}{\Delta^2+p^4/a^4}\left\{\frac{p^2}{a^2\Delta}\frac\pi2-\log\frac{p^2}{a^2\Delta}\right\}. \tag{6}
$$

This being an operational solution, can be algebrised in the usual way.

The rational part of (6) makes

$$
\tfrac12\frac{p^2}{a^2}\sin\frac{p^2x}{a^2},\qquad \text{by}\; \Delta\; \text{first}, \tag{7}
$$

or,

$$
\tfrac12\Delta\left(1-a^4\Delta^2\frac{t^4}{[4]}+a^8\Delta^4\frac{t^8}{[8]}-\ldots\right),\qquad \text{by}\; p\; \text{first}. \tag{8}
$$

Next do the logarithmic part of (6). With $\Delta$ first we get

$$
-\frac1\pi\frac{d}{dn_0}\frac{(p^2/a^2)^n(p^2/a^2\Delta)^n}{1+p^4/a^4\Delta^2}, \tag{9}
$$

where $n_0$ means that we put $n=0$ after differentiation to $n$. Or,

$$
-\frac1\pi\frac{d}{dn_0}\left\{\frac{x^n(at)^{-(2n+2)}}{[n]-(2n+2)}+\frac{x^{n+2}}{n+2}\frac{(at)^{-(2n+6)}}{[2n+6]}+\ldots\right\}
$$

$$
=\frac2{\pi}\left[(at)^{-2}g'(-2)-\frac{x^2}{[2]}(at)^{-6}g'(-6)+\ldots\right]
$$

$$
=-\frac{2}{\pi a^2t^2}\left\{1-\frac52\frac{x^2}{[2a^4t^4]}+\frac94\left(\frac{x^2}{a^4t^4}\right)^2-\ldots\right\}. \tag{10}
$$

But if we do $p$ first in the logarithmic part of (6), we get

$$
-\frac1\pi\frac{d}{dn_0}\frac{(p^2/a^2)^n-\Delta^{-(n-2)}}{1+a^4\Delta^2/p^4}, \tag{11}
$$

$$
=-\frac1\pi\frac{d}{dn_0}\left\{\frac{x^{n-2}}{n-2}-\frac{(at)^{(2n-2)}}{(2n-2)}-\frac{x^{n-4}}{n-4}-\frac{(at)^{(2n-6)}}{(2n-6)}+\ldots\right\}
$$

$$
=\frac1\pi\left(\frac{at}{x}\right)^2\left\{\frac12-\frac36\frac{a^4t^4}{x^4}+\frac5{10}\frac{a^8t^8}{x^8}-\ldots\right\}. \tag{12}
$$

The sum of (12) and (8) is one form of solution, the sum of (10) and (7) is another. But (12) is convergent and (10) divergent. Now it is a result of experience that when an algebrisation comes out in the form of a convergent series like (12) coupled with an operational series in integral positive powers of the differentiator, like (8), then the latter part means zero, just as any one would suppose, in fact. Therefore,

$$
\frac{D}{D_0}=\frac1\pi\left(\frac{at}{x}\right)^2\left\{\frac12-\frac36\frac{a^4t^4}{x^4}+\frac5{10}\frac{a^8t^8}{x^8}-\ldots\right\}. \tag{13}
$$

is the convergent solution of our problem. But it is equally a result of experience that when we come to a divergent series like (10) coupled with an operational series like (7), which would seem to mean zero, then it may do so, or it may not. That is, the divergent equivalent of (13) is

$$
\frac{D}{D_0}=\frac{D_1}{D_0}-\frac{2}{\pi a^2t^2}\left\{1-\frac52\frac{x^2}{[2a^4t^4]}+\frac94\frac{x^4}{[4a^8t^8]}-\ldots\right\}, \tag{14}
$$

where $D_1$ is an auxiliary function to be found from (7), or by other means.

Deferring this work, numerical examination of (13) shows it to be oscillatory, but only the extreme outer part, as said before, can be conveniently calculated. Give a constant value to $t$, and then vary $x$ from $\infty$ downwards. $D$ mounts up from zero at $\infty$ to the top of a hump at a finite distance and then falls to zero. Going nearer the origin, there is a negative hump, or a hollow, now of finite length, of course, and, moreover, its maximum is greater than that of the outermost hump. This is quite sufficient, along with experience of this kind of formula, to let one see that between the outermost hump and the origin is an infinite series of humps and hollows with amplitudes increasing and lengths decreasing towards the origin. But we also see the necessity of finding $D_1$ in (14), to enable the waves to be numerically estimated.

Without that, (13) shows that if $y=a^4t^4/x^2$, for any constant value of $y$, $x$ varies as $t^2$ and $D$ varies as $t^{-2}$. Also $x$ varies as $t$, so the velocity of a particular phase, as a node, varies as $t$. The distance between two nodes varies as $t$.

The following is one way of finding $D_1$. Put $q=a^2t^2/4x$ in (13), and $\Delta=d/dq$; then

$$
\frac{D}{D_0}=\frac{4q^{1/2}}{\pi^4a^2t^2}\left(q^{1/2}+\frac{q^{5/2}}{[2\tfrac12]}+\frac{q^{9/2}}{[4\tfrac12]}+\ldots\right) \tag{15}
$$

$$
=\frac{4q^{1/2}}{\pi^4(at)^2}\times\Delta^{-1/2}\cos q. \tag{16}
$$

In this form we see that the transformation from (13) to (14) depends upon the generalised cosine function. Thus, let

$$
\Cos q=\cdots+\frac{q^{-4}}{[-4]}-\frac{q^{-2}}{[-2]}+1-\frac{q^2}{[2]}+\frac{q^4}{[4]}-\cdots, \tag{17}
$$

then $\Cos q$ is numerically the same as $\cos q$. But it does not behave the same when differentiated, for

$$
\Delta^{-r}\Cos q=\cdots+\frac{q^{r-4}}{[r-4]}-\frac{q^{r-2}}{[r-2]}+\frac{q^r}{[r]}-\frac{q^{r+2}}{[r+2]}+\frac{q^{r+4}}{[r+4]}\cdots. \tag{18}
$$

Now $\Delta\cos q=\cos(q+\tfrac12\pi r)$, so the effect of $\Delta^{-r}$ is to add $-\tfrac12\pi r$ to the argument. This makes

$$
\Delta^{-r}\Cos q=\cos\left(q-\tfrac12\pi r\right)=\cdots+\frac{q^{r-2}}{[r-2]}+\frac{q^r}{[r]}-\frac{q^{r+2}}{[r+2]}\cdots, \tag{19}
$$

$$
\Delta^{-r}\Sin q=\sin\left(q-\tfrac12\pi r\right)=\cdots-\frac{q^{r-1}}{[r-1]}+\frac{q^{r+1}}{[r+1]}-\frac{q^{r+3}}{[r+3]}\cdots. \tag{20}
$$

The above is something like the way of constructing an integral for $x^n/[n]$, in vol. 2, p. 435. Or thus (if $\Delta=d/dx$), by the above,

$$
\Delta^{-n}\cos mx=m^{-n}\cos\left(mx-\tfrac12 n\pi\right);
$$

so

$$
\Delta^{-n}\frac1\pi\int_0^\infty \cos mx\,dm=\frac1\pi\int_0^\infty \frac{\cos(mx-\tfrac12 n\pi)}{m^n}\,dm.
$$

This is $\Delta^{-n}\Delta 1$, and

$$
\frac{x^n}{[n]}=\Delta^{-n}1=\frac1\pi\int_0^\infty \frac{\sin(mx-\tfrac12 n\pi)}{m^{n+1}}\,dm. \tag{21}
$$

Finally, we should show the connection with the generalised exponential function. Say

$$
e^x=\cdots+\frac{x^{r-1}}{[r-1]}+\frac{x^r}{[r]}+\frac{x^{r+1}}{[r+1]}+\cdots. \tag{22}
$$

Put $x=yi$. Then we get

$$
\cos y+i\sin y=\left[\left(\cdots+\frac{y^r}{[r]}-\frac{y^{r+2}}{[r+2]}+\cdots\right)-i\left(\cdots+\frac{y^{r-1}}{[r-1]}-\frac{y^{r+1}}{[r+1]}+\cdots\right)\right]i^r. \tag{23}
$$

Next, use $i^r=(\cos+i\sin)\tfrac12 r\pi$, and assume that $y$ is real positive. Then we may separate the real and imaginary parts of (23), and obtain

$$
\cos y=\left(\cdots+\frac{y^r}{[r]}-\frac{y^{r+2}}{[r+2]}+\cdots\right)\cos\tfrac12 r\pi+\left(\cdots+\frac{y^{r-1}}{[r-1]}-\frac{y^{r+1}}{[r+1]}+\cdots\right)\sin\tfrac12 r\pi, \tag{24}
$$

and a similar equation. Both these results involve (19) and (20).

It is to be noted that (22) is numerically true when $x$ is real positive, and that (19), (20) are numerically true when $q$ is real positive. As a test, consider the case $r=\tfrac12$, making

$$
\cos\left(q-\tfrac14\pi\right)=\cdots+\frac{q^{1/2}}{[\tfrac12]}-\frac{q^{5/2}}{[2\tfrac12]}+\frac{q^{9/2}}{[4\tfrac12]}-\cdots. \tag{25}
$$

I have worked out the long sum for the value $(2q)^{1/2}=100$, and obtain the value $-.478$, whilst the tables to make the left side come to $-.477$. Also for the value $(2q)^{1/2}=50$. The series makes $-.917$, whilst the tables make $-.92$. These tests are good, and the errors are well within the admissible errors conditioned by the finite size of the last convergent term in the divergent series.

Now use (25) in (15). We see that thus

$$
\frac{D}{D_0}=\frac{4q^{1/2}}{\pi^4a^2t^2}\left\{\cos\left(q-\tfrac14\pi\right)+\frac{q^{-3/2}}{[-3\tfrac12]}+\cdots\right\}; \tag{26}
$$

or in terms of $x$ and $t$,

$$
\frac{D}{D_0}=\frac{at}{2\sqrt\pi x^{3/2}}\left\{\cos\left(\frac{a^2t^2}{4x}-\frac\pi4\right)-\frac{2}{\pi a^2t^2}\left(1-\frac52\frac{x^2}{[2a^4t^4]}+\cdots\right)\right\}. \tag{27}
$$

Examine (27), to show the behaviour at the origin. By preliminary rough work, it is to be seen that $D$ falls to zero, and becomes negative; then rises again towards zero. The work soon becomes too long; so turn (27) to a divergent series. Thus, putting $z=a^2t^2/4t_1$, we get

$$
\frac{D}{D_0}=\frac{(z\pi)^{1/2}}{\pi t_1}\left(z^{-1/2}-\frac{z^{1/2}}{[\tfrac12]}+\frac{z^{3/2}}{[1\tfrac12]}-\cdots\right). \tag{28}
$$

This belongs to the type of the generalised $e^{-z}$ series, and is equivalent to

$$
\frac{D}{D_0}=\frac{(z\pi)^{1/2}}{\pi t_1}\left(z^{-1/2}-\frac{z^{-3/2}}{[-2\tfrac12]}+\frac{z^{-5/2}}{[-3\tfrac12]}-\cdots\right)
$$

$$
=-\frac1\pi\left(\frac{2}{a^2t^2}+\frac{4}{[2]}\frac{t_1}{a^4t^4}+\frac{6}{[3]}\frac{t_1^2}{a^6t^6}+\cdots\right). \tag{29}
$$

This shows return towards equilibrium without oscillation. As a specimen, put $t_1=1$ and $D_0/\pi=1$; then the initial value of $D$ is $1$, which falls to $\tfrac12$ at a little over $at=1$, passes $0$ a little before $at=2$, and approaches a negative value before rising again asymptotically to zero.

Now derive the value of $D$ at $x$. By the same process,

$$
\frac{D}{D_0}=\frac1\pi\int_0^\infty \frac{t_1\,dn}{t_1^2+x^2}\left\{1-\frac{a^2t^2x^2-t_1^2}{[2](\cdot)^2}+\frac{2a^4t^4t_1^3-3x^2t_1}{[4](\cdot)^3}+\cdots\right\}, \tag{30}
$$

where $(\cdot)$ means $(t_1^2+x^2)$, for brevity. If we use the divergent form to obtain $D$ at $x$ by the same process, it is clear that the arising solution cannot be complete, because the auxiliary function previously called $D_1$ makes no appearance. What we get is, calling this partial solution $D_2$,

$$
\frac{D_2}{D_0}=-\frac{2}{\pi a^2t^2}\left[1-\frac{5}{[2]}\frac{x^2}{a^4t^4}+\frac{9}{[4]}\frac{x^4}{a^8t^8}-\cdots+\frac{t_1}{a^2t^2}\left(3-\frac{14}{[2]}\frac{x^2}{a^4t^4}+\cdots\right)+\cdots\right]. \tag{31}
$$

Returning to (30), let $r=(x^2+t_1^2)^{1/2}$ and $t_1/r=\cos\phi$, $x/r=\sin\phi$. Then, by reference to a trigonometrical work for the expansion of $\cos n\phi$, it will be seen that (30) may be expressed as

$$
\frac{D}{D_0}=\frac1{\pi t_1}\left(\cos\phi-\frac{a^2t^2\cos2\phi}{[2]r}+\frac{2a^4t^4\cos3\phi}{[4]r^2}-\frac{3a^6t^6\cos4\phi}{[6]r^3}+\cdots\right). \tag{32}
$$

Now for any given values of $t_1$ and $x$, the cosine tables may be used to ease the full calculations. The explanation of this form is as follows. In the diagram let the straight line AA represent the undisturbed surface of the water, and the lines BB and CC represent undisturbed lower levels.

![Geometrical construction for the deep-water-wave hump across successive levels.](../media/ch10/fig-525-1.png)

The point $O$ is the origin, $P$ is a point in the water, $z$ its depth beneath the surface, and the rays from $O$ represent the planes along which the displacement is distributed. Then let the water everywhere be displaced along the radial lines leading to the origin $O$, the amount of this displacement at any point $P$ being $D_0/\pi r$, at distance $r$ from $O$. The total displacement through the semicircle through $P$ will be $D_0$. This is true at any distance. Moreover, the upward displacement at $P$ is $(D_0/\pi r)\cos\phi$ or $D_0z/(z^2+x^2)$, and by integration along the level through $P$, it will be seen that the total upward displacement through that level is $D_0$.

The shape of the hump representing the upward displacement at any level is exactly the one last considered, when $t$ represents $z$, the depth of the undisturbed level in question below the top level. Going to higher levels the hump condenses, and at the top level becomes infinitely condensed at the point $O$. We then have the original hump with which we started.

If, then, we take the level CC to be the undisturbed surface of the water, and its upward displacement to be the hump corresponding to the distance below AA, then we have not only solved the problem of the subsequent history of the hump upon the CC level, but by increasing the value of $z$ we have the form for all other levels beneath it; i.e., for the whole body of the water. The process may be continued upward, by having water above CC, and only when we reach the level AA, from which $z$ is measured, do we come to condensed waves. It is to be carefully noted that when the hump is not condensed, and yet belongs to the level of the water surface, then $z$ is not the distance below the level, but below an ideal level surface above the real one.

Knowing the vertical displacement upward, say $D_z$, or

$$
D_z=\frac{D_0}{\pi r}\left(\cos\phi-\frac{a^2t^2\cos2\phi}{[2]r}+\frac{2a^4t^4\cos3\phi}{[4]r^2}-\cdots\right), \tag{33}
$$

throughout the water, it is easy to deduce the horizontal displacement from the condition of incompressibility, $dD_x/dx+dD_z/dz=0$. It makes

$$
D_x=\frac{D_0}{\pi r}\left(\sin\phi-\frac{a^2t^2\sin2\phi}{[2]r}+\frac{2a^4t^4\sin3\phi}{[4]r^2}-\cdots\right). \tag{34}
$$

This is $D_x$ towards the origin, that is, to the left on the right side. Both may be included in one formula. Let $R=re^{i\phi}$. Then

$$
D_z-iD_x=\frac{D_0}{\pi R}\left(1-\frac{a^2t^2}{[2]R}+\frac{2a^4t^4}{[4]R^2}-\frac{3a^6t^6}{[6]R^3}+\cdots\right). \tag{35}
$$

From $D_x$ and $D_z$ the displacement potential may be worked out. But perhaps better more directly thus. Go back to the operational form. We have

$$
D_z=\{1-p_1a^2/p^2\}^{-1}\times \text{initial value of } D_z. \tag{36}
$$

This must apply equally to the potential of which $D_z$ is the derivative. Let the potential be $\Phi$. Its initial value is $(D_0/\pi)\log r$, as it is obvious on differentiation that it produces the assumed initial state of radial displacement. Therefore

$$
\Phi=\left\{1+\frac{a^2t^2}{[2]}p_1+\frac{a^4t^4}{[4]}p_1^2+\cdots\right\}\frac{D_0}{\pi}\log r, \tag{37}
$$

where $p_1=d/dz$. Carry this out. The result is, by the immediate use of $(-p_1)^n\log r=-[n-1]r^{-n}\cos n\phi$,

$$
\Phi=\frac{D_0}{\pi}\left(\log r+\frac{a^2t^2\cos\phi}{[2]r}-\frac{a^4t^4\cos2\phi}{[4]r^2}+\frac{2a^6t^6\cos3\phi}{[6]r^3}-\cdots\right). \tag{38}
$$

and from this the above $D_x$ and $D_z$ may be derived. Also the radial and tangential components $D_r$ and $D_\phi$. Thus,

$$
D_r=\frac{D_0}{\pi r}\left(1-\frac{a^2t^2\cos\phi}{[2]r}+\frac{2a^4t^4\cos2\phi}{[4]r^2}-\frac{3a^6t^6\cos3\phi}{[6]r^3}+\cdots\right), \tag{39}
$$

$$
D_\phi=\frac{D_0}{\pi r}\left(\frac{a^2t^2\sin\phi}{[2]r}-\frac{2a^4t^4\sin2\phi}{[4]r^2}+\frac{3a^6t^6\sin3\phi}{[6]r^3}-\cdots\right). \tag{40}
$$

where $D_r$ and $D_\phi$ are reckoned in the directions of decrease of $r$ and of $\phi$. On this understanding,

$$
D_r-iD_\phi=\frac{D_0}{\pi r}\left(1-\frac{a^2t^2}{[2]R}+\frac{2a^4t^4}{[4]R^2}-\frac{3a^6t^6}{[6]R^3}-\cdots\right). \tag{41}
$$

Here, if we put $c=a^2t^2/4R$, the last equation becomes a part of the generalised $e^{-c}$ series. If $c$ is real, that is, in the vertical plane $\phi=0$ through the origin, we may convert to divergent form for numerical calculation of $D_z$ in that plane, as done above. Also, in the horizontal plane, $\phi=\tfrac12\pi$, we have converted $D_z$ to divergent form by the generalised cosine series. The same may be done for the horizontal displacement. Put $\phi=\tfrac12\pi$ in (34). Then

$$
D_x=\frac{D_0}{\pi x}\left(1-\frac{2a^4t^4}{[4]x^2}+\frac{4a^8t^8}{[8]x^4}-\cdots\right), \tag{42}
$$

which is convergent, with the same defect practically as the similar $D_z$ formula. Next, put $a^2t^2/4x=y$, then

$$
\frac{D_x}{D_0}=\frac{(y\pi)^{1/2}}{\pi x}\left(y^{-1/2}-\frac{y^{1/2}}{[\tfrac12]}+\frac{y^{3/2}}{[\tfrac32]}-\cdots\right)
$$

$$
=\frac{(y\pi)^{1/2}}{\pi x}\left\{\cos\left(y+\tfrac14\pi\right)+\frac{y^{-3/2}}{[-2\tfrac12]}-\cdots\right\}. \tag{43}
$$

This is done by using the generalised cosine form. Or, in terms of $x$ and $t$,

$$
\frac{D_x}{D_0}=\frac{at}{2\sqrt\pi x^{3/2}}\left\{\cos\left(\frac{a^2t^2}{4x}+\tfrac14\pi\right)+\frac{y^{-3/2}}{[-2\tfrac12]}+\cdots\right\}, \tag{44}
$$

which is the companion to (27).

Now, although the calculation difficulties of the convergent formulae for any point not too near the limiting level through the origin are not comparable with those connected with the limiting level itself, it would be desirable to convert the convergent forms to divergent form as well. But it is not so easy to do it as at the limiting level, on account of difficulties in the numerical interpretation of complex divergent formulae. As a preliminary, we may transform the generalised exponential part so as to introduce a time factor of decay. Thus,

$$
\Delta^re^{-c}=e^{-c}(\Delta-1)^r=e^{-c}\Delta^r\left(1-\Delta^{-1}\right)^r
$$

$$
=e^{-c}\Delta^r\left(1-\tfrac12\Delta^{-1}-\frac{1.1}{2.4}\Delta^{-2}-\frac{1.1.3}{2.4.6}\Delta^{-3}-\cdots\right)
$$

$$
=\frac{e^{-c}}{(c\pi)^{1/2}}\left(1-c-\frac{c^2}{3[2]}-\frac{c^3}{5[3]}-\frac{c^4}{7[4]}-\cdots\right). \tag{45}
$$

Here $c$ is complex, $=y e^{-\theta i}$, if $y$ is the real $a^2t^2/4r$. So, separating the two components, we convert the complex form to

$$
D_r-iD_\phi=\frac{e^{-y\cos\phi}}{\pi r}\left\{X\cos(y\sin\phi)-Y\sin(y\sin\phi)+iX\sin(y\sin\phi)+iY\cos(y\sin\phi)\right\}, \tag{46}
$$

where

$$
X=1-y\cos\phi-y^2/3[2]\cos2\phi-y^3/5[3]\cos3\phi-\cdots,
$$

$$
Y=y\sin\phi+y^2/3[2]\sin2\phi+y^3/5[3]\sin3\phi+\cdots. \tag{47}
$$

The factor of decay in (46) is good, by itself, and if $X$ and $Y$ were of such a nature as to be readily calculable for large values of $y$, the real meaning would be ascertainable. We should rather have $X$ and $Y$ expressed in descending powers of $y$. That is, the $c$ series in (45) should be turned to an equivalent divergent series, numerically true for the real and unreal parts separately.

Try another way. Since the water is assumed to be incompressible, its state of displacement all through is entirely determined by its state at the surface level, and this connection is instantaneous. Thus, if $d/dx=\Delta$, and $d^2V/dx^2+d^2V/dz^2=0$, then

$$
V=\cos z\Delta\,V_0+\frac{\sin z\Delta}{\Delta}\frac{dV_0}{dz}, \tag{48}
$$

which finds $V$ at $x,z$ in terms of the values of $V$ and $dV/dz$ at $z=0$. But the boundary condition in this theory is

$$
\frac{dV}{dz}=\frac{\ddot V}{a^2}\qquad \text{at } z=0; \tag{49}
$$

so

$$
V=\cos z\Delta\,V_0+\frac{\sin z\Delta}{\Delta}\frac{\ddot V_0}{a^2}=\Re\,e^{z\Delta i}\left(1-\frac{ip^2}{\Delta a^2}\right)V_0. \tag{50}
$$

If we know $V_0$ as a function of $x$ and $t$, then also $\ddot V_0$. The data are complete, for the operator $e^{z\Delta i}$ turns $x$ in $V_0$ to $x+zi$. Calling this $S$,

$$
V=\Re\left(1-\frac{ip^2}{\Delta a^2}\right)V_0, \tag{51}
$$

if $\Delta=d/dS$, and $V_0$ contains $S$ instead of $x$.

If we apply this process to $D_z$ given convergently for the top level, it will give without difficulty the corresponding $D_z$ at any depth. That is, the original surface solution will be turned to the interior form. $D_x$ may be similarly treated. But now go through the same process with the divergent formula for the surface elevation. Use (27) in (51). First find the transformed factor. We have

$$
D_x=-\frac{\Delta a^2/p^2}{1+\Delta^2a^4/p^4}\frac1{x\pi},\qquad \therefore\qquad \frac{p^2D_z}{\Delta a^2}=\frac{-1}{1+\Delta^2a^4/p^4}\frac1{x\pi}=-D_x. \tag{52}
$$

By inspection of (42), and so now we can use (44) combined with (35). The oscillating terms alone make, if $y=a^2t^2/4x$,

$$
\frac{at}{2\pi^{1/2}x^{3/2}}\left(\cos\left(y-\tfrac14\pi\right)+i\cos\left(y+\tfrac14\pi\right)\right)=\cdots=\frac{at}{2\pi^{1/2}x^{3/2}}i^{1/2}e^{-yi}. \tag{53}
$$

Now change $x$ to $x+zi=re^{\theta i}$, with $y$ turned to $a^2t^2/4r$, and we get

$$
\frac{at}{2\pi^{1/2}r^{3/2}}e^{-\tfrac12 i(y\cos\theta-i\sin\theta)-\tfrac14\pi i+\tfrac12\theta}; \tag{54}
$$

of which the real part is

$$
\frac{at}{2\pi^{1/2}r^{3/2}}e^{-y\sin\theta}\cos\left(y\cos\theta-\tfrac14\pi+\tfrac12\theta\right). \tag{55}
$$

Doing the same for the divergent part of $D_2$, we get, after adding together the transformed pieces and restoring the old notation through $\theta=\tfrac12\pi-\phi$,

$$
\frac{D_z}{D_0}=\frac{at}{2\pi^{1/2}r^{3/2}}e^{-y\cos\phi}\sin\left(y\sin\phi-\tfrac12\phi\right)-\frac{2}{\pi a^2t^2}\left(1+\frac{3}{[1]}\frac{r\cos\phi}{a^2t^2}+\frac{5}{[2]}\frac{r^2\cos2\phi}{a^4t^4}+\cdots\right), \tag{56}
$$

where $y=a^2t^2/4r$. This is to represent the vertical displacement at any depth. To test harmony with former results, put $\phi=0$. Then we obtain the earlier vertical-plane formula; again, put $\phi=\tfrac12\pi$. Then we obtain the surface-elevation formula. So far good. But the first line in (56) changes sign with $\phi$. That is bad, but may be righted by the prefix $\mp$ instead of $-$, according as $\phi$ is $\pm$. Assuming that this formula is correct from $\phi=0$ to $\tfrac12\pi$, it is eminently suitable for showing the meaning without lengthy calculations. The exponential factor is very significant. The function $te^{-y\cos\phi}$ increases with the time to a maximum and then falls to zero, provided $\phi$ is less than $\tfrac12\pi$. But when $\phi=\tfrac12\pi$, the function increases for ever without limit. That is to say, at any point under the limiting plane, the oscillation set up by the initial condensed hump at the origin increases in amplitude up to a certain amount, and afterwards subsides to rest. But at the limiting level, the maximum will never be reached, so no subsidence is shown.