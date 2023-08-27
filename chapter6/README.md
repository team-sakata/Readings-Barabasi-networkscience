[スライド](https://docs.google.com/presentation/d/1LM69XaUdYvsKkUYS6jgCOjWE56by1zBVcZX-h-NcqB8/edit#slide=id.p)にまとめた

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

\*6.1 で述べた Barabási-Albert モデルは、成長速度が次数のみによって決まる場合を考えている。

次数に比例することは、たくさんのノードから接続されているほどよりそのノードが発見されやすくなる事実を、fitness は同じ次数のノードがあったときにより適合度の高いノードを選ぶ事実を捉えている。

各ノードの増加速度は
$$\frac{{\partial k_i }}{{\partial t}} = m\frac{{\eta _i k_i }}{{\sum\limits_j {\eta _j k_j } }} \hspace{20 mm} (6 . 2)$$

$$ k(t,t_i ,\eta_i ) = m\left( {\frac{t}{{t_i }}} \right)^{\beta (\eta_i )} \hspace{20 mm} (6 . 3)$$

$$ \beta (\eta ) = \frac{\eta }{C} \hspace{20 mm} (6 . 4)$$

$$C = \int {\rho (\eta )\frac{\eta }{{1 - \beta (\eta )}}d\eta }  \hspace{20 mm} (6 . 5)$$

\*[連続体論](<https://ja.wikipedia.org/wiki/%E9%80%A3%E7%B6%9A%E4%BD%93_(%E4%BD%8D%E7%9B%B8%E7%A9%BA%E9%96%93%E8%AB%96)#:~:text=%E6%95%B0%E5%AD%A6%E3%81%AE%E4%B8%80%E5%88%86%E9%87%8E%E3%81%A7,(Continuum%20theory)%20%E3%81%A8%E5%91%BC%E3%81%B6%E3%80%82>)
を使うと、と書いてあるが使わなくても示せそう。

$$p_k  \approx C\int {d\eta \frac{{\rho (\eta )}}{\eta }\left( {\frac{m}{k}} \right)^{\frac{C}{\eta } + 1} }  \hspace{20 mm} (6 . 6)$$

$$p_k  \sim \int\limits_0^1 {d\eta \frac{{C^* }}{\eta }\frac{1}{{k^{1 + C^* /\eta } }}}  \sim \frac{{k^{ - (1 + C^* )} }}{{\ln k}} \hspace{20 mm} (6 . 8)$$

# Section 6.3 Measuring Fitness

$$\ln k(t,t_i ,\eta _i ) = \beta (\eta _i )\ln t + B_i  \hspace{20 mm} (6 . 9)$$

$$\frac{{k_2  - k_1 }}{{k_1 }} \sim t^{\frac{{n_2  - n_1 }}{C}} \hspace{20 mm} (6 . 10)$$

$$\Pi _i  \sim \eta _i c_i^t P_i (t) \hspace{20 mm} (6 . 11)$$

$\eta _i$ はその研究が新規性や重要だと認識される度合い。

$c_i^t$ は時点tでの論文iが得ている総引用数。preferential attachment。

$ P_i (t)$ は他の論文に組み込まれていくうちにその論文のアイデアの新規性が薄れる状態を捉える。

$$P_i (t) = \frac{1}{{\sqrt {2\pi t\sigma _i } }}e^{ - \frac{{(\ln t - \mu _i )^2 }}{{2\sigma _i^2 }}}  \hspace{20 mm} (6 . 12)$$

$$C_i^t  = m\left( {e^{\frac{{\beta (\eta _i) }}{A}\Phi (T_t)}  - 1} \right) \hspace{20 mm} (6 . 13)$$

$$ T_t =   {\frac{{\ln t - \mu _i }}{{\sigma _i }}} $$

$$\Phi (x) = \frac{1}{{\sqrt {2\pi } }}\int\limits_{ - \infty }^x {e^{ - y^2 /2} dy}  \hspace{20 mm} (6 . 14)$$

# Section 6.4 Bose-Einstein Condensation

# Section 6.5 Evolving Networks

# Section 6.6 Summary
$$ \gamma  = 3 + \frac{A}{m} \hspace{20 mm} (6 . 24)$$
$$p_k  = C(k + A)^{ - \gamma }  \hspace{20 mm} (6 . 25)$$

$$\Pi (k,k') \sim (A + Bk)(A + Bk)' \hspace{20 mm} (6 . 26)$$ 

$$ \gamma  = 2 + \frac{m}{{m + 2n}} \hspace{20 mm} (6 . 27)$$

$$\gamma  = 3 + \frac{{2n}}{m} \hspace{20 mm} (6 . 28)$$

$$\gamma  = 3 + \frac{2}{{1 - r}} \hspace{20 mm} (6 . 29)$$


$$m(t) = m_0 t^\theta   \hspace{20 mm} (6 . 30)$$

$$\gamma  = 3 + \frac{{2\theta }}{{1 - \theta }} \hspace{20 mm} (6 . 31)$$

$$\Pi (k_i ,t - t_i ) \sim k(t - t_i )^{ - \nu }  \hspace{20 mm} (6 . 32)$$


\Pi (k_i ,t - t_i ) \sim k(t - t_i )^{ - \nu } \hspace{20 mm} (6 . 32)
