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
        - <img src="https://latex.codecogs.com/gif.latex?\frac{1}{2}\left(1+\mathrm{erf}\left(\frac{z}{\sqrt{2}}\right)\right)" />1/2 (1 + erf(z/√2)) のようにも表現できる. erfは誤差関数
- t分布 Student t distribution
    - コーシー分布 Cauchy distribution (t分布で自由度が1の場合)
- ラプラス分布 Laplace distribution


# 2-5. Joint probability distributions
# 2-6. Transformations of random variables
# 2-7. Monte carlo approximation
# 2-8. Information theory
