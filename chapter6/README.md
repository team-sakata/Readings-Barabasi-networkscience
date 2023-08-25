# Section 6.1 Introduction

Google は遅れて WWW の検索分野に参入した。（その当時は AltaVista と Inktomi が最大勢力）
すぐにリンク数は Google が覇権をとり、さらに 10 年後 Facebook がその最大リンクノードの座を奪った。

[Erdős-Rényi](https://en.wikipedia.org/wiki/Erd%C5%91s%E2%80%93R%C3%A9nyi_model) モデル（=ランダムグラフ）では説明ができなかった。

The Barabási-Albert モデル はより現実的な像を描く：ノードの次数は時間の平方根に比例する。

だがそうするとノードの次数はノードの年齢に依存することになってしまう。実際には Web ページも、会社も、俳優も、遅れて出てきたのに急速に大きなノードと繋がることがある。（Garment 地区の事例。）

この章ではノードが次数を増やしていく速度の違いがどのようにネットワークに影響するのかを見ていく。

# 6.2 The Bianconi-Barabási Model

ノードがどれくらいリンクを獲得しやすい傾向を fitness (適合度)と呼ぶことにする。

[The Bianconi-Barabási Model](video-6-1.mov)

Bianconi-Barabasi モデル：それぞれの新しいノードがランダムな fitness を持っており、フィットネスと現在の次数の積で重み付けされた確率で新しいノードが接続されると仮定したモデル。
$$\Pi _i  = \frac{{\eta _i k_i }}{{\sum\limits_j {\eta _j k_j } }} \hspace{20 mm} (6 . 1)$$

\*6.1 で述べた Barabási-Albert モデルは、成長速度が次数のみによって決まる場合を考えている。次数に比例することは、たくさんのノードから接続されているほどよりそのノードが発見されやすくなる事実を、fitness は同じ次数のノードがあったときにより適合度の高いノードを選ぶ事実を捉えている。

各ノードの増加速度は
$$\frac{{\partial k_i }}{{\partial t}} = m\frac{{\eta _i k_i }}{{\sum\limits_j {\eta _j k_j } }} \hspace{20 mm} (6 . 2)$$

$$ k(t,t_i ,\eta_i ) = m\left( {\frac{t}{{t_i }}} \right)^{\beta (\eta_i )} \hspace{20 mm} (6 . 3)$$

$$ \beta (\eta ) = \frac{\eta }{C} \hspace{20 mm} (6 . 4)$$

$$C = \int {\rho (\eta )\frac{\eta }{{1 - \beta (\eta )}}d\eta }  \hspace{20 mm} (6 . 5)$$

\*[連続体論](<https://ja.wikipedia.org/wiki/%E9%80%A3%E7%B6%9A%E4%BD%93_(%E4%BD%8D%E7%9B%B8%E7%A9%BA%E9%96%93%E8%AB%96)#:~:text=%E6%95%B0%E5%AD%A6%E3%81%AE%E4%B8%80%E5%88%86%E9%87%8E%E3%81%A7,(Continuum%20theory)%20%E3%81%A8%E5%91%BC%E3%81%B6%E3%80%82>)
を使うと、と書いてあるが使わなくても示せそう。

# Section 6.3 Measuring Fitness
