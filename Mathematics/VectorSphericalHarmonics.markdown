# Vector Spherical Harmonics



구면 상에서 라플라스 방정식을 풀 때, 각도 방향 해로 튀어나오는 함수가 바로 구면 조화 함수(spherical harmonics)
$$
Y^m_l(\theta,\phi)=Ne^{im\phi}P^m_l(\cos\theta)
$$
이다. 예를 들어 우리가 수소의 슈뢰딩거 방정식을 풀 때, 각도방향 해로 이 구면 조화 함수가 나오며, 수소 원자의 각운동량 양자수와 자기 양자수 l, m이 여기서 튀어나오는 것이다. 이것을 벡터장에 대해 확장한 것이 **벡터 구면 조화 함수(vector spherical harmonics)**이다. 이 벡터 구면 조화 함수는 Mie 산란과 같이 구면 좌표계에서 맥스웰 방정식 같은 것들을 풀 때 주로 등장한다.



### 벡터 구면 조화 함수의 정의

벡터 구면 조화 함수는 아래와 같이 radial 방향 벡터 **r**을 이용하여 정의된다.
$$
\bold{Y}_{lm}=Y_{lm}\hat{\bold r} \\
\bold{\Psi}_{lm}=r\nabla Y_{lm} \\
\bold{\Phi}_{lm}=\bold r \times\nabla Y_{lm}
$$
여기서 **Y**는 radial 방향 해, **&Psi;**와 **&Phi;**는 angular 방향 해에 해당한다. l과 m은 수소 원자의 l, m 양자수의 범위처럼 0 &le; l &lt; &infin;, -l &le; m &le; l 범위를 가지며, 세 함수의 여러 l과 m 모드의 선형 결합으로 구면 좌표 위의 모든 해를 나타낼 수 있다.



### LMN 기저

**Y**, **&Psi;**, **&Phi;**를 사용한 기저로 구면 좌표 위의 방정식의 해를 나타내기에 충분하지만, Mie 산란 문제를 풀 때 나오는 헬름홀츠 방정식에 특화된 또 다른 벡터 구면 조화 함수 기저들이 존재한다. 우선 위에서 라플라스 방정식의 구면 조화 함수를 가져왔을 때 처럼 헬름홀츠 방정식의 해를 가져오자.
$$
\psi_{emn}=\cos(m\phi)P^m_n(\cos\theta)z_n(kr) \\
\psi_{omn}=\sin(m\phi)P^m_n(\cos\theta)z_n(kr) 
$$
여기서 z<sub>n</sub>은 구면 베셀 함수를 의미한다.

그러면 위에서 본 식 (2)와 유사한 정의를 통해 헬름홀츠 방정식에 대한 벡터 구면 조화 함수를 정의할 수 있다. (e, o에 대한 notation은 생략했다.)
$$
\bold L_{mn} = \nabla\psi_{mn} \\
\bold M_{mn} = \nabla\times(\bold r\psi_{mn}) \\
\bold N_{mn} = \frac{\nabla\times\bold M_{mn}}{k}
$$
여기서 L은 longitudinal harmonics, M은 magnetic harmonics, N은 electric harmonics라고 불린다. 보통은 빛이 산란되어 방사될 때, 전기장이 빛의 진행방향인 radial 방향에 수직할 것이므로 L은 잘 사용하지 않는다. 

또한 z<sub>n</sub>에 사용한 구면 베셀 함수의 종류가 뭔지 표기하는 경우도 종종 있는데, M<sup>(1)</sup><sub>mn</sub>, M<sup>(3)</sup><sub>mn</sub>같은 식으로 표기하며, (1), (2)는 구면 베셀과 노이만 함수 j<sub>n</sub>, y<sub>n</sub>, (3), (4)는 구면 한켈 함수 h<sup>(1)</sup><sub>n</sub>, h<sup>(2)</sup><sub>n</sub>에 해당한다. 구면 베셀 함수에 대해 자세한 내용은 [여기](https://en.wikipedia.org/wiki/Bessel_function#Spherical_Bessel_functions:_jn,_yn)를 참고하자. 



### LMN 기저의 개형

![undefined](https://upload.wikimedia.org/wikipedia/commons/thumb/f/f8/VSHwiki.svg/1920px-VSHwiki.svg.png)

위의 그림에서 n=1일 때의 M, N을 보면 그래프가 dipole radiation의 형태와 유사하게 생겼다. 특히 M은 벡터가 한 방향으로 회전하고, N은 한 방향으로 나열되어 있는데, 이것이 마치 magnetic dipole, electric dipole과 유사하지 않은가? 그래서 M을 magnetic harmonics, N을 electric harmonics라고 부르며, l=1일 때 M, N에 해당하는 모드를 각각 magnetic dipole(MD), electric dipole(ED) 모드라고 부른다. n=2, 3으로 가면 함수의 형태가 더 복잡해지는데, 이건 마치 quadrupole, octupole의 방사 형태와 같다. 그래서 이 때의 모드들을 electric/magnetic quadrupole(EQ, MQ) 모드, octuple 모드, &hellip; 하는 식으로 부른다.

이런 이유로 L, M, N 기저를 이용해서 구면 좌표 위의 방정식의 해를 나타내는 것을 다중극 전개(multipole expansion)라고 한다.



### Mie 산란에서의 다중극 전개

Mie 산란에서 입사파, 산란파, 내부 전기장을 다중극 전개를 이용해서 나타낼 때 모든 함수를 사용하지는 않는다. 주로 구면 베셀 함수를 사용한 것(M<sup>(1)</sup>, N<sup>(1)</sup>)과 제 1종 구면 한켈 함수를 사용한 것(M<sup>(3)</sup>, N<sup>(3)</sup>) 중 하나를 사용한다. 어느 것을 사용하는지는 구면 베셀 함수의 성질에 따라 다르다. 평면파인 입사파와 내부 전기장의 경우 나타내는 공간에 원점이 포함되기 때문에 원점에서 발산하지 않는 구면 베셀 함수를 사용하고(M<sup>(1)</sup>, N<sup>(1)</sup>), 외부로 빠져나가는 산란파에 대해서는 한 쪽 방향으로 진행하는 성분만이 존재하는 구면 한켈 함수를 사용하게 된다(M<sup>(3)</sup>, N<sup>(3)</sup>). (구면 베셀과 노이만 함수는 정의에 sin, cos이 들어가며, 구면 한켈 함수는 j<sub>n</sub>&pm;iy<sub>n</sub>꼴이라 e<sup>&pm;ikr</sup>항이 생긴다.)