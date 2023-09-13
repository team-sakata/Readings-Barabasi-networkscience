# chapter4

[スライド](https://img.hideo54.com/slides/barabasi-chap-4.pdf)

**べき分布の傾きが重要**

[SciSci創始者Priceの本](https://www.degruyter.com/document/doi/10.7312/pric91844/html)


## モーメント
- 2次：
    [尖度](https://ja.wikipedia.org/wiki/%E5%B0%96%E5%BA%A6)
    と
    [歪度](https://ja.wikipedia.org/wiki/%E6%AD%AA%E5%BA%A6)
- 3次：

多くのスケールフリーネットワークは2~3、特に
<k>が有限かつ<k^2>が発散するのが特徴→

[Watts and Strogatz model](https://www.researchgate.net/figure/The-Watts-Strogatz-model-of-the-small-world-The-network-at-the-upper-left-hand-corner_fig2_50268221)
のスモールワールド性（クラスター係数を高く保ったまま、距離を短くする）との関連は？
[その他のネットワークモデルについて](https://qiita.com/Takuya-Shuto-engineer/items/c3d6e7d4b06e1d337a06)
[Watts Strogatzのばらばし対応章](http://networksciencebook.com/chapter/3#clustering-3-9:~:text=Box%203.9-,Watts%2DStrogatz%20Model,-Duncan%20Watts%20and)

[fat-tailed & long-tail](https://design.kyusan-u.ac.jp/OpenSquareJP/?Distribution#:~:text=%E3%83%AD%E3%83%B3%E3%82%B0%E3%83%86%E3%83%BC%E3%83%AB-,Longtail%20%E3%81%A8Fattail,-Longtail%0AIT%E7%94%A8%E8%AA%9E)


Wiki

> ファットテール
裾の重い分布の中でも裾の分布がべき乗則にしたがって減衰する分布をファットテールと呼ぶことが多い。
詳細は「:en:Fat-tailed distribution」を参照
ロングテール
確率変数 X がすべての t > 0 について以下を満たす確率分布はロングテールである。

$${\displaystyle \lim _{x\to \infty }\Pr[X>x+t|X>x]=1,\,}$$
これは累積確率分布関数を F として以下と同じである。

$${\displaystyle {\overline {F}}(x+t)\sim {\overline {F}}(x)\quad {\mbox{as }}x\to \infty }$$ 
簡単にいえば、x → ∞ ではほとんど減衰しない裾を持つ分布である。
