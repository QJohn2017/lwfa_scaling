---
author-meta:
- Andrei Berceanu
- Alessio Del Dotto
date-meta: '2019-07-24'
keywords:
- lwfa
- laser
- plasma
lang: en-US
title: Application of laser-wakefield scaling laws
...






<small><em>
This manuscript
([permalink](https://berceanu.github.io/lwfa_scaling/v/f889afc0cf8f23e2962ab23fca8112e0cf9b5f79/))
was automatically generated
from [berceanu/lwfa_scaling@f889afc](https://github.com/berceanu/lwfa_scaling/tree/f889afc0cf8f23e2962ab23fca8112e0cf9b5f79)
on July 24, 2019.
</em></small>

## Authors



+ **Andrei Berceanu**<br>
    ![ORCID icon](images/orcid.svg){.inline_icon}
    [0000-0003-4438-4440](https://orcid.org/0000-0003-4438-4440)
    · ![GitHub icon](images/github.svg){.inline_icon}
    [berceanu](https://github.com/berceanu)<br>
  <small>
     Extreme Light Infrastructure - Nuclear Physics
  </small>

+ **Alessio Del Dotto**<br>
    ![ORCID icon](images/orcid.svg){.inline_icon}
    [0000-0002-1756-5089](https://orcid.org/0000-0002-1756-5089)
    · ![GitHub icon](images/github.svg){.inline_icon}
    [aled121](https://github.com/aled121)<br>
  <small>
     Instituto Nazionale di Fisica Nucleare
  </small>



## Abstract {.page_break_before}

We apply analytical scaling laws to the parameters of the FLAME laser system,
in order to estimate the maximum obtainable electron energy and total charge in
a laser-wakefield acceleration scenario. We also roughly predict the expected
betatron radiation spectrum, emitted by the accelerated electrons.


## 1. FLAME parameters

The FLAME Laser System (FLAME) has a wavelength $\lambda_L = 800$ nanometers.
The operating laser pulse energy can range from 0.03 J up to 3 J on target.^[In
the latest experimental campaign, the aim is to use 3 J.]
Inside the laser focus, the energy is roughly 40% of that.
The pulse duration can range from 28 fs up to a maximum of 300 fs.
The beam waist is $w_0 = 15\, \mu$m.
We can take the pulse duration to be $\tau_L = 30$ fs at FWHM in intensity.

When using a gas-jet target, available plasma density range is between 1 and 5
$\times 10^{18}$ cm${}^{-3}$, correspoding to an acceleration length between 5
and 1 mm.

## 2. Electron acceleration estimate

For optimal acceleration, we impose the condition that
the dephasing length should be equal to the pump depletion length
$L_{\text{dephasing}} = L_{\text{depletion}}$ [@pHOLg7Nh].

$$L_{\text{dephasing}} = \frac{4}{3} \left(\frac{\omega_L}{\omega_p}\right)^2 \frac{\sqrt{a_0}}{k_p} = L_{\text{depletion}} = \left(\frac{\omega_L}{\omega_p}\right)^2 c \tau_L$$

In practical units, we have $\lambda_p [\mu \text{m}] = 3.34 \times 10^{10} (n_p [\text{cm}^{-3}])^{-1/2}$,
therefore $k_p [\mu \text{m}^{-1}]= 2\pi / \lambda_p  [\mu \text{m}] = 1.88 \times 10^{-10} (n_p [\text{cm}^{-3}])^{1/2}$
and $\omega_p [\text{fs}^{-1}] = 5.64 \times 10^{-11} (n_p [\text{cm}^{-3}])^{1/2}$.
This allows us to obtain the ratio $a_0/n_p$ from above.

$$\frac{a_0}{n_p [\text{cm}^{-3}]} = 1.79 \times 10^{-21} (\tau_L [\text{fs}])^2$$

### Plasma density and normalized vector potential

If we want to use any external guiding (eg via capilaries),
then we also need to impose the condition for self-guided propagation of the laser:

$$a_0 \geq \left(\frac{n_c}{n_p}\right)^{1/5}$$

with the critical density $n_c [\text{cm}^{-3}] = 1.12 \times 10^{21} / (\lambda_L [\mu\text{m}])^2$,
which is $1.75 \times 10^{21} \text{cm}^{-3}$ in our case.
Substituting above and taking the lower limit, we get

$$n_p [\text{cm}^{-3}] = \frac{1.12 \times 10^{21} }{a_0^5 (\lambda_L [\mu\text{m}])^2}$$

Substituting $n_p$ in the ratio $a_0/n_p$ from above, we finally get:

$$a_0 \approx 2^{1/6} \left( \frac{\tau_L [\text{fs}]}{\lambda_L [\mu\text{m}]} \right)^{1/3} $$

and

$$n_p [\text{cm}^{-3}] = 6.29 \times 10^{20} \frac{1}{(\lambda_L [\mu\text{m}])^{1/3} (\tau_L [\text{fs}])^{5/3}}$$

For FLAME parameters, we get $a_0 \approx 3.7$ and $n_p \approx 2.3 \times 10^{18} \text{cm}^{-3} = 13 \times 10^{-4} n_c$.


For $a_0 \geq 4-5$ we also get **self-injection** from pure Helium.

Helium has the **ionization** energies 24.59 eV (He${}^{+}$) and 54.42 eV (He${}^{2+}$),
corresponding to laser intensities $1.4 \times 10^{15}$, respectively $8.8 \times 10^{15}$ W/cm${}^2$ [@XIzWHcCi],
and will therefore be easily ionized by the laser prepulse.

Knowing the density, we get $\omega_p = 8.63 \times 10^{-2}$ fs${}^{-1}$,
and more importantly, $\omega_p^{-1} = 11.59$ fs,
which is the same order of magnitude as the pulse duration $\tau_L = 30$ fs.
For $\tau_L \gg \omega_p^{-1}$ (eg. $\tau_L = 600$ fs), one would either be in the **SMLWFA** or **DLA regime**,
depending on the value of $a_0$.

### Beam waist

We also need to match the beam waist $w_0$ of the focused Gaussian laser pulse to the plasma, giving the condition $w_0 k_p = 2 \sqrt{a_0}$, so

$$w_0 [\mu \text{m}] = 1.06 \times 10^{10}   \left(\frac{a_0}{n_p [\text{cm}^{-3}]}\right)^{1/2} = 44.84  \frac{\tau_L [\text{fs}]}{100}$$

For FLAME, we get $w_0 \approx 13 \mu \text{m}$ at $1/e^2$ intensity, so FWHM (1/2 intensity) = $w_0 \sqrt{2 \ln{2}} \approx 18 \mu$m.

### Laser energy, power and intensity

We now estimate the required laser energy $\varepsilon_L$.
The peak laser intensity in the focal plane is 

$$I_L [10^{18} \text{W}/\text{cm}^2 ] \approx 6 \times 10^4  \frac{\varepsilon_L [\text{J}]}{\tau_L [\text{fs}] (w_0 [\mu \text{m}])^2}$$

so for our parameters $I_L \approx 2.96 \times 10^{19}$ W/cm${}^2$.
For a relative scale, the atomic Coulomb field is on the order of $10^{14}$ W/cm${}^2$
and relativistic effects become important for laser intensities above $10^{17}$ W/cm${}^2$ ($a_0 \geq 1$),
while QED effects such as radiation reaction only become important for intensities beyond $\sim 2 \times 10^{21}$ W/cm${}^2$.
We know that $a_0 = 0.855 \lambda_L [\mu\text{m}] (I_L [10^{18} \text{W}/\text{cm}^2 ])^{1/2}$, so

$$\varepsilon_L [\text{J}] = 2.28 \times 10^{-5} a_0^2 (w_0 [\mu \text{m}])^2 \frac{\tau_L [\text{fs}] }{(\lambda_L [\mu\text{m}])^2} = 5.68 \times 10^{-6} \frac{ (\tau_L [\text{fs}])^{11/3} }{(\lambda_L [\mu\text{m}])^{8/3}}$$

Therefore, for FLAME we need $\varepsilon_L \approx 2.7$ J on target.
The laser power on target is

$$P [\text{TW}] = 2.41 \times 10^{18}   \frac{a_0^3}{n_p [\text{cm}^{-3}]} \frac{1}{(\lambda_L [\mu\text{m}])^2}$$

$$P [\text{TW}] = 2 \times 10^3 \sqrt{\frac{\ln{2}}{\pi}} \frac{1}{\tau_L [\text{fs}]} \varepsilon_L [\text{J}] = 5.34 \times 10^{-3} \left(\frac{ \tau_L [\text{fs}] }{\lambda_L [\mu\text{m}]}\right)^{8/3}$$

so approximately 84 TW in our case.

### Acceleration distance

The optimum propagation distance is equal to $L = L_{\text{dephasing}} (= L_{\text{depletion}})$.

$$L [\text{mm}] = 3.34 \times 10^{17} \frac{\tau_L[\text{fs}]}{ (\lambda_L [\mu\text{m}])^2} \frac{1}{n_p [\text{cm}^{-3}]} = 5.31 \times 10^{-4} \frac{(\tau_L [\text{fs}])^{8/3}}{ (\lambda_L [\mu\text{m}])^{5/3}}$$

which for FLAME amounts to $L \approx 7$ mm.

### Maximum electron energy and charge

The maximum electron energy that can be reached under these circumstances is

$$\gamma = \frac{\Delta \varepsilon}{mc^2} = \frac{2}{3} a_0 \frac{\omega_L^2}{\omega_p^2}$$

$$\gamma = 7.44 \times 10^{20} \frac{a_0}{n_p [\text{cm}^{-3}]} \frac{1}{ (\lambda_L [\mu\text{m}])^2 } = 1.33 \left(\frac{\tau_L [\text{fs}]}{ \lambda_L [\mu\text{m}] }\right)^2 $$

$$\Delta \varepsilon [\text{GeV}]= 5.11 \times 10^{-4} \gamma = 6.8 \times 10^{-4} \left(\frac{\tau_L [\text{fs}]}{ \lambda_L [\mu\text{m}] }\right)^2$$

For FLAME, we get $\Delta \varepsilon = 0.95$ GeV and a Lorentz factor $\gamma = 1870$.

We assume the blowout radius $R = w_0 = 44.84 \tau_L [\text{fs}]/100 = 18 \, \mu$m.
The number of accelerated electrons $N_e \propto R^3 n_p$ is equal to the ionic charge of the bubble, so [@pHOLg7Nh]

$$N_e \approx 3.13 \times 10^8 \lambda_L [\mu\text{m}] \left(P [\text{TW}]\right)^{1/2} = 2.28 \times 10^7  \frac{ (\tau_L [\text{fs}])^{4/3} }{ (\lambda_L [\mu\text{m}])^{1/3} }$$

$$N_e \approx 4.85 \times 10^{17}   \frac{a_0^{3/2}}{(n_p [\text{cm}^{-3}])^{1/2}}$$

giving a charge

$$Q_e [\text{pC}] = N_e \times e [\text{pC}] \approx 3.65  \frac{ (\tau_L [\text{fs}])^{4/3} }{ (\lambda_L [\mu\text{m}])^{1/3} }$$

For FLAME we get $Q_e \approx 366 \, \text{pC} \approx 0.36$ nC and $N_e = 2.29 \times 10^9$ electrons.
As a last note, with PW lasers, the higher laser energy can be focused to a larger focal spot matched by a lower plasma density.

## 3. Betatron emission

After matching the laser spot size, and pulse duration to the plasma density,
we can look at betatron emission [@2hiGds1a].
The betatron oscillation radius $r_{\beta} = 3\, \mu$m for a blowout radius $R = 21 \, \mu$m.
Since the betatron oscillations are limited by the bubble size,
it is reasonable to assume a linear dependence on $R$ and
therefore take $r_{\beta} = 2.6 \, \mu$m in our case.

We now need to work out the five relevant parameters for the wiggler:
the relativistic electron factor $\gamma$,
the number of electrons $N_e$,
the strength parameter $K$,
the period of the wiggler $\lambda_u$
and the number of (betatron) periods $N$.
We already know the first two parameters.
Once we have the parameters,
we can calculate the critical radiation energy $\hbar \omega_c$,
the opening angle of the radiation $\theta_r$
and the number of emitted photons per electron and per betatron period, $N_{\gamma}$.
We can then get the total number of emitted photons per laser shot, $N_{\gamma} \times N_e \times N$.

$$\theta_r [\text{mrad}] = 10^3 \times \frac{K}{\gamma} $$
$$N_{\gamma} = 3.31 \times 10^{-2} K$$
$$\hbar \omega_c [\text{keV}] = 1.86 \times 10^{-3} \frac{K \gamma^2}{\lambda_u [\mu\text{m}]}$$

### Wiggler parameters

In the case of betatron oscillations, the strength parameter is given by

$$K = \sqrt{\frac{\gamma}{2}} \left(k_p [\mu\text{m}^{-1}]\right) (r_{\beta} [\mu\text{m}]) = 1.33 \times 10^{-10} r_{\beta} [\mu\text{m}] (\gamma \, n_p [\text{cm}^{-3}])^{1/2}$$

so $K \approx 26$ in our case, which puts us in the wiggler regime $K \gg 1$.

$$\lambda_u [\mu\text{m}]= \sqrt{2} \gamma^{1/2} (\lambda_p [\mu\text{m}]) = 4.72 \times 10^{10}  \left(\frac{\gamma}{n_p [\text{cm}^{-3}]}\right)^{1/2}$$

so $\lambda_u = 1334 \, \mu\text{m} = 1.33$ mm.

### Radiation properties

We now easily obtain $\theta_r = 14$ mrad and $N_{\gamma} = 0.87$ photons / (electron x betatron period).
While the electrons radiate throughout the whole acceleration process,
the main contribution comes from the part of the trajectory where their energy is maximum,
ie, after the distance $L$.
If the electron is around its maximum energy for about $N \sim 3$ betatron periods,
the total number of emitted photons per shot will be
$N_{\gamma}^{\text{shot}} = N_{\gamma} \times N_e \times N = 0.87 \times 2.28 \times 10^9 \times 3 \approx 6 \times 10^9$ photons.
Finally, the critical energy is in our case $\hbar \omega_c = 128$ keV.

**Note:** The betatron amplitude $r_{\beta} \propto \sqrt{a_0/n_p}$ and the numer of betatron oscillations $N \propto 1/\sqrt{n_p}$.

## 4. Quantum effects

We are now ready to estimate the size of the quantum corrections.
Quantum effects become important when the electron energy loss due to photon emission becomes comparable to the electron energy.

Radiation reaction can be neglected when the electron - laser interaction duration is much smaller
than the electron energy loss rate, or equivalently,
the number of oscillations $N \ll N_{\text{RR}}$, with [@2hiGds1a]

$$N_{\text{RR}} = 2.7 \times 10^7 \frac{\lambda_u [\mu\text{m}]}{\gamma K^2}$$

so for FLAME parameters $N_{\text{RR}} \sim 2.8 \times 10^4 \gg N$.


## References {.page_break_before}

<!-- Explicitly insert bibliography here -->
<div id="refs"></div>
