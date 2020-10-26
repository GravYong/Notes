# Chapter 4. Energy Conservation

Let us consider the net energy in a unit time passing the sphere of a radius $r$, $L(r)$, or $L(m)$.

In the shell $[r,r+\text dr]$, or $[m,m+\text dm]$

1. If no energy generation/absorption

   - Eulerian picture: fixed fluid position
     $$
     \frac{\partial L}{\partial r}=0
     $$

   - Lagrange's picture: the coordinates move with mass
     $$
     \frac{\partial L}{\partial m}=0
     $$

   - In astrophysics, Lagrange's picture is usually adopted. One example is the perturbation theory.

     >In the perturbation theory, people usually consider a mass element with certain thermaldynamical quantities, such as $\rho$, $T$, $P$, etc. As the mass element moves, the change in each quantity can be easily characterized with its partial derivative with respect to $m$. Important applications include
     >
     >- Stellar pulsation
     >- Tidal perturbation of NS/WD and the gravitational radiation (GW)

2. If the energy is generated by nuclear burning
   $$
   \text dL=4\pi r^2\rho\text dr\cdot\varepsilon_\text{nuc}
   $$
   where $\varepsilon_\text{nuc}$ is the **energy generation rate per unit mass**. Then
   $$
   \frac{\partial L}{\partial m}=\varepsilon_\text{nuc}
   $$
   and
   $$
   \Delta E=\Delta mc^2\sim\Delta t\int_0^M\varepsilon_\text{nuc}\text dm
   $$

3. If the energy is used to increase the internal energy and/or expand/contract a mass shell

   The first law in thermodynamics requires
   $$
   \text de+P\text{d}\left(\frac1\rho\right)=T\text ds\Rightarrow \frac{\partial e}{\partial t}+P\frac{\partial}{\partial t}\left(\frac1\rho\right)=T\frac{\partial s}{\partial t}
   $$
   we $s$ is the **specific entropy**. Thus
   $$
   \frac{\partial L}{\partial m}=\varepsilon_\text{nuc}-T\frac{\partial s}{\partial t}\equiv \varepsilon_\text{nuc}+\varepsilon_\text{gas}
   $$
   For contraction, $\varepsilon_\text{gas}>0$, or expansion, $\varepsilon_\text{gas}<0$. Therefore, if there is no nuclear burning, $\partial L/\partial m=\varepsilon_\text{gas}$, and the total luminosity is given by
   $$
   \begin{align*}
   L&=\int_0^M\frac{\partial L}{\partial m}\text dm=-\int_0^M\text dm\left[\frac{\partial e}{\partial t}+P\frac{\partial}{\partial t}\left(\frac1\rho\right)\right]\\
   &=-\frac{\text dE_\text{int}}{\text dt}-\int_0^MP\frac{\partial}{\partial t}\left(\frac1\rho\right)\text dm
   \end{align*}
   $$
   From the perspective of energy conservation, the second term should correspond to the time derivative of $E_\text{g}$. Now we give a proof.

   The virial theorem reveals that
   $$
   E_g=-3\int_0^M\frac{P}{\rho}\text dm
   $$
   The time derivative is thus
   $$
   \frac{\text dE_\text{g}}{\text dt}=-3\int_0^M\left[\frac{\partial P}{\partial t}\frac{1}{\rho}+P\frac{\partial}{\partial t}\left(\frac1\rho\right)\right]\text dm
   $$
   We just need to prove
   $$
   -3\int_0^M\left[+P\frac{\partial}{\partial t}\left(\frac1\rho\right)\right]\text dm=\int_0^MP\frac{\partial}{\partial t}\left(\frac1\rho\right)\text dm \Leftarrow 3P\frac{\partial}{\partial t}\left(\frac1\rho\right)+4\frac{\partial P}{\partial t}\frac{1}{\rho}=0
   $$

   $$
   \iff 3\frac{\partial \ln(1/\rho)}{\partial t}+4\frac{\partial \ln P}{\partial t}=4\frac{\partial \ln P}{\partial t}-3\frac{\partial \ln \rho}{\partial t}=0
   $$

   $$
   \iff\frac{\partial}{\partial t}\ln\left(\frac{P}{\rho^{4/3}}\right)=0
   $$

   This is true for the radiation-dominated case, where
   $$
   P\propto\rho^{4/3}
   $$
   Finally, we have derived
   $$
   L=-\frac{\text d}{\text dt}\left(E_\text{int}+E_\text g\right)
   $$
   simply assuming spherical symmetry, hydrostatic equilibrium in radiation-dominated fluid.

