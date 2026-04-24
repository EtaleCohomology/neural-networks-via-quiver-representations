# Neural Networks via Quiver Representations

**クィバー表現論で理解するニューラルネットワーク**

A technical survey on quiver representation theory and its application to neural networks, written for undergraduate-level readers.

クィバー表現論とニューラルネットワークへの応用についての技術サーベイ。学部 1-2 年生レベル向け。

---

## Overview | 概要

### English

Can a neural network be described, exactly and without approximation, by a classical object in algebra? In 2020, Marco Armenta and Pierre-Marc Jodoin showed that the answer is yes: a neural network is, strictly, a **quiver representation** equipped with activation functions at each vertex.

This survey traces the research program that has grown around this discovery over the past five years, covering:

- The basic definitions of quivers and quiver representations, built up through elementary examples
- The Armenta–Jodoin (2021) paper and its five central claims, explained in accessible terms
- A **moduli space** perspective: the geometric atlas of isomorphism classes of representations
- **Positive scale invariance of ReLU** and its role as the theoretical foundation of batch normalization
- Seven follow-up papers, including results on lossless model compression, neural teleportation, interpretability, and the algebraic-geometric origin of softmax
- Speculative directions for large language models (the author's own proposals)
- Open problems as of April 2026

The survey assumes only first-year linear algebra. It is written for readers who are curious about the inner workings of AI but do not have graduate-level mathematical training.

### 日本語

ニューラルネットワークは、代数学の古典的対象として、近似なしに厳密に記述できるだろうか。2020 年、Marco Armenta と Pierre-Marc Jodoin は、その答えが「できる」ことを示した。ニューラルネットワークは、各頂点に活性化関数を備えた **クィバー表現** として厳密に記述できる。

本サーベイ論考は、この発見から 5 年間に形成された研究の系譜を、以下の構成で辿るものである：

- クィバーとクィバー表現の基本定義 ― 小さな例から段階的に構築
- Armenta-Jodoin (2021) の論文と 5 つの主要主張 ― 平易な言葉で解説
- **モジュライ空間** の視点：表現の同型類を点とする幾何学的な地図
- **ReLU の正スケール不変性** ― バッチ正規化の理論的基盤
- 後続 7 論文の紹介：情報損失ゼロのモデル圧縮、Neural Teleportation、解釈可能性、softmax の代数幾何学的必然性など
- 大規模言語モデルへの応用可能性 (筆者による独自考察)
- 2026 年 4 月時点の未解決問題

本サーベイ論考は線形代数の基礎のみを前提とし、AI の内部構造に関心を寄せているが大学院レベルの数学的訓練を受けていない読者を想定読者として執筆した。

---

## Contents | 構成

### English

1. **Introduction** — Why look for mathematics inside AI
2. **Vector spaces and linear maps** — A review of the foundations
3. **Quivers** — Directed graphs with multiplicity
4. **Quiver representations** — Decorating a graph with numerical data
5. **Neural networks, translated into quivers** — The exact correspondence
6. **Isomorphism** — What it means for two representations to be "the same"
7. **Moduli spaces** — An atlas of isomorphism classes
8. **The Armenta–Jodoin paper of 2021** — Five central claims
9. **Subsequent developments** — Six follow-up papers in brief
10. **Applicability to large language models** — Open territory
11. **Current status and open problems**

Appendices:
- A. Chronology of key papers
- B. Glossary
- C. References

### 日本語

1. **はじめに** ― AI と数学のつながりを見たい
2. **準備: ベクトル空間と線形写像を復習する**
3. **クィバーとは何か** ― 矢印つきのグラフ
4. **クィバー表現とは何か** ― グラフに数字を付けたもの
5. **ニューラルネットの復習とクィバーへの翻訳**
6. **「同じ」とはどういうことか** ― 同型の考え方
7. **モジュライ空間** ― 「同じ」を 1 点にまとめた地図
8. **Armenta & Jodoin (2021) の中身**
9. **その後の発展** ― 6 つの論文のダイジェスト
10. **大規模言語モデルへの応用可能性**
11. **現状と未解決問題**

付録:
- A. 主要論文の年表
- B. 用語集
- C. 参考文献

---

## How to Read | 読み方

### English

**Intended audience.** Undergraduates in their first two years, comfortable with the basics of linear algebra; readers curious about machine learning but daunted by theoretical papers; anyone who wants to peek inside the black box of neural networks.

**Recommended reading strategy.** First, skim the whole document to get a sense of the landscape. Pay attention to the figures and examples; they are doing most of the work. Skip any passage that feels too hard and come back to it later. The most important takeaway is simply a feel for this way of looking at AI.

**This survey moves slowly, deliberately.** New terms are introduced through four stages: (1) why we need it, (2) a minimal example, (3) a more substantial example, (4) the formal definition. Abstract language appears only at stage 4.

### 日本語

**想定読者**: 大学 1〜2 年生レベルで、線形代数の基礎に慣れている方。機械学習に興味があるが理論論文が難しいと感じる方。ニューラルネットワークの「内側」を覗いてみたい方。

**推奨される読み方**: まず本文を飛ばし飛ばし眺めて、全体像を掴む。図と例に注目する。難しい箇所はスキップして次へ進む。大事なのは、「こんな視点で AI を見る研究があるんだ」という感覚を得ること。

**本サーベイは急がず、抽象語を避け、日常例を必ず先に置く**方針で書かれている。新しい用語は、以下の 4 段階を経て導入される:
1. なぜそれが必要か
2. 極めて単純な具体例
3. 普通の具体例
4. 正式な定義

抽象的な言葉は 4 段階目にのみ登場する。

---

## Files | ファイル構成

```
neural-networks-via-quiver-representations/
├── README.md                                       (this file)
├── LICENSE                                         (CC BY 4.0)
├── en/
│   └── quiver_neural_networks_survey.pdf           (English version)
└── ja/
    └── quiver_neural_networks_survey_ja.pdf        (Japanese version)
```

---

## Related Articles | 関連記事

### Zenn Article (Japanese, short version) | Zenn 記事 (日本語、要約版)

An introductory digest of this survey is available on Zenn:

本サーベイのダイジェスト版記事:

- (Add Zenn URL here after publication / 公開後に Zenn URL を追記)

### Qiita Article (Japanese, engineering-focused) | Qiita 記事 (日本語、実装寄り)

A practitioner-focused article with Python code examples, emphasizing model compression:

実装寄りの記事。PyTorch による動くコード例、モデル圧縮の視点を中心に:

- (Add Qiita URL here after publication / 公開後に Qiita URL を追記)

---

## Author | 著者

**Étale Cohomology** (pen name / 筆名)

- GitHub: [@EtaleCohomology](https://github.com/EtaleCohomology)
- Contact: etalecohomology@proton.me

---

## License | ライセンス

This work is licensed under the **Creative Commons Attribution 4.0 International License (CC BY 4.0)**. See the [LICENSE](./LICENSE) file for the full text.

You are free to share and adapt the material with appropriate attribution.

本作品は **クリエイティブ・コモンズ 表示 4.0 国際ライセンス (CC BY 4.0)** の下で公開されている。全文は [LICENSE](./LICENSE) を参照。

適切なクレジット表示のもと、共有・改変が自由に認められている。

---

## Citation | 引用

If you find this survey useful in your work, please consider citing it:

本サーベイが研究や学習に役立った場合は、以下の形式で引用いただけると幸いです:

```bibtex
@misc{etale2026moduli_nn,
  author = {Étale Cohomology},
  title  = {Neural Networks and Moduli Spaces: Understanding AI through Quiver Representation Theory --- A Survey for Undergraduates},
  year   = {2026},
  month  = {April},
  note   = {Technical survey, version 1.0, available at \url{https://github.com/EtaleCohomology/neural-networks-via-quiver-representations}}
}
```

---

## Feedback | フィードバック

Issues and pull requests are welcome. Reports of unclear passages, typos, or factual errors are especially appreciated.

Issues と pull requests を歓迎します。分かりにくい箇所、誤字、事実誤認の報告は特に歓迎します。

---

*This work is part of a broader series of surveys and notes by Étale Cohomology on the mathematical foundations of artificial intelligence.*

*本作品は、Étale Cohomology による人工知能の数学的基盤に関するサーベイ・ノートシリーズの一環である。*
