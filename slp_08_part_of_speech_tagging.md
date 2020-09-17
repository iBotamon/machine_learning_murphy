# 8-1. (Mostly) English Word Classes
- POS taggingは大まかに2つにわかれる
  - closed class types: 構成要素がほとんど変化しないもの. たとえば前置詞など. 新しい前置詞が登場することはほぼないため.
    - 前置詞 perpositions
    - 冠詞 determiners
    - 接続詞 conjunctions
    - 代名詞 pronouns
    - 助動詞 auxiliary verbs
    - 数詞 numerals
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
# 8-3. Part-of-Speech Tagging
# 8-4. HMM Part-of-Speech Tagging
## 8-4-1. Markov Chains
## 8-4-2. The Hidden Markov Model
## 8-4-3. The components of an HMM tagger
## 8-4-4. HMM tagging as decoding
## 8-4-5. The Viterbi Algorithm
## 8-4-6. Working through an example
## 8-4-7. Extending the HMM Algorithm to Trigrams
## 8-4-8. Beam Search
## 8-4-9. Unknown Words
# 8-5. Maximum Entropy Markov Models
# 8-6. Bidirectionality
# 8-7. Part-of-Speech Tagging for Morphological Rich Languages
