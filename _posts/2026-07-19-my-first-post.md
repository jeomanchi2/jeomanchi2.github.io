---
title: "포스트 제목"
date: 2026-07-19
mathjax: true
---
<!-- embed 태그를 사용하는 방법 -->
<embed src="assets/2026_A.pdf" type="application/pdf" width="100%" height="800px" />


## 1번 문제

<!-- 2026_중등1차_물리_전공A.pdf 1페이지 이미지 삽입 위치 -->
<!-- ![1번 문제 이미지](/assets/images/problem1.jpg) -->

### <풀이 1> 미분형 풀이

도체판은 $x$축과 $y$축 방향으로 무한히 넓고, 전류 밀도

$$ \vec J(z)=\alpha |z|\,\hat{x} $$

는 $z$에만 의존한다. 대칭성에 의해 자기장은 $y$축에 나란하고 $z$에만 의존하므로

$$ \vec B(z)=B_y(z)\,\hat{y} $$

로 둘 수 있다. 오른손 법칙에 따라 $z>0$에서는 $-\hat y$ 방향, $z<0$에서는 $+\hat y$ 방향이다. 또한 $z=0$에 대하여 전류 분포가 대칭이므로 $B_y(-z)=-B_y(z)$이며, 특히 $B_y(0)=0$이다.

앙페르 법칙의 미분형

$$ \nabla\times\vec B=\mu_0\vec J $$

에서 $x$성분을 비교하면

$$ -\frac{dB_y}{dz}=\mu_0 J_x \quad\Longrightarrow\quad \frac{dB_y}{dz}=-\mu_0\alpha |z| $$

을 얻는다.

### (1) $z=-\frac{d}{2}$에서

$-d \le z \le 0$에서는 $|z|=-z$이므로

$$ \frac{dB_y}{dz}=\mu_0\alpha z. $$

$B_y(0)=0$을 이용하여 적분하면

$$ B_y(z)=\frac{\mu_0\alpha}{2}z^2. $$

따라서

$$ \vec B\!\left(-\frac d2\right) = \frac{\mu_0\alpha d^2}{8}\,\hat y. $$

$$ \boxed{\left|\vec B\!\left(-\frac d2\right)\right| = \frac{\mu_0\alpha d^2}{8}}. $$

### (2) $z=\frac{3d}{2}$에서

$z>d$인 도체판 밖에서는 $J_x=0$이므로 자기장은 일정하다. 따라서 $z=3d/2$에서의 자기장은 도체판의 위쪽 표면 $z=d$에서의 자기장과 같다. $0 \le z \le d$에서는 $|z|=z$이므로

$$ B_y(d)-B_y(0) = -\mu_0\alpha\int_0^d z\,dz = -\frac{\mu_0\alpha d^2}{2}. $$

그러므로

$$ \vec B\!\left(\frac{3d}{2}\right) = -\frac{\mu_0\alpha d^2}{2}\,\hat y. $$

$$ \boxed{\left|\vec B\!\left(\frac{3d}{2}\right)\right| = \frac{\mu_0\alpha d^2}{2}}. $$

따라서 요구한 자기장의 크기는 순서대로

$$ \boxed{\frac{\mu_0\alpha d^2}{8}}, \qquad \boxed{\frac{\mu_0\alpha d^2}{2}} $$

이다.

### <풀이 2> 적분형 풀이

<!-- 직사각형 앙페르 경로의 모식도(TikZ) 이미지 삽입 위치 -->
<!-- ![앙페르 경로 모식도](/assets/images/ampere_path.jpg) -->
*직사각형 앙페르 경로의 모식도(그림은 $a>d$인 경우)*

$z=\pm a$에 놓인 두 긴 변의 길이가 $\ell$이고, 긴 변이 $y$축에 나란한 직사각형 앙페르 고리를 잡는다. 경로를 그림의 화살표 방향으로 잡으면 위쪽과 아래쪽 긴 변에서 각각

