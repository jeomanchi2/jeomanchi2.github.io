---
title: "26학년도 중등 물리 임용시험 전공A"
categories:
  - physics
date: 2026-07-19
mathjax: true
toc: true
toc_sticky: true
toc_levels: 2..2
---
<iframe src="/assets/2026_A.pdf" width="100%" height="800px" style="border: none;"></iframe>

## 1번 문제

### <풀이 1> 미분형 풀이  

도체판은 $x$축과 $y$축 방향으로 무한히 넓고, 전류 밀도  $\vec J(z)=\alpha |z|\,\hat{x}$는 $z$에만 의존한다. 대칭성에 의해 자기장은 $y$축에 나란하고 $z$에만 의존하므로

$$ \vec B(z)=B_y(z)\,\hat{y} $$

로 둘 수 있다. 오른손 법칙에 따라 $z>0$에서는 $-\hat y$ 방향, $z<0$에서는 $+\hat y$ 방향이다. 또한 $z=0$에 대하여 전류 분포가 대칭이므로 $B_y(-z)=-B_y(z)$이며, 특히 $B_x=0$, $B_z=0$이다.

앙페르 법칙의 미분형으로부터 자기장$B_y$는 다음과 같다.
$$
\begin{flalign}

&\nabla \times \vec{B} = \mu_0 \vec{J} & \\\\
&\left( \cancelto{0}{\frac{\partial B_z}{\partial y}} - \frac{\partial B_y}{\partial z} \right)\hat{x} - \left( \cancelto{0}{\frac{\partial B_z}{\partial x}} - \cancelto{0}{\frac{\partial B_x}{\partial z}} \right)\hat{y} + \left( \frac{\partial B_y}{\partial x} - \cancelto{0}{\frac{\partial B_x}{\partial y}} \right)\hat{z} = & \\\\
&\left( -\frac{\partial B_y}{\partial z}, 0, \frac{\partial B_y}{\partial x} \right) = \mu_0 \vec{J}\quad \because \frac{dB_y}{dx} = \mu_0 J_x \Rightarrow \frac{dB_y}{dx} =0\\\\ 
&\quad-\frac{dB_y}{dz} = \mu_0 J_z & \\\\
&\Rightarrow\quad \frac{dB_y}{dz} = -\mu_0\alpha |z| & \\\\
&\Rightarrow\quad B_y = -\frac{1}{2}\mu_0\alpha z^2 + C \quad \because B_y(0) =0,\quad C=0 &\\\\
&\Rightarrow\quad B_y = -\frac{1}{2}\mu_0\alpha z^2 &
\end{flalign}
$$
### (1) $z=-\frac{d}{2}$에서 자기장 크기

$$
\begin{flalign}
&B_y = -\frac{1}{2}\mu_0\alpha z^2 \quad \Leftarrow z=-\frac{d}{2}&\\\\
&\boxed{B \! \left(-\frac d2\right) = \frac{\mu_0\alpha d^2}{8}} &
\end{flalign}
$$





### (2) $z=\frac{3d}{2}$에서 자기장 크기

$z>d$인 도체판 밖에서는 $J_x=0$이므로 자기장은 일정하다. 따라서 $z=3d/2$에서의 자기장은 도체판의 위쪽 표면 $z=d$에서의 자기장과 같다. 
$$
\begin{flalign}

&B_y \! \left(\frac 32d\right) =B_y \! \left(d\right)\\\\
&\Rightarrow B_y = -\frac{1}{2}\mu_0\alpha z^2 \quad \Leftarrow z=d&\\\\
&\Rightarrow\boxed{B_y= \frac{\mu_0\alpha d^2}{2}}
\end{flalign}
$$


 ### <풀이 2> 적분형 풀이

짧은 변의 길이가 $z$이고, 긴 변의 길이가 $\ell$ 직사각형 앙페르 고리를 잡는다. 적분경로를 반시계 방향으로 잡으면 위쪽과 아래쪽 긴 변에서 각각 다음과 같다.

$$ \int_{\text{위}}\vec B\cdot d\vec\ell=B(z)\ell, \qquad \int_{\text{아래}}\vec B\cdot d\vec\ell=B(z)\ell $$

