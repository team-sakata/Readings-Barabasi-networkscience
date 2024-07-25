# Chapter 8. ネットワークの堅牢性

## Section 1. Introduction

この chapter の目的: 複雑系の堅牢性 (robustness) を理解する

## Section 2. 浸透理論

![](http://networksciencebook.com/images/ch-08/figure-8-3.jpg)

格子上の各点に確率 $p$ で石を置いていくとしましょう。現れるネットワークについて、以下のような性質が現れてきます。

* 各クラスタのサイズの平均 $\langle s \rangle \sim |p - p_c| ^ {-\gamma_p}$
* ランダムに選んだ石が最大コンポーネントに属している確率 $P_\infty \sim (p - p_c) ^ \beta_p$
* 2つの石のペアの距離の平均 $\xi \sim |p - p_c| ^ {-\nu}$

![](http://networksciencebook.com/images/ch-08/figure-8-4.jpg)

つまり、ある値 $p_c$ を境にして、性質が急に変化します。この $p_c$ の値は格子のトポロジに依りますが、どのような値でもこのべき乗の性質は変わらず、普遍的なものとなっています。

逆に、格子状のすべての点に置かれた石を、ある割合 $f$ だけ取り除く場合にも、次のように急にネットワークが崩壊していくような結果となります。

![](http://networksciencebook.com/images/ch-08/figure-8-5.jpg)

## Section 3. スケールフリーネットワークの堅牢性

Section 2 では、普通の格子について堅牢性を検討しましたが、これをスケールフリーネットワークに適用するとどうなるのでしょうか。

![](http://networksciencebook.com/images/ch-08/figure-8-7.jpg)

Section 2 の理論では「ある値からガラッと崩壊する」ような形だったのに対して、どれだけ取り除いてもネットワークが崩壊しないという結果になりました。
こうした性質はどのような場合に現れるのでしょうか。

$\kappa = \frac{\langle k^2 \rangle}{k} > 2$ であれば巨大なコンポーネントが生まれる、とする  Molloy-Reed  基準があります。2を下回ればネットワークは多くのプツ切れのコンポーネントに分かれてしまいます。ランダムネットワークであれば $\langle k^2 \rangle = \langle k \rangle (1 + \langle k \rangle$ として、$\langle k \rangle > 1$ となります。

$f_c = 1 - \frac{1}{\frac{\langle k^2 \rangle}{k} - 1}$ が導け、同様に $\langle k^2 \rangle = \langle k \rangle (1 + \langle k \rangle$ を当てはめると、$f_c^{ER} = 1 - \frac{1}{\langle k \rangle}$ となります (このあたりの導出の詳細は Advanced Topic に載っているらしい)。つまり、ランダムネットワークの密度が大きければ大きいほど、ネットワークを崩壊させるのは難しくなります。

![](http://networksciencebook.com/images/ch-08/figure-8-9.jpg)

$f_c$ の式で、$\langle k \rangle, \langle k^2 \rangle$ をスケールフリーネットワークのパラメータ $\gamma$ や $k_{max}, k_{min}$ で置き換えると

* $2 < \gamma < 3$ では $1 - \frac{1}{\frac{\gamma - 2}{3 - \gamma} k_{min}^{\gamma - 2} k_{max}^{3 - \gamma} - 1}$
* $\gamma > 3$ では $1 - \frac{1}{\frac{\gamma - 2}{\gamma - 3} k_{min} - 1}$

となります。 $\gamma > 3$ では、 $f_c$ は $k_{max}$ に依存しないため、ネットワークサイズに依存せず、ランダムネットワークのような挙動になって、ネットワークが崩壊しやすくなります。 $\gamma < 3$ では、 $N \to \infty$ では $f_c \to 1$ となり、ネットワークを崩壊させるにはすべてのノードを取り除かねばならなくなります。

以上はこの章の一番大事なところです。スケールフリーネットワークでは次数が低いノードが大量にあるので、ランダムにノードを取り除くぶんには、ハブはなかなか崩れません。空港のネットワークで例えれば、ランダムにノードを壊していっても地方のどっか知らんところの空港が潰れていくだけで、New York から東京に移動するのには何の支障も生じません。

とはいっても、実際のところネットワークのノード数は多いと言っても有限なので、 $N$ との関係は気になるところです。 $f_c \sim 1 - \frac{C}{N^{\frac{3 - \gamma}{\gamma - 1}}}$ と近似でき ( $C$ は $N$ に依らない定数)、例えばインターネットなら $f_c = 0.972$ と算出できます。

一般に、ランダムネットワークよりも閾値が高ければ、堅牢性は成り立ちます。ネットワークが堅牢であるうえで、ネットワークの次数の分布が厳密にべき乗則に従っている必要はありません。同様のサイズのランダムネットワークよりも $\langle k^2 \rangle$ が大きくさえあればよいのです。そしてそれはほとんどの自然界のネットワークで成り立っています。

以上のような議論は、ノード除去だけでなくエッジ除去でも同様に成り立ちます。
![](http://networksciencebook.com/images/ch-08/figure-8-10.jpg)

![Screen Shot 2024-07-25 at 11 20 38](https://github.com/user-attachments/assets/3773cc07-a32e-4c8f-b981-6cc67e7bdd6d)

## Section 4. 攻撃耐性

TBA

## Section 5. なだれのような崩壊 (Cascading Failure)

TBA

## Section 6. なだれのような崩壊のモデリング

TBA

## Section 7. 堅牢性の作りかた

TBA

## Section 8. まとめ

TBA