$$ \int_{\text{위}}\vec B\cdot d\vec\ell=B(a)\ell, \qquad \int_{\text{아래}}\vec B\cdot d\vec\ell=B(a)\ell $$

이다. 왼쪽과 오른쪽 변에서는 $d\vec\ell\perp\vec B$이므로 선적분이 $0$이다. 따라서 앙페르 법칙의 적분형으로부터 

$$ 
\begin{aligned}
\oint\vec B(a)\cdot d\vec\ell 
&=\int_{\text{위}}\vec B(a)\cdot d\vec\ell + \int_{\text{아래}}\vec B(a)\cdot d\vec\ell \\\\
&\quad+\cancelto{0}{\int_{\text{왼쪽}}\vec B(a)\cdot d\vec\ell} + \cancelto{0}{\int_{\text{오른쪽}}\vec B(a)\cdot d\vec\ell} \\\\
&=2\int\vec B(a)\cdot d\vec\ell \\\\
&=2B(a)\ell \\\\
&=\mu_0 I_{\mathrm{enc}}
\end{aligned}
$$

이 된다.

### (1) $a=\frac{d}{2}$인 경우

$0 \le a \le d$이면 앙페르 경로가 둘러싼 전류는

$$ 
\begin{aligned}
I_{\mathrm{enc}} 
  &=\int J dA \\\\
  &=\int_{-a}^{a}\alpha|z|\ell \,dz \\\\
  &=2\alpha\ell\int_0^a z\,dz \\\\
  &=\alpha\ell a^2
\end{aligned}
$$

그러므로

$$ 
\begin{aligned}
2B(a)\ell 
  &=\mu_0 I_{\mathrm{enc}} \\\\
  &=\mu_0\alpha\ell a^2, \\\\
B(a)&=\frac{\mu_0\alpha a^2}{2}.
\end{aligned}
$$

$a=d/2$를 대입하면

$$ \boxed{\left|\vec B\!\left(-\frac d2\right)\right| = \frac{\mu_0\alpha d^2}{8}}. $$

### (2) $a=\frac{3d}{2}$인 경우

$a>d$이면 앙페르고리를 관통하는 전류 $I_{\mathrm{enc}}$는 도체판의 단면에만 존재하므로

$$ 
\begin{aligned}
I_{\mathrm{enc}} 
  &=\int J\,dA \\\\
  &=\int_{-d}^{d}\alpha|z|\ell\,dz \\\\
  &=2\alpha\ell\int_0^d z\,dz \\\\
  &=\alpha\ell d^2.
\end{aligned}
$$

따라서

$$ 
\begin{aligned}
2B(a)\ell 
  &=\mu_0 I_{\mathrm{enc}} \\\\
  &=\mu_0\alpha\ell d^2.
\end{aligned}
$$

그러므로

$$ \boxed{\left|\vec B\!\left(\frac{3d}{2}\right)\right| = \frac{\mu_0\alpha d^2}{2}}. $$

---

## 2번 문제

<!-- 2번 문제 이미지 삽입 위치 -->

### <풀이> 고윳값 차이

해밀토니언에서 $E_0 I$를 빼고 $\Delta$로 나눈 무차원 행렬을

$$ 
A=\frac{H-E_0I}{\Delta} 
=\begin{pmatrix}
  0 & i\dfrac{\sqrt3}{2}\\\\[2pt]
  -i\dfrac{\sqrt3}{2} & 1
\end{pmatrix}
$$

로 둔다. $A$의 고윳값을 $\lambda$라고 하면

$$ 
\begin{aligned}
0&=\det(A-\lambda I) \\\\
 &=\begin{vmatrix}
   -\lambda & i\dfrac{\sqrt3}{2}\\\\[2pt]
   -i\dfrac{\sqrt3}{2} & 1-\lambda
 \end{vmatrix} \\\\
 &=\lambda^2-\lambda-\frac34 \\\\
 &=\left(\lambda+\frac12\right)\left(\lambda-\frac32\right).
\end{aligned}
$$