왼쪽과 오른쪽 짧은변에서는 $d\vec\ell\perp\vec B$이므로 내적이 $0$이다. 따라서 앙페르 법칙의 적분형으로부터 $B$는다음과 같다.
$$
\begin{flalign}
&\oint\vec B(z)\cdot d\vec\ell =\mu_0 I_{enc}\\\\
&\int_{\text{위}}\vec B(z)\cdot d\vec\ell + \int_{\text{아래}}\vec B(z)\cdot d\vec\ell \quad+\cancelto{0}{\int_{\text{왼쪽}}\vec B(z)\cdot d\vec\ell} + \cancelto{0}{\int_{\text{오른쪽}}\vec B(z)\cdot d\vec\ell}= \mu_0 I_{enc}&\\\\
&\Rightarrow2\int\vec B(z)\cdot d\vec\ell = \mu_0 I_{enc}& \\\\
&\Rightarrow2B(z)\ell=\mu_0 I_{enc}& \\\\
&\Rightarrow B_(z)=\frac{1}{2\ell}\mu_0 I_{\mathrm{enc}}
\end{flalign}
$$
### (1) $z=\frac{d}{2}$인 경우 자기장의 세기

$0 \le z \le d$이면 앙페르 경로가 둘러싼 전류 $I_{enc}$는 다음과 같다.
$$
\begin{aligned}
I_{\mathrm{enc}} 
  &=\int J dA \\\\
  &=\int_{-z}^{z}\alpha|z|\ell \,dz \\\\
  &=2\alpha\ell\int_0^z z\,dz \\\\
  &=\alpha\ell z^2
\end{aligned}
$$
그러므로 $B(z=-\frac d2)$ 는 다음과 같다.
$$
\begin{flalign}
&B_(z)=\frac{1}{2\ell}\mu_0 I_{\mathrm{enc}} \quad \Leftarrow I_{enc}= \alpha\ell z^2& \\\\
&B(z)=\frac{\mu_0\alpha z^2}{2}\quad \Leftarrow z = -\frac d2 & \\\\
&\boxed{B(-\frac d2)=\frac{\mu_0\alpha d^2}{8}}
\end{flalign}
$$

### (2) $z=\frac{3d}{2}$인 경우 자기장의 세기

$z>d$이면 앙페르고리를 관통하는 전류 $I_{\mathrm{enc}}$는 도체판의 단면에만 존재하므로 다음과 같다.
$$
\begin{aligned}
I_{\mathrm{enc}} 
  &=\int J\,dA \\\\
  &=\int_{-d}^{d}\alpha|z|\ell\,dz \\\\
  &=2\alpha\ell\int_0^d z\,dz \\\\
  &=\alpha\ell d^2.
\end{aligned}
$$
그러므로 $B(z=\frac {3d}{2})$ 는 다음과 같다.
$$
\begin{flalign}
&B_(z)=\frac{1}{2\ell}\mu_0 I_{\mathrm{enc}} \quad \Leftarrow I_{enc}= \alpha\ell d^2& \\\\
&B(z)=\frac{\mu_0\alpha d^2}{2} & \\\\
&\boxed{B(\tfrac{3d}{2})=\frac{\mu_0\alpha d^2}{2}}
\end{flalign}
$$


## 2번 문제

고윳값을 구하라고 하였으므로 고윳값 방정식을 세운다.
$$
\begin{flalign}
&\qquad H\psi=\lambda\psi \\\\
&\Rightarrow (H-\lambda I)\psi=0 & \\\\
&\Rightarrow \det(H-\lambda I)=0 & \\\\
&\Rightarrow \begin{vmatrix}
   E_0-\lambda & i\dfrac{\sqrt3}{2}\Delta\\\\
   -i\dfrac{\sqrt3}{2}\Delta & E_\Delta+\Delta-\lambda
 \end{vmatrix} \\\\
 &\Rightarrow(E_0-\lambda)(E_0+\Delta-\lambda)-\frac34\Delta^2=0 \qquad \text{Let} \quad x \equiv E_0-\lambda&\\\\
 &\Rightarrow x^2+\Delta x-\frac34\Delta^2=0 &\\\\
 &\Rightarrow x = -\frac32 \Delta ,\quad x = \frac12 \Delta  &\\\\
 &\Rightarrow \lambda_1  = E_0 -\frac12 \Delta ,\quad \lambda_2 = E_0 + \frac32 \Delta  &\\\\
 &\Rightarrow \boxed{ |E_2 - E_1| =|\lambda_2 - \lambda_1| = 2\Delta}  &\\\\
 & E_0, \Delta > 0 이므로 E_1이 바닥상태, E_2가 첫번째 들 뜬 상태 이다. & 
