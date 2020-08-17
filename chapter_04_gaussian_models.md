(pp.65-95)

# 4-1. Introduction
## 4-1-1. 記法
## 4-1-2. 多変量ガウス分布の分散の基底変換
## 4-1-3. 多変量ガウス分布の平均と分散の最尤推定
## 4-1-4. 多変量ガウス分布はエントロピーを最大にする分布である

# 4-2. Gaussian discriminant analysis (判別分析) [???]
## 4-2-1. Quadratic Discriminant Analysis (2次判別) [???]
## 4-2-2. Linear Discriminant Analysis, LDA (線形判別分析) [???]
- 主成分分析は, データの分散が最大となるような軸を探す
- それに対して, 線形判別分析では, データのクラスをもっともよく分けられるような軸を探す
## 4-2-3. Two-class LDA (2クラス線形判別分析) [???]
## 4-2-4. 判別分析のための最尤推定
## 4-2-5. オーバーフィッティングを防ぐために
## 4-2-6. Regularized LDA (正則化判別分析) [???]
## 4-2-7. Diagonal LDA (対角線形判別分析) [???]
## 4-2-8. Nearest shrunken centroids classifier [???]

# 4-3. Inference in jointly Gaussian distributrions (分割したガウス分布における推論)
## 4-3-1. 分割したガウス分布における条件付き確率
## 4-3-2. 事例
### 4-3-2-1. 4-3-1.と似たようなもの
### 4-3-2-2. ノイズのないデータ点を補完する
- 1次元データを考える.
- 隣り合うデータ点x_{j-1}, x_{j+1}の間にあるデータ点を, x_{j} = (x_{j-1}とx_{j+1}の平均) + gaussian noize と仮定する.
- 

## 4-3-3. Information form
- ガウス分布のmoment parametersは<img src="https://latex.codecogs.com/gif.latex?\boldsymbol{\mu}" />, <img src="https://latex.codecogs.com/gif.latex?\boldsymbol{\Sigma}" />.
- しかし, canonical parameters あるいは natural parameters として, これらを次のように表現することもできる.
    - <img src="https://latex.codecogs.com/gif.latex?\boldsymbol{\Lambda}=\boldsymbol{\Sigma}^{-1}" /> (これは精度としてPRMLにも登場している)
    - <img src="https://latex.codecogs.com/gif.latex?\boldsymbol{\xi}=\boldsymbol{\Sigma}^{-1}\boldsymbol{\mu}" /> (これは初めて見た)
- これらを用いると, ガウス分布を information form によって表記できる:
    - <img src="https://latex.codecogs.com/gif.latex?\mathcal{N}_{c}(\mathbf{x}|\boldsymbol{\xi},\boldsymbol{\Lambda})=(2\pi)^{-D/2}|\boldsymbol{\Lambda}|^{\frac{1}{2}}\exp\left(-\frac{1}{2}(\mathbf{x}^{T}\boldsymbol{\Lambda}\mathbf{x}+\boldsymbol{\xi}^{T}\boldsymbol{\Lambda}^{-1}\boldsymbol{\xi}-2\mathbf{x}^{T}\boldsymbol{\xi})\right)" /> 
- こうすると, 分割したガウス分布の条件付き確率は<img src="https://latex.codecogs.com/gif.latex?\mathcal{N}_{c}" />を用いて簡略に表記することができる.
- 周辺化は本来のmoment formで表記するほうが簡潔になり, 条件付き確率にするにはinformation formで表記するほうが簡潔になる.
### 4-3-4-1. シューア補行列による, 分割した行列の逆行列
### 4-3-4-2. 逆行列に関する補題

# 4-4. 線形ガウスモデル
## 4-4-1.
## 4-4-2.
### 4-4-2-3. ノイズのあるデータ点を補完する-
## 4-4-3. 

# 4-5. ウィシャート分布
## 4-5-1. 逆ウィシャート分布

# 4-6. ガウス分布のパラメータ推定
## 4-6-1. ベイズ推定における平均の事後確率
## 4-6-2. ベイズ推定における分散の事後確率