따라서

$$ \lambda_1=-\frac12, \qquad \lambda_2=\frac32 $$

이고, $H$의 두 고윳값은

$$ E_1=E_0-\frac{\Delta}{2}, \qquad E_2=E_0+\frac{3\Delta}{2} $$

이다. 그러므로 두 고윳값의 차이는

$$ \boxed{|E_2-E_1|=2\Delta}. $$

### 바닥상태와 $\alpha$

$\Delta>0$이므로 바닥상태의 에너지는

$$ E_1=E_0-\frac{\Delta}{2} $$

이다. 문제에 제시된 바닥상태의 계수 벡터는

$$ \begin{pmatrix}\alpha\\\\1\end{pmatrix} $$

에 비례한다. 바닥상태 고유값 방정식

$$ (H-E_1I)\begin{pmatrix}\alpha\\\\1\end{pmatrix}=0 $$

에서

$$ 
H-E_1I 
=\Delta 
\begin{pmatrix}
  \dfrac12 & i\dfrac{\sqrt3}{2}\\\\[2pt]
  -i\dfrac{\sqrt3}{2} & \dfrac32
\end{pmatrix}
$$

이므로 첫째 행을 이용하면

$$ \frac12\alpha+i\frac{\sqrt3}{2}=0. $$

따라서

$$ \boxed{\alpha=-i\sqrt3}. $$

실제로 $|\alpha|^2=3$이므로 규격화 인자는

$$ \frac{1}{\sqrt{1+|\alpha|^2}}=\frac12 $$

이고, 규격화된 바닥상태는

$$ \boxed{ |E_1\rangle =\frac12\left(-i\sqrt3\,|0\rangle+|1\rangle\right) }. $$

---

## 3번 문제

<!-- 3번 문제 이미지 삽입 위치 -->

### <풀이> 회전 관성과 각운동량 보존

(가)에서 물체 A는 회전축 위의 질점이므로 회전 관성 모멘트에 기여하지 않는다. 따라서

$$ I_0=\frac12MR^2, \qquad K_0=\frac12I_0\omega_0^2. $$

(나)에서 A는 질량 $m$, 반지름 $r$인 원판이므로

$$ I=\frac12MR^2+\frac12mr^2. $$

이에 따라

$$ \boxed{\frac{I}{I_0} = \frac{MR^2+mr^2}{MR^2} = 1+\frac{mr^2}{MR^2}}. $$

외부 알짜 토크가 $0$이므로 각운동량이 보존되어

$$ I_0\omega_0=I\omega \quad\Longrightarrow\quad \omega=\frac{I_0}{I}\omega_0. $$

따라서 운동 에너지의 비는

$$ 
\begin{aligned}
\frac{K}{K_0} 
&=\frac{I\omega^2}{I_0\omega_0^2} 
 =\frac{I_0}{I} \\\\
&=\boxed{\frac{MR^2}{MR^2+mr^2}}.
\end{aligned}
$$

즉, 원판 A가 펼쳐지면서 회전 관성 모멘트는 증가하고, 각운동량은 보존되지만 회전 운동 에너지는 감소한다.

---

## 4번 문제

<!-- 4번 문제 이미지 삽입 위치 -->

### <풀이> 장벽 충돌 횟수와 투과 확률

알파 입자는 핵의 중심을 지나는 지름 방향으로 왕복한다. 한쪽 핵 표면에서 반대쪽 핵 표면까지의 거리는 $2R$이므로 장벽과 연속해서 충돌하는 데 걸리는 시간은

$$ \Delta t=\frac{2R}{v}. $$

따라서 단위 시간당 장벽에 충돌하는 횟수는

$$ \boxed{N=\frac{1}{\Delta t}=\frac{v}{2R}}. $$

장벽에 한 번 충돌할 때의 투과 확률이

$$ T=\exp\!\left[ -\frac{2\sqrt{2m(V_0-E)}}{\hbar}a \right] $$