\end{flalign}
$$


바닥상태 상태함수($\psi_0$)를  구하기 위하여 바닥상태 에너지 $E_0$를  고윳값 방정식에 대입하면
$$
\begin{flalign}
&\qquad H\psi_0=E_1\psi_0& \\\\
&\Rightarrow(H-E_1I)\begin{pmatrix}\alpha\\1\end{pmatrix}=0 \qquad \because \psi_0 = \alpha \begin{pmatrix}1\\0\end{pmatrix}+ \begin{pmatrix}0\\1\end{pmatrix}=\begin{pmatrix}\alpha\\1\end{pmatrix}&\\
&\Rightarrow(H-E_1I)\begin{pmatrix}\alpha\\1\end{pmatrix}=0 \qquad \because \psi_0\\
&\Rightarrow \frac{1}{\sqrt{\quad}}\begin{pmatrix}
   E_0 -E_1 & i\dfrac{\sqrt3}{2}\Delta\\
   -i\dfrac{\sqrt3}{2}\Delta & E_0+ \Delta -E_1
 \end{pmatrix}\begin{pmatrix}\alpha\\\\1\end{pmatrix}=0\\\\
\end{flalign}
$$
이다. 앞서 구한 $E_1=E_0-\frac12\Delta$로 부터 $E_0-E_1=\frac12 \Delta$이고, $E_0+ \Delta -E_1=\frac32\Delta$이므로 
$$
\begin{flalign}
&\Rightarrow \frac{1}{\sqrt{\quad}}\begin{pmatrix}
   \frac12 \Delta & i\dfrac{\sqrt3}{2}\Delta\\
   -i\dfrac{\sqrt3}{2}\Delta & \frac32 \Delta
 \end{pmatrix}\begin{pmatrix}\alpha\\\\1\end{pmatrix}=0&\\\\
\end{flalign}
$$
이다. 이 때, 1행으로부터 $\alpha$를 구하면 다음과 같다.
$$
\begin{flalign}
&\qquad \frac12 \Delta \alpha + i\dfrac{\sqrt3}{2}\Delta =0 &\\\\
&\Rightarrow \alpha = -i\sqrt3&
\end{flalign}
$$

---

## 3번 문제

(가)에서 물체A는 회전축 위의 질점이므로 회전 관성 모멘트에 기여하지 않는다. 따라서 $\frac{I}{I_0},\frac{K}{K_0}$는 다음과 같다.
$$
\begin{flalign}
&ⅰ)\quad I=\frac{1}{2}MR^2+\frac12 mr^2, \quad I_0=\frac12MR^2 &\\\\ 
&ⅱ)\quad\boxed{ \frac{I}{I_0} = \frac{MR^2+mr^2}{MR^2}} &
\end{flalign}
$$

$$
\begin{flalign}
&ⅰ) K_0 = \frac12 I_0\omega_0^2, \quad K = \frac12 I\omega^2 & \\\\
&ⅱ)\frac{K}{K_0} =\frac{I\omega^2}{I_0\omega_0^2} \quad \dots ①\\\\
&ⅲ) \text{각운동량보존}&\\ 
&\quad I_0\omega_0=I\omega \quad \dots ②&\\\\
&ⅳ) ①←② & \\
&\quad \frac{K}{K_0} =\frac{I_0}{I} & \\\\
&=\boxed{\frac{MR^2}{MR^2+mr^2}}
\end{flalign}
$$


## 4번 문제

