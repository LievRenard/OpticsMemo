# Cauchy Principal Value



우리가 정적분을 할 때, 만약 함수가 발산하는 점이 있다면 이것을 어떻게 다룰 것인가? 이것을 다루기 위한 적분 방법이 바로 코시 주요값(Cauchy principal value)이다. 코시의 주요값은 적분 구간의 특이점 주위를 대칭적으로 잘라내어 극한을 취해 만든다. 예를 들어, 적분 구간이 [a,c]라고 하고, 함수 f(x)가 a < b < c인 b에서 발산한다고 해보자. 그러면, 이 적분에 대한 코시 주요값은
$$
\mathcal{P}\int_a^cf(x)dx=\lim_{\epsilon\rarr 0^+}\bigg[\int_a^{b-\epsilon}f(x)dx + \int_{b+\epsilon}^cf(x)dx \bigg]
$$
로써 나타낸다.



### 소호츠키-플레멜 정리

물리학에서 코시 주요값이 자주 쓰이는 관계식 중 하나는 아래와 같은 것이다.
$$
\lim_{\epsilon\rarr 0^+}\frac1{x\pm i\epsilon}=\mp i\pi\delta(x)+\mathcal{P}\bigg(\frac1x\bigg)
$$
이 관계식을 소호츠키-플레멜(Sokhotski-Plemelj) 정리라고 부른다. 이것의 다른 버전으로는 아래와 같은 것이 있으며,
$$
\lim_{\epsilon\rarr 0^+}\bigg[\frac1{x-i\epsilon}-\frac1{x+i\epsilon}\bigg]=2\pi i\delta(x)
$$
위의 두 식에 각각 적분을 취하면 다음과 같이 만들 수 있다.
$$
\lim_{\epsilon\rarr 0^+}\int_a^b\frac{f(x)}{x\pm i\epsilon}dx=\mp i\pi f(0)+\mathcal{P}\int_a^b\frac{f(x)}xdx \\
\lim_{\epsilon\rarr 0^+}\int_a^b\bigg[\frac{f(x)}{x-i\epsilon}-\frac{f(x)}{x+i\epsilon}\bigg]dx=2\pi if(0)
$$


### 크라머스-크로니히 관계식

허수부가 양수인 어떤 해석적인(무한히 미분 가능한, 또는 테일러 급수로 표현 가능한) 함수 &chi;가 &chi;(&omega;) = &chi;<sub>1</sub>(&omega;)+i&chi;<sub>2</sub>(&omega;)로 정의된다고 하자. 이때 &chi;<sub>1</sub>,  &chi;<sub>2</sub>, &omega;는 실수이고, |&omega;|가 무한으로 가면 함수가 0으로 수렴한다고 하자. 그러면 이 함수의 허수부와 실수부 사이의 아래와 같은 관계식을 크라머스-크로니히 관계식(Kramers-Kronig relation)이라고 한다.
$$
\chi_1(\omega)=\frac1\pi\mathcal{P}\int_{-\infin}^\infin\frac{\chi_2(\omega')}{\omega'-\omega}d\omega' \\
\chi_2(\omega)=-\frac1\pi\mathcal{P}\int_{-\infin}^\infin\frac{\chi_1(\omega')}{\omega'-\omega}d\omega'
$$
또는, 보통의 물리적인 상황에서는 &chi;(-&omega;) = &chi;*(&omega;)를 만족하며, 이 때 &omega;가 양수로만 한정되어
$$
\chi_1(\omega)=\frac2\pi\mathcal{P}\int_0^\infin\frac{\omega'\chi_2(\omega')}{\omega'^2-\omega^2}d\omega' \\
\chi_2(\omega)=-\frac{2\omega}\pi\mathcal{P}\int_0^\infin\frac{\chi_1(\omega')}{\omega'^2-\omega^2}d\omega'
$$
가 된다. 이런 관계를 만족하는 물리량으로는 굴절률(n과 k), 유전율(ε의 실수부와 허수부) 등이 있다. (다만, 이러한 관계는 에너지 이득이 없는 선형 매질에서만 만족한다.)

이와 유사하게, 어떤 물리량
$$
H(\omega)=e^{\alpha(\omega)+i\phi(\omega)}
$$
의 세기 α(ω)와 위상 φ(ω) 사이에는 아래와 같은 관계가 만족하며,
$$
\phi(\omega)=-\mathcal{H}\{\alpha(\omega)\} \\
\alpha(\omega)=\alpha(\infin)+\mathcal{H}\{\phi(\omega)\}
$$
여기서 힐베르트 변환 H는
$$
\mathcal{H}\{u(t)\}=\frac1\pi\mathcal{P}\int_{-\infin}^\infin\frac{u(\tau)}{t-\tau}d\tau
$$
로 정의된다.