이므로 단위 시간당 투과 확률은 충돌 횟수와 한 번의 투과 확률의 곱으로 주어진다. 즉,

$$ \boxed{ P=NT = \frac{v}{2R} \exp\!\left[ -\frac{2a\sqrt{2m(V_0-E)}}{\hbar} \right]}. $$

$\hbar=h/(2\pi)$를 이용하면 같은 결과를

$$ \boxed{ P=\frac{v}{2R} \exp\!\left[ -\frac{4\pi a}{h}\sqrt{2m(V_0-E)} \right]} $$

로도 쓸 수 있다.

---

## 5번 문제 및 해설

<!-- 5번 문제 이미지 삽입 위치 -->

### ㉠ 과학적 사고의 유형

$$ \boxed{\text{귀추적 사고}} $$

뉴턴은 "프리즘을 통과한 빛이 길쭉한 색 띠를 만든다"라는 뜻밖의 관찰을 설명하기 위해, 테니스 라켓에 맞은 공의 진로가 꺾이는 유사 사례를 끌어와 "프리즘이 빛의 진행 방향을 꺾기 때문일 것이다"라는 잠정적 설명 가설을 세웠다. 관찰 사실과 유사 사례로부터 가능한 원인을 추론하였으므로 귀추적 사고이다.

### ㉡ 길쭉한 스펙트럼이 생기는 이유

백색광은 굴절 정도가 서로 다른 여러 색의 빛으로 이루어져 있다. 첫 번째 프리즘에서 분리된 빨간색 빛과 파란색 빛을 두 번째 프리즘에 각각 입사시키면 두 빛의 진행 방향이 서로 다르게 꺾인다. 일반적으로 파란색 빛이 빨간색 빛보다 더 크게 굴절하므로 각 색이 서로 다른 위치에 도달하고, 그 결과 스크린에 길쭉한 스펙트럼이 나타난다.

### ㉢ 반증하려 한 기존의 생각

뉴턴이 반증하려 한 생각은

$$ \boxed{\text{백색광은 순수하고 균질한 단일한 빛이다}} $$

라는 당시의 관점이다. 이 관점에서는 여러 색이 프리즘에 의해 새롭게 덧입혀진다고 보았다. 그러나 첫 번째 프리즘은 백색광을 여러 색으로 분리하고, 두 번째 프리즘에 한 색만 입사시키면 그 색은 다시 다른 색으로 변하지 않으면서 그 색에 고유한 정도로 굴절한다. 따라서 색은 프리즘이 만든 것이 아니라 백색광에 이미 포함되어 있으며, 각 색은 고유한 굴절성을 가진다.

### 답안 요약

1. **㉠ 귀추적 사고:** 관찰한 이상 현상을 유사 사례로 설명하는 잠정적 가설을 세웠다.
2. **㉡** 색마다 굴절 정도가 달라 서로 다른 위치에 도달하므로 길쭉한 스펙트럼이 생긴다.
3. **㉢** 백색광이 순수하고 균질한 빛이라는 생각을 반증하였다.

---

## 6번 문제 및 해설

<!-- 6번 문제 이미지 삽입 위치 -->

### ㉠과 ㉡에 나타난 실험의 역할

두 사례에서 실험은 제안된 과학적 가설이나 이론을 경험적으로 검증하고, 그 결과를 근거로 과학 지식을 수용하도록 하는 역할을 한다. 즉,

$$ \boxed{\text{가설ㆍ이론의 검증과 과학 지식의 수용}} $$

이 공통적인 역할이다.

사례로 페랭은 물 분자의 크기를 측정하는 실험에 성공하였다. 이 결과는 원자ㆍ분자의 실재를 뒷받침하는 증거가 되어, 그때까지 원자의 존재를 거부하던 과학자들이 원자론을 받아들이는 데 기여하였다. 보어의 경우에도 수소 스펙트럼의 기존 자료를 설명하고 새 계열을 예측하여 실험으로 확인함으로써 양자화 가설이 수용되었다.

### (다)의 결정적 실험

