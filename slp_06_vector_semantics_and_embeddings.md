# 6-1. Lexical Semantics
- lemma: 標準形, 辞書形
- wordform: 表層形, 出現形
- synonymy と similarity
  - 同義語をもたない単語はあまり多くないが, 似た単語をもつ単語はたくさんある
  - 例: catとdogは同義語ではないが"似ている"
  - SimLex-999 dataset (2015) という単語の類似度を付与したデータセットがある
- semantic frames and roles 意味役割
- connotation 含意
  - valence: 
  - arousal: 
  - dominance: 

# 6-2. Vector Semantics
- 語をベクトル化するという概念の紹介
- 具体例として tf-idf と word2vec を紹介する
- 類似度の評価法としてコサイン類似度を紹介する

# 6-3. Words and Vectors
### 6-3-1. Vectors and documents
- term-document matrix

### 6-3-2. Words as vectors
- term-term matrix (word-word matrix, term-context matrix)
- Co-occurrence vector

# 6-4. Cosine for measuring similarity
- コサイン類似度の計算法の紹介

# 6-5. TF-IDF: Weighing terms in the vector
- 6-3-1. にあるように単語と文書の関係をベクトルにすることができる
- TF-IDFは文や文書をベクトル化することには向いているが, 単語のベクトル化には向いていない(意味がない)

# 6-6. Applications of the tf-idf vector model

# 6-7. Optional: Pointwise Mutual Information (PMI)
- PMIとは, 2つの事象x,yが, 偶然よりも共起しやすいかどうかを測る指標
- <img src="https://latex.codecogs.com/gif.latex?I(x,y)=\log_{2}\frac{P(x,y)}{P(x)P(y)}" />
- NLPに応用すると, 単語wとコンテキストcに適用して, <img src="https://latex.codecogs.com/gif.latex?\mathrm{PMI}(w,c)=\log_{2}\frac{P(w,c)}{P(w)P(c)}" />
- PMIが負の値になるときは0に置き換えるようにしたものをPPMI(Positive PMI)とよぶ
  - <img src="https://latex.codecogs.com/gif.latex?\mathrm{PPMI}(w,c)=max(\log_{2}\frac{P(w,c)}{P(w)P(c)},0)" />
- したがって, PMIを用いると, ある単語wを, 他の単語w1,...,w|V|との関係において表現することができる(分散表現のようなことができる).
- よって, PMIは単語のベクトル化に向いている
- ただし, PMIはかなり珍しい単語に対して高い値を出力してしまうというバイアスがあるので, 調整することがある
  - <img src="https://latex.codecogs.com/gif.latex?\mathrm{PPMI}_{\alpha}(w,c)=max(\log_{2}\frac{P(w,c)}{P(w)P_{\alpha}(c)},0)" />

# 6-8. Word2vec
- skip-gram with negative sampling (SGNS)
  - ターゲットとコンテキストの組が与えられたときに, 本当にその組が正しいかどうかを二値分類する
- continuous bag-of-words (CBOW)
  - コンテキストからターゲットを予測する
- negative samplingをどうするか?
  - コーパスには正例しかないので, 負例について学習できない
  - そこで, 負例を適当にサンプリングして作る
  - 負例は単語の出現頻度を0.75乗して丸めた確率分布

# 6-9. Visualizing Embeddings

# 6-10. Semantic properties of embeddings

# 6-11. Bias and Embeddings

# 6-12. Evaluating Vector Models
- どのように評価するか?
  - WordSim-353 dataset
  - SimLex-999 datasert
  - TOEFL dataset
  - SCWS (Stanford Contextual Word Similarity) dataset
  - WiC (Word-in-Context) dataset

# 6-13. Summary
