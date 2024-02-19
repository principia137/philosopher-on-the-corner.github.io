---
author:
- Joon sik, CAU Physics
date: September 2023
title: Hydrogen Atom Visualization
---
## Wave function table

   $n$   $l$     $m$    $\psi_{n, l, m}(r, \theta, \phi)$
  ----- ----- --------- ----------------------------------------------------------------------------------------------------------------------
    1     0       0     $\frac{1}{\sqrt{\pi} a_0^{3/2}} e^{-r/a_0}$
    2     0       0     $\frac{1}{4\sqrt{2\pi} a_0^{3/2}}\left(2-\frac{r}{a_0}\right) e^{-r/2a_0}$
    2     1       0     $\frac{1}{4\sqrt{2\pi} a_0^{3/2}} \frac{r}{a_0} e^{-r/2a_0} \cos \theta$
    2     1    $\pm 1$  $\frac{1}{8\sqrt{3\pi} a_0^{3/2}} \frac{r}{a_0} e^{-r/2a_0} \sin \theta e^{\pm i \phi}$
    3     0       0     $\frac{1}{81\sqrt{3\pi} a_0^{3/2}}\left(27-18\frac{r}{a_0}+2\frac{r^2}{a_0^2}\right) e^{-r/2a_0}$
    3     1       0     $\frac{1}{81\sqrt{3\pi} a_0^{3/2}}\left(6-\frac{r}{a_0}\right) \frac{r}{a_0} e^{-r/3a_0} \cos \theta$
    3     1    $\pm 1$  $\frac{1}{81\sqrt{3\pi} a_0^{3/2}}\left(6-\frac{r}{a_0}\right) \frac{r}{a_0} e^{-r/3a_0} \sin \theta e^{\pm i \phi}$
    3     2       0     $\frac{1}{81\sqrt{6\pi} a_0^{3/2}} \frac{r^2}{a_0^2} e^{-r/3a_0}\left(3 \cos^2 \theta-1\right)$
    3     2    $\pm 1$  $\frac{1}{81\sqrt{\pi} a_0^{3/2}} \frac{r^2}{a_0^2} e^{-r/3a_0} \sin \theta \cos \theta e^{\pm i \phi}$
    3     2    $\pm 2$  $\frac{1}{162\sqrt{\pi} a_0^{3/2}} \frac{r^2}{a_0^2} e^{-r/3a_0} \sin^2 \theta e^{\pm 2i \phi}$

  : Hydrogen Atom Wave Functions

# Probability Distribution

(set $a_0=1$)

## Radial Function($r^2 R(r)^2$) 

![for some n=1,2 , l=0,1](img/Radial.png){:width="30%"}

## Spherical Harmonic Function($Y(\theta,\phi)^2$)

$\leftarrow$ less probability    high probability $\rightarrow$
![image](img/probability.png)
  --------------------------------------- --------------------------------------- ---------------------------------------
   ![image](img/SH00.png){width="4.4cm"}   ![image](img/SH10.png){width="4.4cm"}   ![image](img/SH11.png){width="4.4cm"}
                $l=0, m=0$                              $l=1, m=0$                            $l=1, m=1, -1$
                                                                                  
   ![image](img/SH20.png){width="4.4cm"}   ![image](img/SH21.png){width="4.4cm"}   ![image](img/SH22.png){width="4.4cm"}
                $l=2, m=0$                            $l=2, m=1, -1$                          $l=2, m=2, -2$
  --------------------------------------- --------------------------------------- ---------------------------------------

  --------------------------------------- --------------------------------------- ---------------------------------------
   ![image](img/SH30.png){width="4.4cm"}   ![image](img/SH31.png){width="4.4cm"}   ![image](img/SH32.png){width="4.4cm"}
                $l=3, m=0$                            $l=3, m=1, -1$                          $l=3, m=2, -2$
                                                                                  
   ![image](img/SH33.png){width="4.4cm"}                                          
              $l=3, m=3, -3$                                                      
  --------------------------------------- --------------------------------------- ---------------------------------------

  : Spherical Harmonics

## Wave Function($\psi(r,\theta,\phi)^2=R(r)^2Y(\theta,\phi)^2$) {#wave-functionpsirthetaphi2rr2ythetaphi2 .unnumbered}

$\leftarrow$ less probability    high probability $\rightarrow$

  -------------------------------------------- -------------------------------------------- --------------------------------------------
   ![image](img/Hydrogen100.png){width="5cm"}   ![image](img/Hydrogen200.png){width="5cm"}   ![image](img/Hydrogen210.png){width="5cm"}
                $n=1, l=0, m=0$                              $n=2, l=0, m=0$                              $n=2, l=1, m=0$
                                                                                            
   ![image](img/Hydrogen211.png){width="5cm"}                                               
              $n=2, l=1, m=1, -1$                                                           
  -------------------------------------------- -------------------------------------------- --------------------------------------------

  -------------------------------------------- -------------------------------------------- --------------------------------------------
   ![image](img/Hydrogen300.png){width="5cm"}   ![image](img/Hydrogen310.png){width="5cm"}   ![image](img/Hydrogen311.png){width="5cm"}
                $n=3, l=0, m=0$                              $n=3, l=1, m=0$                            $n=3, l=1, m=1, -1$
   ![image](img/Hydrogen320.png){width="5cm"}   ![image](img/Hydrogen321.png){width="5cm"}   ![image](img/Hydrogen322.png){width="5cm"}
                $n=3, l=2, m=0$                            $n=3, l=2, m=1, -1$                          $n=3, l=2, m=2, -2$
  -------------------------------------------- -------------------------------------------- --------------------------------------------

  : Hydrogen Atom Orbitals

# MATHEMATICA Code

## DensityPlot3D {#densityplot3d .unnumbered}

![image](img/DensityPlot3D.png){width="15cm"}

## Reference {#reference .unnumbered}

<https://reference.wolfram.com/language/ref/DensityPlot3D.html>