결정적 실험은

$$ \boxed{\text{아스페의 얽힌 광자쌍에 대한 벨 부등식 검증 실험}} $$

이다. 아스페의 실험에서는 벨 부등식이 성립하지 않았으며, 측정값은 양자 역학의 예측과 거의 일치하였다. 따라서 숨은 변수를 가정한 국소적 결정론의 예측은 반증되고, 양자 역학이 예측하는 비국소적 상관관계가 지지되었다.

이 실험은 서로 양립할 수 없는 두 설명, 즉 벨 부등식을 만족하는 숨은 변수 결정론과 벨 부등식을 위반하는 양자론 사이에서 실제 측정 결과를 통해 양자론을 선택하게 하였으므로 결정적 실험에 해당한다. 또한 자료에 따르면 벨의 정리를 처음으로 완전하게 검증한 실험이라는 점도 그 근거가 된다.

---

## 7번 문제 해설

<!-- 7번 문제 이미지 삽입 위치 -->

### ㉠ 수업 모형

$$ \boxed{\text{서술적 순환학습 모형}} $$

탐색 단계에서 학생들은 교사가 먼저 개념이나 가설을 제시하지 않은 상태에서 렌즈와 물체 사이의 거리를 바꾸며 상을 관찰하고, 관찰 결과로부터 규칙성을 귀납적으로 발견한다. 이어 용어 도입 단계에서 발견한 규칙성을 발표하고 교사가 "초점", "실상"의 용어를 도입하므로 서술적 순환학습 모형에 해당한다.

### ㉡ 복합 렌즈 적용의 적절성

$$ \boxed{\text{부적절하다.}} $$

2022 개정 과학과 교육과정의 "물리학"에서는 단일 볼록 렌즈에 의해 상이 맺히는 과정과 초점ㆍ상의 관계를 다룬다. 복합 렌즈에 의한 상 맺기 원리는 해당 성취기준의 내용 범위를 벗어나므로, 학습 주제 1의 적용 단계에서 다루는 것은 적절하지 않다.

### ㉢ 초점 거리를 알아내는 방법

볼록 렌즈를 태양이나 충분히 먼 물체를 향하게 하고 렌즈 뒤에 스크린을 둔다. 스크린을 이동하여 가장 작고 선명한 상이 생기는 위치를 찾는다. 먼 물체에서 오는 빛은 거의 평행광이므로 이때의 렌즈와 스크린 사이의 거리가 초점 거리이다.

---

## 8번 문제

<!-- 8번 문제 이미지 삽입 위치 -->

### <풀이>

위쪽을 $+y$ 방향으로 잡으면

$$ y_A=v_0t-\frac12gt^2, \qquad y_B=H-v_0t-\frac12gt^2. $$

### A가 최고점에 도달하는 동안 B의 이동 거리

A가 최고점에 도달하는 시간은

$$ t_{\mathrm{top}}=\frac{v_0}{g} $$

이다. 이 시간 동안 B가 아래쪽으로 이동한 거리는

$$ s_B=v_0t_{\mathrm{top}}+\frac12gt_{\mathrm{top}}^2 = \boxed{\frac{3v_0^2}{2g}}. $$

### B가 $y=0$에 도달할 때의 속력

등가속도 관계식으로

$$ v_B^2=v_0^2+2gH $$

이므로 속력은

$$ \boxed{v_B=\sqrt{v_0^2+2gH}}. $$

### $y=h$에서의 속력 조건

각 물체가 $y=h$를 지날 때의 속력은

$$ v_A^2=v_0^2-2gh, \qquad v_B^2=v_0^2+2g(H-h). $$

$v_A=\frac12v_B$를 제곱하여 대입하면

$$ v_0^2-2gh = \frac14\{v_0^2+2g(H-h)\}. $$

따라서

$$ 4v_0^2-8gh = v_0^2+2gH-2gh $$

이고,

$$ \boxed{h=\frac{3v_0^2-2gH}{6g} = \frac{v_0^2}{2g}-\frac{H}{3}}. $$