문제상황에서 단위시간당 충돌 횟수를 구하라고 하였으므로, 1번 충돌하는데 걸리는 시간을 구하고 역수를 취해 구하도록 하자.  

알파 입자는 핵의 중심을 지나는 지름 방향으로 왕복한다고 가정하였으므로, 한쪽 핵 표면에서 $v$의 속력으로 출발하여 $2R$ 만큼 떨어진 반대쪽 핵 표면까지 도달하여 1번 충돌하는데 걸리는 시간$t$은 다음과 같다. 

$$  t=\frac{2R}{v}. $$

따라서 단위 시간당 장벽에 충돌하는 횟수는 $\frac{1}{t}$이므로, $N$은 다음과 같다.

$$ \boxed{N=\frac{1}{ t}=\frac{v}{2R}} $$



단위 시간당 투과 확률$P$은 단위시간당 충돌 횟수와 한 번의 투과 확률의 곱으로 주어진다. 즉,

$$ \boxed{ P=NT = \frac{v}{2R} \exp\!\left[ -\frac{2a\sqrt{2m(V_0-E)}}{\hbar} \right]}. $$

이다.

---

## 5번 문제 및 해설

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

문제상황에서 A공이 최고점에 도달한다고 하였으므로 $v-t$그래프를 그려보자.

이 때, 공A가 최고점에 도달하는 시간은 $t_{A}$, 공B가 이동한 거리를 $S_B$는 다음과 같다.
$$
\begin{flalign}
 &ⅰ)t_{\mathrm{A}}=\frac{v_0}{g}&\\
 &ⅱ)s_B=v_0t_{\mathrm{A}}+\frac12gt_{\mathrm{A}}^2 = \boxed{\frac{3v_0^2}{2g}}
\end{flalign}
$$


 $y=0$에 도달할 때의 공A, 공B의 속력을 각각 $v_A,$ $v_B$라 하면, 등가속도 공식 3번으로 부터 h는 다음과 같다.
$$
\begin{flalign}
&ⅰ)\quad 2gh=v_0^2 - v_A^2  \\
&\Rightarrow\quad 8gh=4v_0^2 - 4v_A^2 \dots①& \\\\

&ⅱ)\quad 2g(H-h)=v_B^2 - v_0^2 \quad\because 2v_A=v_B &\\
&\Rightarrow\quad 2gH-2gh=4v_A^2 - v_0^2 \dots② &\\\\

&ⅲ)①+②&\\
&\quad 2gH + 6gh = 3v_0^2&\\
&\Rightarrow  6gh = 3v_0^2 - 2gH &\\
&\Rightarrow \boxed{h=\frac{3v_0^2-2gH}{6g} = \frac{v_0^2}{2g}-\frac{H}{3}}& 
\end{flalign}
$$


---

## 9번 문제

