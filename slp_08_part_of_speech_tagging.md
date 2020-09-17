# 8-1. (Mostly) English Word Classes
- POS taggingは大まかに2つにわかれる
  - closed class types: 構成要素がほとんど変化しないもの. たとえば前置詞など. 新しい前置詞が登場することはほぼないため.
    - 前置詞 perpositions
    - 不変化詞 particles
    - 冠詞 determiners
    - 接続詞 conjunctions
    - 代名詞 pronouns
    - 助動詞 auxiliary verbs
      - コピュラ copula (be動詞など)
      - modal verb: do, haveなど
    - 数詞 numerals
    - 間投詞 interjections
    - 否定詞 negatives
    - 丁寧語 politeness markers
    - 挨拶 greetings
    - 存在のthere existential there
  - open class types: 構成要素が新しく登場しうるもの. 英語では名詞, 動詞, 形容詞, 副詞の4つ.
    - 名詞はさらに proper nouns, common nouns にわかれる
      - proper nouns: 何らかのentityの名前(人名や地名など)
      - common nouns: count nouns, mass nounsなどにさらに細分化される
        - count nouns: 可算名詞
        - mass nouns: 非可算名詞
    - 動詞
    - 形容詞
      - 韓国語では形容詞は動詞のようにふるまう
    - 副詞
      - directional adverb / locative adverb: 方向や場所を示す
      - degree adverb: 程度を示す
      - manner adverb: 動作のようすを修飾する
      - temporal adverb: それが起こった日時を示す

# 8-2. The Penn Treebank Part-of-Speech Tagset
- POS taggingのための有名なコーパス
  - 英語
    - Brown corpus
      - 500文から作成されている
      - POS tagは87種類定義されている
    - PTB
      - 1993年に発表
      - POS tagは45種類定義されている (Brown tag setから減らされている)
    - WSJ
      - 1億語からなる
    - Universal Dependencies project
      - 2016年発表
  - ちなみに日本語では?
    - 京都大学テキストコーパス
      - 毎日新聞のテキスト4万文に形態素と構文情報が付与されている
      - 形態素の区切り, 品詞, よみ, 原形, 活用型, 活用形など
      - 文節の区切り, 文節間の係り受けが付与されている
    - NAISTテキストコーパス
      - 京都大学テキストコーパスに述語項構造と照応関係がアノテーションされている
    - BCCWJコーパス
      - 現代日本語書き言葉均衡コーパス
      - 書籍, 新聞, ブログ, 白書などから作成している
      - 約1億語からなる
      - すべてのテキストが形態素解析されている
      - 一部のテキストについては単語, 文節係り受け, 並列構造, 節境界などの構文情報が付与されている

# 8-3. Part-of-Speech Tagging
- POS taggingは実質的には語義曖昧性解消に近い
- つまり複数の品詞をとりうる単語に対して正しく品詞タグを付与できるかどうかが問題となる
  - 複数の品詞をとりうる単語は, 語彙としては14-15%にすぎないが, 高頻度語が多いので単語としては55-67%を占めている
  - これはWSJでもBrownでも同じ
- WSJコーパスにおけるモデルの性能
  - most-frequent-tag baseline: accuracy 92.34%
  - HMM, MEMM, NN, ルールベースなど: accuracy 97%

# 8-4. HMM Part-of-Speech Tagging
## 8-4-1. Markov Chains
- マルコフ仮定 Markov Assumption
  - 次の状態は直前の状態だけに依存する
- マルコフ連鎖は状態をノード, 遷移をエッジとしたグラフで表現できる
  - エッジには確率を付与できる

## 8-4-2. The Hidden Markov Model
- HMMはマルコフ連鎖の拡張
- 隠れ状態は, 直前の隠れ状態にのみ依存する
- 出力状態は, 同時点での隠れ状態にのみ依存する

## 8-4-3. The components of an HMM tagger
- まず品詞の遷移確率 transition probability をカウントベースで求める:
  - P(t_i | t_(i-1)) = C(t_(i-1), t_i) / C(t_(i-1))
- 次に品詞を条件とする単語の条件付き確率である出力確率 emission probability をカウントベースで求める:
  - P(w_i | t_i) = C(t_i, w_i) / C(t_i)
- このようにして遷移確率の行列A, 出力確率の行列Bを求める

## 8-4-4. HMM tagging as decoding
- HMMにおいて, 2つの仮定をおくと, 推論は遷移確率と出力確率の積によって求められる
  - 仮定1: 単語は品詞だけに依存して決定される
  - 仮定2: bigram assumption: 品詞は直前の品詞だけに依存する

## 8-4-5. The Viterbi Algorithm
- Viterbi Algorithm

## 8-4-6. Working through an example


## 8-4-7. Extending the HMM Algorithm to Trigrams
## 8-4-8. Beam Search
## 8-4-9. Unknown Words
# 8-5. Maximum Entropy Markov Models
# 8-6. Bidirectionality
# 8-7. Part-of-Speech Tagging for Morphological Rich Languages
