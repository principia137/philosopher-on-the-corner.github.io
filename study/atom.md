---
author:
- Joon Sik, CAU Physics
date: September 2023
title: Hydrogen Atom Visualization
---

# 수소원자 확률분포의 시각화
### 수소원자는 '실제로' 어떻게 생겼을까?
수소원자의 파동함수를 구하고 확률분포를 시각화 해보자. 우리는 수소원자가 어떻게 '생겼냐'를 묻고 있으므로 '위치'에 대한 확률분포를 구하면 된다. 여기서 내가 제목을 그냥 수소원자의 시각화가 아니라 수소원자의 확률분포의 시각화라고 한 이유는 글쎄 나는 수소원자가 실제로 어떻게 생겼냐고 묻는다면 잘 모르겠다.  
우리가 슈뢰딩거 방정식을 풀어내서 일반해를 구했지만 특정한 해를 함수형태로 알고 있는 것은 아니다. 그러니까 일반해를 얻긴 했지만 일반해는 각각 에너지 고유상태들의 선형결합으로 이루어져 있는데 각 고유상태들의 계수가 정해지지는 않았다. 문제를 풀 때에는 문제에서 함수형태를 주어주기도 하지만 과연 실제로는 어떨지는 모르는 것이다. 그래서 보통 수소원자 확률분포의 시각화에서 보여주는 그림은 각각 양자수 n, l, m에 따른 개별 고유상태에서의 파동함수에 대한 것을 보여준다. 그런데 만약 정확한 파동함수의 형태를 우리가 알고 있는 경우나 모르는 경우나 어쨋든 위치는 공간상에 확률적으로 퍼져있기 때문에(여러 가능성이 중첩되어있기 때문에) 이것을 수소원자가 어떻게 '생겼는지' 말해준다고 하기에는 조금 애매해 보인다. 어쨋든 수소 원자핵을 중심으로 근방에 전자가 하나 존재하긴 할 것이다.  
이해하기 쉽게 쓴다고 썻는데 내 말이 잘 전달이 되었는지는 모르겠다. 어쨌거나 지금 보이려고 하는 것은 각 고유상태별로 수소원자의 '위치에 대한 확률분포'라고 명확하게 해두겠다.

### 확률분포 시각화하는 방법
3차원 공간상에서 확률분포를 표현하고 싶다면 어떻게 해야 할까. 어렵게 생각할 필요 없이 그냥 3차원 좌표에서 임의의 위치마다 그 지점에 확률이 얼마인지를 쓰면 된다.
만약 우리가 1차원 공간(공간 변수가 1개인)에서 파동함수에 대한 확률을 표현하고 싶다면 x축을 공간좌표로 쓰고 y축을 확률값으로 하면된다. 2차원 공간에서 파동함수의 확률을 표현하고 싶다면 x축, y축을 공간좌표로 쓰고 z축을 확률값으로 하면된다. 그런데 3차원 공간에서 파동함수의 확률을 표현하고 싶다면? x축, y축, z축을 공간좌표로 쓰면 더이상 확률을 표현할 차원이 없다. 우리는 3차원 세상까지만 인식할 수 있기때문이다. 그래서 확률값을 새로운 축을 통해 표현하기는 힘들기 때문에 각 지점에 대응하는 확률을 그 지점에 '색깔', '투명도' 따위로 표현하면 된다. 따라서 우리는 3차원 공간상에서 각 지점에 색깔을 통해 값을 할당 할 수 있는 컴퓨터 도구가 필요하다. 그 도구중 하나는 Mathematica의 "3D Density Plot"함수이다.


매스매티카를 써야하는 이유




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
