(pp.65-95)

# 3-1. Introduction
# 3-2. Bayesian concept learning
- concept learningの導入
- fuzzy set theory
- number gameを例にとって考える
    - C: 推定したいconcept
    - D: いくつかの正例の集合
    - x~: 未知の入力
    - p(x~∈C|D): posterior predictive distribution
    - H: 仮説空間 (Cの分類基準として考えられるもの)
    - つまりnumber gameとは: D = {16, 8, 2, 64} のとき, Dはどのような基準(C)で選ばれているでしょうか? という基準をいくつかの候補(H)から正しく当て, さらに未知の入力x~をCに当てはまるか否かを正しく二値分類するゲーム
    
### 3-2-1. Likelihood 尤度
- hを仮説空間Hに属する1つの仮説とする. たとえばh_two=「正例は2の累乗」, h_even=「正例は偶数」などと名付ける.
- このとき, DのサイズをNとすると, Dはhをみたすサンプル(その個数を|h|とする)を重複を許してN回サンプリングすることで構成できるから, p(D|h) = (1/|h|) ^ N.
- たとえば, D={16}のときは p(D|h_two)=1/6, p(D|h_even)=1/50となり, D={16,8,2,64}のときは p(D|h_two)=7.7x10^-4, p(D|h_even)=1.6x10^-7 になる.

### 3-2-2. Prior
### 3-2-3. Posterior
- ベイズの定理より p(h|D) = p(D|h)p(h) / p(D) = p(D|h)p(h) / sum(p(D|h')p(h'))
- ここで先ほどの議論より p(D|h) = I[D∈h] x (1/|h|) ^ N とできる. ただし I[D∈h] はD中のすべての要素がhを満たせば1, そうでなければ0とする.
- MAP推定は h_MAP = argmax_h p(h|D) とするもの.
- 最尤推定は h_MLE = argmax_h p(D|h) とするもの.

### 3-2-4. Posterior predictive distribution
- Posterior は belief state about the worldである.
- p(x~∈C|D) = sum(p(y=1|x~,h)p(h|D)) for h in H
- MAP,MLE推定後は p(x~∈C|D) = p(y=1|x~,h_ESTIMATED)

### 3-2-5. More complex prior
- p(h) = πo p_RULES(h) + (1-π0)p_INTERVAL(h)

# 3-3. Beta-binomial model
# 3-4. Dirichlet-multinomial model
# 3-5. Naive Bayes Classifiers
- xをD次元ベクトルとするとき, p(x|y=c, θ) = product(p(xj|y=c,θjc)) for j=1,...,D とモデル化すること.
















