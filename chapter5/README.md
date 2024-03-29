# 5 The Barabási-Albert Model
summerised by [Yatima Kagurazaka](https://twitter.com/Yatima_K)

## 5.1 Introduction

WWWや細胞の代謝ネットワークなどの全く異なるシステムが，同じようなスケールフリーアーキテクチャに収束するのはなぜか？  
スケールフリー特性の出現に関わるメカニズムがこの章の主要なトピック

## 5.2 Growth and Preferential Attachment

ランダムネットワークにはハブとべき乗則が存在しない  
以下のような特徴がないのが大きい  
- 成長：現実のネットワークは，ノード数 $N$ を継続的に増加させる成長プロセスの結果  
- 優先的選択：現実のネットワークでは，新しいノードはより接続されているノードにリンクする傾向  

例）WWW，論文，映画俳優

## 5.3 The Barabási-Albert Model

Barabási-Albertモデル（別名：BA モデル，スケールフリーモデル）  
優先的選択として，ノード $i$ に接続する確率を次数 $k_i$ により決定
$$\Pi (k_i ) = \frac{{k_i }}{{\sum\limits_j {k_j } }} \hspace{20 mm} (5 . 1)
$$
べき乗則とハブの起源は，成長と優先的選択の共存によって引き起こされる，富む者が更に富む現象

## 5.4 Degree Dynamics
  
<img src="./figures/figure-5-6.jpg" alt="5.6 Degree Dynamics">

古いノードが若いノードよりも有利になり，最終的にはハブに  
 $β$ はdynamical exponentと呼ばれ， $\frac{1}{2}$ である  
- すべてのノードは同じ力学的法則に従う  
- 度数の増加は線形未満（ $β<1$ ）．新しいノードのリンクより既存ノードの方が多く，奪い合いになるため  

## 5.5 Degree Distribution

Barabási-Albertモデルはdegree exponent $γ=3$ のスケールフリーネットワークを生成
$$p(k) \approx 2m^{1/\beta } k^{ - \gamma }  \hspace{20 mm} (5 . 9)$$

<img src="./figures/figure-5-7.jpg" alt="5.7 Probing the Analytical Predictions">

**a.** $\: m_0=m=1 \text{(blue)}, 3 \text{(green)}, 5 \text{(grey)}, 7 \text{(orange)}$  
各色が平行である事実は， $γ$ が $m$ および $m_0$ から独立していることを示す  
紫色の線の傾きは $-3$ で，degree exponent $γ=3$ に対応

## 5.6 The Absence of Growth or Preferential Attachment

スケールフリー特性の出現には，成長と優先的選択の両方とも必要なのか？

<img src="./figures/figure-5-8.jpg" alt="5.8 Model A and Model B">

**a.** 成長のみ． $m_0=m=1 \text{(circles)}, 3 \text{(squares)}, 5 \text{(diamonds)}, 7 \text{(triangles)} $  
すべてのノードが等しい確率でリンクを取得するため，富豪になるプロセスが欠けている  
**b.** 優先的選択のみ． $t=N \text{(circles)}, 5N \text{(squares)}, 40N \text{(diamonds)}$  
定常性が失われ，ネットワークが完全なグラフに収束することになる  

## 5.7 Measuring Preferential Attachment

優先的選択が現実のネットワークにも存在することを検出するには？  
- 条件1：あるノードに接続する可能性 $Π(k)$ は、そのノードの次数 $k$ に依存  
- 条件2： $Π(k)$ は $k$ において線形  
$$\frac{{\Delta k_i }}{{\Delta t}} \sim \Pi (k_i ) \hspace{20 mm} (5 . 20)$$

<img src="./figures/figure-5-9.jpg" alt="5.9 Detecting Preferential Attachment">
<img src="./figures/figure-5-10.jpg" alt="5.10 Evidence of Preferential Attachment">

破線は線形の優先的選択 ( $π(k) \sim k^2$ ) ，実線は優先的選択なし( $π(k) \sim k$ ) 

## 5.8 Non-linear Preferential Attachment

<img src="./figures/figure-5-12.jpg" alt="5.12 Nonlinear Preferential Attachment">

## 5.9 The Origins of Preferential Attachment

なぜ $Π(k)$ は $k$ に依存するのか？ $Π(k)$ が $k$ において線形になるのはなぜか？  
- ローカルメカニズム：ランダムなイベントとネットワークの構造的特性の間の相互作用  
例）知人から人を紹介される，読んだ論文の参考文献をたどる．遺伝子の複製とタンパク質相互作用ネットワークの関係性も該当するらしい  
- グローバルメカニズム：新しいノードやリンクが，矛盾するニーズのバランスを取る＝全体を把握していることを前提  
例）社会学における合理的選択理論，新しいケーブルを敷設する際の費用対効果の分析  

詳細な数式は原著参照

## 5.10 Diameter and Clustering Coefficient

<img src="./figures/figure-5-18.jpg" alt="5.18 Average Distance">
<img src="./figures/figure-5-19.jpg" alt="5.19 Clustering Coefficient">

## 5.11 Summary

ネットワーク構造と進化は切り離せない  
Erdős-RényiモデルやWatts-Strogatzモデルは絵画を写真に撮ったようなものであって，絵画を描いていったようなものではない  
  
以下のようなBarabási-Albertモデルの制限は，第6章で解決
- 現実のネットワークのdegree exponentは $γ=2～5$
- WWWや引用ネットワークなど多くのネットワークは有向
- 既存のノードからのリンクや，リンクやノードの消滅が考慮されていない
- ノードの区別をしていない
- あくまで最小限の原理証明モデル


t-miura memo:  
βは奪い合いになるので1より小さくならざるを得ない ← 時間の指数

γは一度に追加するリンク数mと独立で -3 ←次数分布の指数

*preferential attachmentとnetwork growthのどっちが重要？
→PAとgrowthをそれぞれ単独でやってみると、べき分布は現れない。（PAのみだと最初の時間区間Nはべき分布に近くなる）