4. If neutrinos carry energy away, we have to somehow modify our equation
   $$
   \frac{\partial L}{\partial m}=\varepsilon_\text{nuc}+\varepsilon_\text{gas}-\varepsilon_\nu
   $$
   Neutrinos hardly interact with matter. The typical cross section for neutrino scattering is $\sigma_\nu\sim10^{-44}$ cm$^{2}$, about 20 orders of magnitude smaller than the cross section of Thomson scattering. Take the Sun as an example, the mean free path $l_\text{mfp}$ of neutrinos in the Sun is
   $$
   l_{\text{mfp},\nu}=\frac1{n\sigma_\nu}\sim10^{19-20}\text{ cm}>1\text{ AU}\gg R_\odot
   $$
   As a result, neutrinos produced in the Sun escape without any scattering. They can be treated as an energy sink in stars.



## Total Energy Conservation of a Star

The energy conservation law of the whole star is
$$
L+L_\nu=-\frac{\text d}{\text dt}\left(E_\text{int}+E_\text{g}+E_\text{nuc}\right)
$$
where the **nuclear energy** $E_\text{nuc}$ is given by
$$
E_\text{nuc}=\int\text dt\int_0^M\varepsilon_\text{nuc}\text dm
$$
On the other hand,
$$
L=\int_0^M\left(\varepsilon_\text{nuc}+\varepsilon_\text{gas}-\varepsilon_\nu\right)\text dm=-\frac{\text dE_\text{nuc}}{\text dt}-L_\nu+\int_0^M\varepsilon_\text{gas}\text dm
$$

$$
\Rightarrow \frac{\text d}{\text dt}\left(E_\text{int}+E_\text{gas}\right)+\int_0^M\varepsilon_\text{gas}\text dm=0
$$



## Energy Source of the Sun

**Nuclear timescale**
$$
t_\text{nuc}=\frac{E_\text{nuc}}{L}
$$
is the timescale of continuous, stable nuclear burning in a star. Considering the hydrogen fusion
$$
\ce{4 ^1H->^4He}\Rightarrow Q=\frac{\Delta mc^2}{4m_p}=6.3\times10^{18}\text{ erg/g}
$$
where $Q$ stands for the available energy per unit mass.

For the Sun,
$$
t_\text{nuc}\sim\frac{M_\odot Q}{L_\odot}\sim10^2\text{ Gyr}
$$
Recall that
$$
t_\text{sc}\approx t_\text{ff}\sim 10^3\text{ s}\quad\ll\quad t_\text{KH}\sim 10^{0-1}\text{ Myr}\quad \ll \quad t_\text{nuc}\sim10^2\text{ Gyr} 
$$
This is usually the case for a normal, stable star.

**What Powers Our Sun?**

The energy conversion efficiency of the Sun is approximately
$$
\sim\frac{L_\odot}{M_\odot}=1.5\text{ erg/s/g}
$$
According to radioactive elements in comets, the age of our system is at least $\sim 10$ Gyr.

1. Gravity
   $$
   Q\sim\frac{E_\text{g}}{M_\odot}\sim\frac{GM_\odot}{R_\odot}=2\times10^{15}\text{ erg/s}
   $$
   Considering the energy conversion efficiency, the Sun would be burnt out after
   $$
   t_\text{g}\sim10^{15}\text{ s}\sim10^2\text{ Myr}
   $$
   Not enough!

2. Chemical Reaction

   For hydrogen atoms, $E\sim13.6$ eV, so
   $$
   Q\sim \frac{13.6\text{ eV}}{m_p}=10^{13}\text{ erg}/g\Rightarrow t_\text{chem}<1\text{ Myr}
   $$
   Not enough!

3. Nuclear Burning
   $$
   t_\text{nuc}\sim10^2\text{ Gyr}
   $$
   Sufficient!