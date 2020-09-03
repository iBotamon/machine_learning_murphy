# 7-1. Units
# 7-2. XOR Problem
- 2つの入力に対してXORを出力するような回路は単層のパーセプトロン(<img src="https://latex.codecogs.com/gif.latex?y=\sigma(wx+b)" />)では作れない
  - 線形分離できないから
- AND回路とOR回路をつくるのは簡単
  - w1 = 1, w2 = 1, b = -1, y = 1 if wx+b > 0 else 0 if wx+b <= 0 にするとAND回路
  - w1 = 1, w2 = 1, b = 0, y = 1 if wx+b > 0 else 0 if wx+b <= 0 にするとOR回路

# 7-2-1. The solution: neural networks
- しかし多層にして表現力を増すとXOR回路も作れるようになる
  - h1 = x1 + x2, h2 = x1 + x2 - 1, y = σ(h1 - 2h2) とするとXOR回路になる

# 7-3. Feed-Forward Neural Networks
- Feed-Forward Neural Networksとは
  - 定義: 多層ネットワークでかつ閉路をもたないもの. つまり入力は低層から高層にのみ流れ, 高層から低層には流れない
  - 注意: RNNは閉路をもつ
  - 歴史的経緯からMLP (multi-layer perceptrons)　とも呼ばれるが正確ではない
    - パーセプトロンは純粋な線形モデルのみを指し, 非線形活性関数を含むネットワークはパーセプトロンとは呼ばない
    
# 7-4. Training Neural Nets
略.

# 7-5. Neural Language Models
略.
