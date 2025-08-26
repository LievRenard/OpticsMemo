# Mie Scattering



빛이 작은 입자를 지나면 여러 방향으로 퍼져나가는 산란이 일어나게 된다. 이때 입자의 크기가 파장보다 많이 작으면 레일리 산란(Rayleigh scattering), 입자의 크기가 파장과 비슷하거나 더 크면 미 산란(Mie scattering)이 일어나게 된다. 레일리 산란과 비교되는 미 산란의 특징은, 파장의 네제곱에 반비례하는 레일리 산란과는 달리 미 산란은 비교적 파장에 고르게 산란이 일어난다는 것이다. 또한 빛의 진행 방향으로 산란되는 전방 산란(front scattering)과 반대 방향의 후방 산란(back scattering)에 대해, 레일리 산란은 전방과 후방 산란이 상대적으로 비슷한 정도지만, 미 산란은 전방 산란의 양이 후방 산란보다 많다는 차이점이 있다.

![https://i.sstatic.net/uoXQb.gif](https://i.sstatic.net/uoXQb.gif)



### 미 산란 계수

![img](https://upload.wikimedia.org/wikipedia/commons/thumb/6/60/Miewiki.svg/250px-Miewiki.svg.png)

어떤 산란체에 대한 헬름홀츠 방정식 &nabla;<sup>2</sup>**E**+k<sup>2</sup>**E**=0을 풀면 이 때의 해는 입사파 E<sub>inc</sub>. 산란파 E<sub>s</sub>, 내부 전기장 E<sub>i</sub>의 합으로 나타낼 수 있고, 균일한 등방성 구체에 대해 이러한 세 전기장 해는 벡터 구면 조화 함수로 아래와 같이 전개할 수 있다.
$$
\bold E_{inc}=\sum^\infin_{n=1}E_n(\bold M^{(1)}_{1n}(k,\bold r)-i\bold N^{(1)}_{1n}(k,\bold r)) \\
\bold E_s=\sum^\infin_{n=1}E_n(ia_n\bold N^{(3)}_{1n}(k,\bold r)-b_n\bold M^{(3)}_{1n}(k,\bold r)) \\
\bold E_i=\sum^\infin_{n=1}E_n(-id_n\bold N^{(1)}_{1n}(k_1,\bold r)+c_n\bold M^{(1)}_{1n}(k_1,\bold r))
$$
여기서 산란파와 내부 전기장의 계수, a<sub>n</sub>, b<sub>n</sub> ,c<sub>n</sub>, d<sub>n</sub>을 미 산란 계수라고 한다. 미 산란 계수는 아래와 같이 리카티-베셀 함수 &psi;<sub>n</sub>(x)=xj<sub>n</sub>(x), &xi;<sub>n</sub>(x)=xh<sup>(1)</sup><sub>n</sub>(x)를 이용하여 쓸 수 있다.
$$
a_n=\frac{\mu n_1\psi'_n(ka)\psi_n(k_1a)-\mu_1n\psi'_n(k_1a)\psi_n(ka)}{\mu n_1\xi'_n(ka)\psi_n(k_1a)-\mu_1n\psi'_n(k_1a)\xi_n(ka)}\\
b_n=\frac{\mu_1 n\psi'_n(ka)\psi_n(k_1a)-\mu n_1\psi'_n(k_1a)\psi_n(ka)}{\mu_1 n\xi'_n(ka)\psi_n(k_1a)-\mu n_1\psi'_n(k_1a)\xi_n(ka)}\\
c_n=\frac{\mu_1n\xi'_n(ka)\psi_n(ka)-\mu_1n_1\psi'_n(ka)\xi_n(ka)}{\mu_1 n\xi'_n(ka)\psi_n(k_1a)-\mu n_1\psi'_n(k_1a)\xi_n(ka)}\\
d_n=\frac{\mu_1n_1n^2\xi'_n(ka)\psi_n(ka)-\mu_1n_1^2n\psi'_n(ka)\xi_n(ka)}{\mu n_1\xi'_n(ka)\psi_n(k_1a)-\mu_1 n\psi'_n(k_1a)\xi_n(ka)}\\
$$


### 산란 단면적

빛이 물체에 맞고 산란될 때, 빛의 입장에서 느끼는 유효 단면적을 산란 단면적(scattering cross-section)이라고 한다. 이 외에도 흡수에 대한 흡수 단면적(absorption cross-section)이 있고, 산란과 흡수를 모두 고려한 소멸 단면적(extinction cross-section)이 있다. 산란 단면적 C<sub>s</sub>, 흡수 단면적 C<sub>a</sub>와 소멸 단면적 C<sub>e</sub> 사이에는 아래의 관계가 만족한다.
$$
C_e=C_s+C_a
$$
또한, 이러한 단면적들을 실제 물체의 단면적으로 나누면 효율이 되며, 각각 Q<sub>s</sub>, Q<sub>a</sub>, Q<sub>e</sub>로 표현한다. 미 산란에서 산란 효율과 흡수 효율은 미 산란 계수를 이용하여 아래와 같이 나타낼 수 있다.
$$
Q_s=\frac2{k^2a^2}\sum^\infin_{n=1}(2n+1)(|a_n|^2+|b_n|^2) \\
Q_a=\frac2{k^2a^2}\sum^\infin_{n=1}(2n+1)\Re(a_n+b_n)
$$
여기서 특정 n에 대한 항만을 꺼내면 특정 모드의 기여분을 계산할 수 있다.

한편, 미 산란에서는 서로 다른 모드가 겹쳐져서 특정 방향으로 산란이 잘 일어나는 방향성이 생기는데, 이를 커커 효과(Kerker effect)라고 한다. 미 산란에서 전방 산란 단면적과 후방 산란 단면적은 그 값이 아래와 같이 다르며,
$$
C_s^{backward}=\frac1{k^2a^2}\bigg|\sum^\infin_{n=1}(2n+1)(-1)^n(a_n-b_n)\bigg|^2 \\
C_s^{forward}=\frac1{k^2a^2}\bigg|\sum^\infin_{n=1}(2n+1)(a_n+b_n)\bigg|^2
$$
이에 따라 n>1인 항이 0일 때인 쌍극자 근사(dipole approximation) 조건에선 a<sub>1</sub>-b<sub>1</sub>=0 (first Kerker condition)이면 후방 산란이 최소화되고  a<sub>1</sub>+b<sub>1</sub>=0 (second Kerker condition)이면 전방 산란이 최소화되는 모습을 보인다.



### 미 산란과 다중극 모드

벡터 구면 조화 함수에서도 언급했듯, 각각의 모드 N<sub>mn</sub>과 M<sub>mn</sub>으로 인한 방사 패턴은 전기나 자기 쌍극자, 사중극자 등의 방사 패턴과 유사하여 이들을 다중극 모드(multipole mode)라 부른다. 예를 들어 N<sub>m1</sub>은 전기 쌍극자(ED) 모드, M<sub>m1</sub>은 자기 쌍극자(MD)모드, N<sub>m2</sub>와 M<sub>m2</sub>는 전기와 자기 사중극자(EQ, MQ) 모드인 식이다. 또한 전기장이나 자기장이 마치 토로이드(솔레노이드의 처음과 끝을 이어 말아놓은 것) 모양을 띠는 토로이달(toroidal) 모드라는 것도 존재한다. 토로이달 모드와 다른 다중극 모드가 상쇄 간섭을 일으켜 산란 효율이 0으로 떨어지는 상태를 아나폴(anapole)이라고 한다.

![img](https://upload.wikimedia.org/wikipedia/commons/thumb/0/09/Siwiki.svg/1024px-Siwiki.svg.png)

![img](https://upload.wikimedia.org/wikipedia/commons/9/97/Cross_section_vs._wavelength_of_Au_nanoparticle_cropped.png)

미 산란에서 입자의 크기와 물성에 따라 각각의 다중극 모드의 기여도가 달라진다. 예를 들어 유전체 구의 경우, 실리콘처럼 굴절률이 큰 경우엔 쌍극자 모드 외에도 사중극자 모드까지도 선명한 peak를 보이지만, 굴절률이 낮으면 이들이 서로 겹쳐 peak 폭이 넓어지는 모습을 보인다. 또한 입자의 크기가 아주 작아서 레일리 산란에 가까워지면 전기 쌍극자 모드가 우세해지고, 반면 입자의 크기가 충분히 큰 경우에는 빛이 입자 표면을 따라 진행하는 whipering gallery mode(WGM)라는 모드가 생길 수 있다. 충분히 작은 구형 금속 입자의 경우에도 전기 쌍극자 모드가 우세하고, 이때의 공명을 localised plasmon resonance라고 한다.