---

## 9번 문제

<!-- 9번 문제 이미지 삽입 위치 -->

### <풀이> 자기장

점 P에서 전자기파는 $\hat r$ 방향으로 진행하고 전기장은 $\hat\theta$ 방향이다. 평면파에서

$$ \vec B=\frac1c\hat r\times\vec E $$

이고 $\hat r\times\hat\theta=\hat\phi$이므로

$$ \boxed{ \vec B(\theta,t)= \alpha\frac{I_0\sin\theta}{cR} \cos[\omega(t-t')]\,\hat\phi}. $$

따라서 자기장의 크기는 $|\vec E|/c$이고, 코사인 값이 양수일 때 $+\hat\phi$, 음수일 때 $-\hat\phi$ 방향이다.

### 포인팅 벡터와 시간평균

$$ 
\begin{aligned}
\vec S(\theta,t) 
  &=\frac1{\mu_0}\vec E\times\vec B \\\\
  &=\frac{\alpha^2I_0^2}{\mu_0cR^2} \sin^2\theta\, \cos^2[\omega(t-t')]\,\hat r.
\end{aligned}
$$

주기는 $T=2\pi/\omega$이고, 한 주기 동안 $\langle\cos^2\rangle=1/2$이므로

$$ \boxed{ \langle\vec S(\theta,t)\rangle = \frac{\alpha^2I_0^2}{2\mu_0cR^2} \sin^2\theta\,\hat r}. $$

시간 지연 $t'$은 위상만 이동시키므로 한 주기 시간평균에는 영향을 주지 않는다.

---

## 10번 문제

<!-- 10번 문제 이미지 삽입 위치 -->

### <풀이> 초기 분자 수

(가)에서 세 기체의 압력은 같으며

$$ p_0=\frac{NkT_0}{V_0}. $$

따라서 Y와 Z의 분자 수를 각각 $N_Y, N_Z$라 하면

$$ N_Y=\frac{p_0V_0}{k(2T_0)}=\frac N2, \qquad N_Z=\frac{p_0V_0}{kT_0}=N. $$

### (나)에서 Y의 부피와 압력

최종 공통 압력을 $p_f$라 하면 이상 기체 상태방정식으로

$$ V_X=\frac{68NkT_0}{p_f},\quad V_Y=\frac{4NkT_0}{p_f},\quad V_Z=\frac{24NkT_0}{p_f}. $$

실린더의 전체 부피는 일정하므로

$$ 3V_0=V_X+V_Y+V_Z =\frac{96NkT_0}{p_f}. $$

따라서

$$ \boxed{p_f=\frac{32NkT_0}{V_0}}, \qquad \boxed{V_Y=\frac{V_0}{8}}. $$

### $Q_1+Q_2$

전체 실린더는 단열되고 전체 부피가 고정되어 있으므로 외부로 한 일은 $0$이다. Y에는 열이 직접 공급되지 않으므로 전체 계에 가해진 열은

$$ Q_1+Q_2=\Delta U_X+\Delta U_Y+\Delta U_Z $$

이다. 단원자 이상 기체의 내부 에너지는 $U=\frac32N_ikT$이므로 초기 내부 에너지는

$$ U_i=\frac32NkT_0 +\frac32\frac N2k(2T_0) +\frac32NkT_0 =\frac92NkT_0. $$

최종 내부 에너지는

$$ 
\begin{aligned}
U_f&=\frac32Nk(68T_0) +\frac32\frac N2k(8T_0) +\frac32Nk(24T_0)\\\\
   &=144NkT_0.
\end{aligned}
$$

그러므로

$$ \boxed{Q_1+Q_2=U_f-U_i = \frac{279}{2}NkT_0}. $$

---

## 11번 문제

<!-- 11번 문제 이미지 삽입 위치 -->

### <풀이> 운동 방정식

뉴턴 운동 법칙과 $k=9m\omega^2$을 이용하면

$$ m\ddot x+kx=m\omega^2A\sin(\omega t) $$

이므로

$$ \ddot x+9\omega^2x=\omega^2A\sin(\omega t). $$

특수해를 $x_p=C\sin(\omega t)$로 두면

$$ (-\omega^2+9\omega^2)C=\omega^2A $$

이므로

$$ C=\frac A8, \qquad x_p=\frac A8\sin(\omega t). $$

동차방정식의 해를 더하면 일반해는

$$ x(t)=C_1\cos(3\omega t)+C_2\sin(3\omega t) +\frac A8\sin(\omega t). $$

초기 조건 $x(0)=A$로부터 $C_1=A$이다. 속도는

$$ v(t)=-3\omega C_1\sin(3\omega t) +3\omega C_2\cos(3\omega t) +\frac{A\omega}{8}\cos(\omega t) $$

이고, $v(0)=A\omega/8$을 대입하면 $C_2=0$이다. 따라서

$$ \boxed{x(t)=A\cos(3\omega t)+\frac A8\sin(\omega t)}. $$

$t_1=\pi/(2\omega)$에서

$$ \boxed{x(t_1)=\frac A8} $$

이고,

$$ 
\begin{aligned}
v(t_1) 
  &=-3A\omega\sin\frac{3\pi}{2} +\frac{A\omega}{8}\cos\frac\pi2 \\\\
  &=\boxed{3A\omega}.
\end{aligned}
$$

---

## 12번 문제

<!-- 12번 문제 이미지 삽입 위치 -->

### <풀이> 위치 연산자와 행렬 원소

주어진 소멸 연산자와 생성 연산자를 이용하면

$$ \hat x=\sqrt{\frac{\hbar}{2m\omega}} (\hat a+\hat a^\dagger). $$

따라서

$$ \langle n|\hat x|0\rangle =\sqrt{\frac{\hbar}{2m\omega}}\,\delta_{n1} $$

이고, 섭동 해밀토니언의 행렬 원소는

$$ H'_{10}=\langle1|\hat H'|0\rangle =-e\alpha\sqrt{\frac{\hbar}{2m\omega}}. $$

또한

$$ E_0-E_1=-\hbar\omega. $$

### 1차 섭동 함수

$n=1$인 항만 남으므로

$$ 
\begin{aligned}
|0'\rangle 
  &=|0\rangle+ \frac{H'_{10}}{E_0-E_1}|1\rangle \\\\
  &=\boxed{|0\rangle+ \frac{e\alpha}{\sqrt{2m\hbar\omega^3}}|1\rangle}.
\end{aligned}
$$

편의를 위해

$$ \beta=\frac{e\alpha}{\sqrt{2m\hbar\omega^3}} $$

로 두면 $|0'\rangle=|0\rangle+\beta|1\rangle$이다.

### $\langle0|\hat H'|0'\rangle$

$$ 
\begin{aligned}
\langle0|\hat H'|0'\rangle 
  &=\beta\langle0|\hat H'|1\rangle \\\\
  &=-\beta e\alpha \sqrt{\frac{\hbar}{2m\omega}} \\\\
  &=\boxed{-\frac{e^2\alpha^2}{2m\omega^2}}.
\end{aligned}
$$

### $\langle0'|\hat x|0'\rangle$

$\langle0|\hat x|0\rangle=\langle1|\hat x|1\rangle=0$이고

$$ \langle0|\hat x|1\rangle =\langle1|\hat x|0\rangle =\sqrt{\frac{\hbar}{2m\omega}} $$

이므로

$$ 
\begin{aligned}
\langle0'|\hat x|0'\rangle 
  &=2\beta\sqrt{\frac{\hbar}{2m\omega}} \\\\
  &=\boxed{\frac{e\alpha}{m\omega^2}}.
\end{aligned}
$$

이는 전기장에 의해 조화 퍼텐셜의 평형 위치가 $e\alpha/(m\omega^2)$만큼 이동한다는 결과와도 일치한다.