자기장과 전기장의 관계는 $$ \vec B=\frac1c\hat r\times\vec E $$ 이고 $\hat r\times\hat\theta=\hat\phi$이므로, $B(\theta,t)$는 다음과 같다.
$$
\begin{flalign}
 &\quad B=\frac Ec&\\
 &\Rightarrow \boxed{\alpha\frac{I_0\sin\theta}{cR} \cos[\omega(t-t')]}&
 \end{flalign}
$$
자기장 방향은 전기장이 $\hat{\theta}$이므로 $\hat{\phi}$ 이다.

포인팅 벡터 $\vec{S}$는 전기장과 자기장의 벡터곱으로 주어진다. 따라서
$$
\begin{flalign}
\vec S(\theta,t)&=\frac1{\mu_0}\vec E\times\vec B& \\\\
   \qquad &=\frac{\alpha^2I_0^2}{\mu_0cR^2} \sin^2\theta\, \cos^2[\omega(t-t')]\,\hat r.&\\
\end{flalign}
$$
이다. 자료로 부터  $\vec{S}$의 시간평균은 다음과 같다.
$$
\begin{flalign}
<S>&=\frac{\alpha^2I_0^2}{\mu_0cR^2} \sin^2\theta\, \langle\cos^2[\omega(t-t')]\rangle\ \because \frac{1}{2\pi}\int_0^{2\pi} \cos^2x dx= \frac12& \\\\
   &=\frac{\alpha^2I_0^2}{2\mu_0cR^2} \sin^2\theta \quad &\\\\
   &\therefore \boxed{<\vec S>=\frac{\alpha^2I_0^2}{2\mu_0cR^2} \sin^2\theta \, \hat r }&
\end{flalign}
$$

## 10번 문제

문제상황에서 (가),(나) 상황에서 역학적 평형을 이루고 있으므로, 각 상황에서 세 기체의 압력은 $P_가$, $P_나$ 로 같다. 
(나)상황에서 XYZ기체의 부피를 각각  $V_X,, V_Y, V_Z$라고 할 때, $V_Y$는 이상기체 상태방정식으로부터 다음과 같다.
$$
\begin{flalign}
ⅰ)&\quad PV=NkT&\\\\
&\Rightarrow V_Y=\frac{ N_Yk8T_0}{p_나} \dots ① \\\\

\end{flalign}
$$
X, Y, Z 기체의 분자 수를 각각 $N, N_Y, N_Z$라 하면 다음과 같다.
$$
\begin{flalign}

ⅱ) &N_=\frac{p_가V_0}{kT_0}, \quad N_Y=\frac{p_가V_0}{k(2T_0)}=\frac N2, \qquad N_Z=\frac{p_가V_0}{kT_0}=N \dots ② &\\\\
ⅲ) &V_X=\frac{68NkT_0}{p_나},\quad V_Y=\frac{4NkT_0}{p_나},\quad V_Z=\frac{24NkT_0}{p_나} \dots ③ &

\end{flalign}
$$
실린더의 전체 부피로 부터 $P_나$ 는 다음과 같다.

$$
\begin{flalign}
ⅳ)& 3V_0=V_X+V_Y+V_Z =\frac{96NkT_0}{p_나}&\\
&\Rightarrow \quad \boxed{p_나=\frac{32NkT_0}{V_0}}\dots ④&\\
\end{flalign}
$$
$V_Y$는 다음과 같다.
$$
\begin{flalign}
Ⅴ)& ①←②,④\\
& \boxed{V_Y=\frac{V_0}{8}} \dots ⑤&
\end{flalign}
$$


전체 실린더는 단열되고 전체 부피가 고정되어 있으므로 외부로 한 일은 $0$이다. 그러니 각각의 기체가 한 일은 고려할 필요가 없다.(가)상황 내부에내지를 $U$, (나)상황 내부에너지를 $U'$ 이라고 할 때, 전체 계에 가해진 열은

$$
\begin{flalign}
Ⅵ)& Q_1+Q_2=\Delta U_{tot} = U'_{tot}-U_{tot} \dots ⑥&\\\\
\end{flalign}
$$

$$
\begin{flalign}
Ⅶ) U_{tot}&=U_{X}+U_{Y}+U_{Z}&\\
&=\frac32NkT_0 +\frac32\frac N2k(2T_0) +\frac32NkT_0 \\
&=\frac92NkT_0 \dots ⑦&\\ 
\end{flalign}
$$

$$
\begin{flalign}
Ⅷ)U'&=\frac32Nk(68T_0) +\frac32\frac N2k(8T_0) +\frac32Nk(24T_0)&\\\\
   &=144NkT_0 \dots ⑧&
\end{flalign}
$$

$$
\begin{flalign}
Ⅸ)&⑥←⑦,⑧&\\
& \boxed{Q_1+Q_2 = \frac{279}{2} NkT_0} &\\\\
   \end{flalign}
$$

---

## 11번 문제

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

$$
\begin{aligned}
v(t_1) 
  &=-3A\omega\sin\frac{3\pi}{2} +\frac{A\omega}{8}\cos\frac\pi2 \\\\
  &=\boxed{3A\omega}.
\end{aligned}
$$

$$
\begin{aligned}
|0'\rangle 
  &=|0\rangle+ \frac{H'_{10}}{E_0-E_1}|1\rangle \\\\
  &=\boxed{|0\rangle+ \frac{e\alpha}{\sqrt{2m\hbar\omega^3}}|1\rangle}.
\end{aligned}

---

## 12번 문제

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
