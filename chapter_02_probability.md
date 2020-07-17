(pp.27-64)

# 2-1. Introduction
- 頻度主義 frequentist vs ベイズ主義 Bayesian

# 2-2. A brief review of probability theory
- 離散確率変数 Discrete random variables
    - 状態空間 state space: 確率変数のとりうる全ての値の集合
- いくつかの定理
    - 同時確率 joint probabilities
    - 周辺確率 marginal distributions
    - 条件付き確率 conditional probability
    - ベイズの定理 Bayes Theorem
        - 基準率の誤謬 base rate fallacy (=事前確率(有病率)を無視して診断を下してしまうこと)
    - 独立 unconditionally independent / marginally independent
    - 条件つき独立 conditionally independent
- 連続確率変数 continuous random variables
    - 累積確率関数 cdf = cumulative distributon function
    - 確率密度関数 probability density function
    - 分位点 quantile
- 平均 mean (期待値 expected value), 分散 variance, 標準偏差 standard deviation

# 2-3. Some common discrete distributions
- 二項分布 binomial distribution
- ベルヌーイ分布 Bernoulli distributions
- 多項分布 multinomial distribution
- カテゴリカル分布 categorical distribution (= Multinoulli distribution. 多項分布で試行回数が1回の場合)
- ポアソン分布 Poisson distribution
- 経験分布 empirical distribution (単純にその値になっているサンプル数/全体のサンプル数を確率とする)

# 2-4. Some common continuous distributions
- ガウス分布 Gaussian distribution
    - ガウス分布の精度 precision
    - ガウス分布の累積密度関数
        - <img src="https://latex.codecogs.com/gif.latex?\frac{1}{2}\left(1+\mathrm{erf}\left(\frac{z}{\sqrt{2}}\right)\right)" /> のようにも表現できる. erfは誤差関数
- t分布 Student t distribution
    - コーシー分布 Cauchy distribution (t分布で自由度が1の場合)
- ラプラス分布 Laplace distribution <img src="https://latex.codecogs.com/gif.latex?\mathrm{Lap}(x|\mu,b)=\frac{1}{2b}\exp{\left(-\frac{|x-\mu|}{b}\right)}" />
- ガンマ分布
    - 指数分布 exponential distribution
    - アーラン分布 Erlang distribution
    - カイ二乗分布 chi-squared distribution
- ベータ分布 Beta distribution
- パレート分布 Pareto distribution

# 2-5. Joint probability distributions
- 共分散 covariance
- 多変量ガウス分布 multivariate Gaussian
- 多変量t分布 multivariate Student t distribution
- ディリクレ分布 Dirichlet distribution

# 2-6. Transformations of random variables
- Ax+bの期待値 (線形性)
- Ax+bの共分散
- 一般的な変数変換
    - Jacobianを掛ける: <img src="https://latex.codecogs.com/gif.latex?p_{y}(\mathbf{y})=p_{x}(\mathbf{x})|\det{\mathbf{J}_{\mathbf{y}\to\mathbf{x}}}|" />
- 中心極限定理 central limit theorem

# 2-7. Monte carlo approximation
- 確率変数 <img src="https://latex.codecogs.com/gif.latex?X" /> の確率密度関数 
 <img src="https://latex.codecogs.com/gif.latex?f(X)" /> を, 多数のサンプルによって近似する方法.
- つまり, ある入力 <img src="https://latex.codecogs.com/gif.latex?x" /> に対して確率値 <img src="https://latex.codecogs.com/gif.latex?y=f(x)" /> が返ってくるとき, <img src="https://latex.codecogs.com/gif.latex?(x,y)" /> の組を多数得ることによって<img src="https://latex.codecogs.com/gif.latex?f" /> を近似したい.
- そこで, <img src="https://latex.codecogs.com/gif.latex?S" /> 個のサンプルを <img src="https://latex.codecogs.com/gif.latex?x_{1},...,x_{S}" /> のように生成する. ただしサンプルは確率分布 <img src="https://latex.codecogs.com/gif.latex?x_{s}\sim" /><img src="https://latex.codecogs.com/gif.latex?p_{\mathrm{rand}}(x)" /> に従うとする. このとき, <img src="https://latex.codecogs.com/gif.latex?f(X)" /> をその経験分布 <img src="https://latex.codecogs.com/gif.latex?\{f(x_{s})\}_{s=1}^{S}" /> によって近似する.

# 2-8. Information theory
- エントロピー Entropy
- KLダイバージェンス KL divergence
- 相互情報量 mutual information
