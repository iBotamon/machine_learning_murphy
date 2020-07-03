# 1-1. Machine learning: what and why?
教師なし学習, 教師あり学習, 強化学習
cf. 強化学習の基礎 -> 5-7  

# 1-2. Supervised learning
cf. MAP推定 -> 5-7  
cf. Bag of words -> 3-4  

# 1-3. Unsupervised learning
教師あり学習との違いは2点ある.

- 1つ目: <img src="https://latex.codecogs.com/gif.latex?p(y_{i}|\mathbf{x}_{i},\boldsymbol{\theta})" /> という条件付確率を推定するのではなく <img src="https://latex.codecogs.com/gif.latex?p(\mathbf{x}_{i}|\boldsymbol{\theta})" />
という確率を推定していること

- 2つ目: <img src="https://latex.codecogs.com/gif.latex?p(y_{i}|\mathbf{x}_{i}" /> は通常多次元ベクトルなので, 多次元分布を扱う必要がある

主な教師なし学習の応用例
- クラスタリング
- 主成分の検出
- グラフ構造
- 行列補完
    - image inpainting
    - collaborative filtering
    - market basket analysis

cf. 主成分分析 PCA -> 12-1
cf. トピックモデル -> 27-2
cf. 信号処理における次元削減 -> 12-6
cf. 画像処理における次元削減 -> 15-5
cf. graphical lasso -> 26-7

# 1-4. Some basic concepts in machine learning

- ノンパラメトリックモデルの例
    - k-近傍法
- 次元の呪い
- パラメトリックモデルの例
    - 線形回帰
    - ロジスティック回帰
- 過学習
- モデル選択
