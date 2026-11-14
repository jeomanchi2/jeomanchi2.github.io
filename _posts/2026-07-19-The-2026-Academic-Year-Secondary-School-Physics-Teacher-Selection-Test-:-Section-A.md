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

<div class="exam-sticky-layout">
  <!-- 왼쪽 여백에 고정될 문제 PDF 영역 -->
  <div class="sticky-problem-area">
    <iframe src="/assets/2026_A.pdf" width="100%" height="800px" style="border: none;"></iframe>
  </div>

  <!-- 우측에 스크롤되며 풀이를 읽을 본문 영역 -->
  <div class="scroll-content-area" markdown="1">

## 1번 문제

### <풀이 1> 미분형 풀이  
도체판은 $x$축과 $y$축 방향으로 무한히 넓고, 전류 밀도  $\vec J(z)=\alpha \vert{}z\vert{}\,\hat{x}$는 $z$에만 의존한다. 대칭성에 의해 자기장은 $y$축에 나란하고 $z$에만 의존하므로

$$\vec B(z)=B_y(z)\,\hat{y}$$

로 둘 수 있다. 오른손 법칙에 따라 $z>0$에서는 $-\hat y$ 방향, $z<0$에서는 $+\hat y$ 방향이다. 또한 $z=0$에 대하여 전류 분포가 대칭이므로 $B_y(-z)=-B_y(z)$이며, 특히 $B_x=0$, $B_z=0$이다.

앙페르 법칙의 미분형으로부터 자기장$B_y$는 다음과 같다.
앙페르 법칙의 미분형으로부터 자기장 $B_y$ 는 다음과 같다.

$$ \begin{flalign} &\nabla \times \vec{B} = \mu_0 \vec{J} & \\\\ &\left( \cancelto{0}{\frac{\partial B_z}{\partial y}} - \frac{\partial B_y}{\partial z} \right)\hat{x} - \left( \cancelto{0}{\frac{\partial B_z}{\partial x}} - \cancelto{0}{\frac{\partial B_x}{\partial z}} \right)\hat{y} + \left( \frac{\partial B_y}{\partial x} - \cancelto{0}{\frac{\partial B_x}{\partial y}} \right)\hat{z} = & \\\\ &\left( -\frac{\partial B_y}{\partial z}, 0, \frac{\partial B_y}{\partial x} \right) = \mu_0 \vec{J}\quad \because \frac{dB_y}{dx} = \mu_0 J_x \Rightarrow \frac{dB_y}{dx} =0\\\\  &\quad-\frac{dB_y}{dz} = \mu_0 J_z & \\\\ &\Rightarrow\quad \frac{dB_y}{dz} = -\mu_0\alpha \vert{}z\vert{} & \\\\ &\Rightarrow\quad B_y = -\frac{1}{2}\mu_0\alpha z^2 + C \quad \because B_y(0) =0,\quad C=0 &\\\\ &\Rightarrow\quad B_y = -\frac{1}{2}\mu_0\alpha z^2 & \end{flalign}$$

### (1) $z=-\frac{d}{2}$에서 자기장 크기  $$
\begin{flalign}
&B_y = -\frac{1}{2}\mu_0\alpha z^2 \quad \Leftarrow z=-\frac{d}{2}&\\\\
&\boxed{B \! \left(-\frac d2\right) = \frac{\mu_
