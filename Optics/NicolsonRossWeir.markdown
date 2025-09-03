# Nicolson-Ross-Weir Method



Nicolson-Ross-Weir(NRW) 방법이란 어떤 테스트 물질의 반사와 투과 성질(S-parameter)을 통해 광학적 특성, 즉, 유전율과 투자율을 알아내는 방법이다. 이 방법을 통해서 메타물질의 유효 굴절률 역시 계산할 수 있다.

우선 S-parameter S<sub>11</sub>과 S<sub>21</sub>은 아래와 같이 반사 계수 Γ과 투과 계수 T를 통해 나타낼 수 있다. S-parameter는 테스트 물질의 양쪽 면에서 반복적으로 반사된 빛들의 합을 이용해서 기하급수의 합을 이용하여 구할 수 있다.
$$
S_{11}=\frac{(1-T^2)\Gamma}{1-\Gamma^2T^2} \\
S_{21}=\frac{(1-\Gamma^2)T}{1-\Gamma^2T^2}
$$
이것을 역산하면 아래와 같이 S-parameter를 이용해 반사 계수와 투과 계수를 얻을 수 있다.
$$
X=\frac{1-S_{21}^2+S_{11}^2}{2S_{11}} \\
\Gamma=X\pm\sqrt{X^2-1} \\
T=\frac{S_{11}+S_{21}-\Gamma}{1-(S_{11}+S_{21})\Gamma}=\frac{V_1-\Gamma}{1-V_1\Gamma}
$$
이 때, 물질이 passive 물질(빛이 증폭되지 않고 감쇠만 하는 물질)이므로 Γ에 대한 식 안의 부호는 Γ의 값이 |Γ|≤1이 되도록 설정되어야 한다. 한편, 반사 계수와 투과 계수는 아래와 같이 굴절률 n과 임피던스 Z로 구할 수도 있으며,
$$
\Gamma=\frac{Z-Z_0}{Z+Z_0} \\
T = e^{i\gamma L}=e^{ik_0 nL}
$$
여기서 굴절률과 임피던스는 아래와 같이 구해진다.
$$
Z=Z_0\frac{1+\Gamma}{1-\Gamma} \\
n=\frac{\ln T}{ik_0L}
$$
또는 Weir가 Nicolson-Ross의 방법을 수정한 것으로 아래와 같이 유전율과 투자율을 구할 수도 있다.
$$
\mu_r=\frac{\lambda_0}\Lambda\bigg( \frac{1+\Gamma}{1-\Gamma} \bigg) \\
\epsilon_r =\frac{\lambda_0^2}{\mu_r}\frac1{\Lambda^2}
$$
여기서,
$$
\frac1\Lambda=\sqrt{-\bigg[ \frac{\ln(1/T)}{2\pi d} \bigg]^2} \\
\ln\frac1T=\ln\bigg|\frac1T\bigg|+i\bigg( \arg\frac1T+2\pi m \bigg), \qquad m\in\mathbb N
$$
이 된다. 여기서 m은 복소 로그함수의 성질때문에 생기는데, 이것으로 인해 발생하는 문제를 분기 문제(branch problem)라고 한다. 정확한 유전율과 투자율을 구하기 위해 m을 적절하게 결정하는 것이 중요한데, 테스트 물질의 두께가 파장의 절반보다 작을 경우, m은 0으로 두어도 무방하다.



### 레퍼런스 면 보정

만약 S-parameter를 얻은 레퍼런스 면이 테스트 물질의 경계와 떨어져 있을 경우 이를 보정해주어야 한다. 보정은 얻은 S-parameter를 레퍼런스 면과 테스트 물질의 표면까지의 거리 R<sub>1</sub>, R<sub>2</sub>로 나눠준다.
$$
S^C_{11}=\frac{S_{11}}{R_1^2} \\
S^C_{21}=\frac{S_{21}}{R_1R_2}
$$