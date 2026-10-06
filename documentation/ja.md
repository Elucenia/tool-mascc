<!-- ELUCENIA technical documentation · mascc · ja · no clinical/professional/rights approval -->

# MASCC指数

[条件・出典・許諾](https://elucenia.org/ja/tools/mascc)

## 使い方

ポータルでツールを使用するか、ローカルHTTPサーバー経由でindex.htmlを開いてください。言語を選択し、項目を入力して計算してください。

## 入力項目と単位

### 疾患の負担（発熱エピソードの症状）

`carga`

- `0` — 重度または瀕死
- `3` — 中等度
- `5` — なしまたは軽度

### 低血圧（収縮期血圧 \< 90 mmHg）

`hipotensao`

- `0` — はい
- `5` — いいえ

### 活動性の慢性閉塞性肺疾患

`dpoc`

- `0` — はい
- `4` — いいえ

### がんの種類

`tumor`

- `0` — 血液腫瘍で真菌感染の既往あり
- `4` — 固形腫瘍，または真菌感染の既往のない血液腫瘍

### 静脈補液を要する脱水

`desidratacao`

- `0` — はい
- `3` — いいえ

### 発熱が始まった場所

`local`

- `0` — 入院中
- `3` — 外来

### 年齢

`idade`

- `0` — ≥ 60 歳
- `2` — \< 60 歳

## 方法の版

MASCC/Klastersky 2000：7領域、計0–26、閾値≥21；ASCO/IDSA 2018の背景

## 記載された計算式

疾患負担：なし/軽度5、中等度3、重度0 · 低血圧なし5 · COPDなし4 · 固形腫瘍4、または真菌感染歴のない血液悪性腫瘍4 · 脱水なし3 · 外来3 · 年齢\<60歳2。最高26。

## 限界・対象集団

MASCC ≥21は合併症のリスクが低いことを示しますが、それだけで退院、経口抗菌薬、外来管理を認めるものではありません。ASCO/IDSA 2018の文脈では、対象者の選定は臨床評価、安定性、併存疾患、再診予定を守れること、自宅の介護者、利用できる電話と交通手段に依存します。外来管理の候補者は退院前に少なくとも4時間観察し、フォローアップが必要です。本実装の低血圧基準は2000年の原変数に従います：収縮期血圧\<90 mmHg。

## 参考文献

- [Klastersky J et al. The Multinational Association for Supportive Care in Cancer risk index: a multinational scoring system for identifying low-risk febrile neutropenic cancer patients. J Clin Oncol, 2000.](https://doi.org/10.1200/JCO.2000.18.16.3038)

- [Taplitz RA et al. Outpatient management of fever and neutropenia in adults treated for malignancy: American Society of Clinical Oncology and Infectious Diseases Society of America clinical practice guideline update. J Clin Oncol, 2018.](https://doi.org/10.1200/JCO.2017.77.6211)

- [ASCO/IDSA2018;DOI10.1200/JCO.2017.77.6211](https://www.idsociety.org/globalassets/idsa/practice-guidelines/outpatient-management-of-fever-and-neutropenia.pdf)

- [Original Klastersky2000;DOI10.1200/JCO.2000.18.16.3038](https://theempulse.org/wp-content/uploads/2016/04/The-Multinational-Association-for-Supportive-care-in-cancer-risk-index.pdf)

## 技術テストの再現

このリポジトリのルートディレクトリでnode test.cjsを実行すると、記録された合成ケースを再実行できます。元の入力、期待結果、許容誤差は保持されています。技術テストは臨床的検証を意味しません。

```sh
node test.cjs
```

tool.jsonには出典、版、確認範囲が記録されています。examples.jsonには合成入力と期待結果が保持され、results.jsonには実際に得られた結果が記録されています。

[記録・参考文献](../tool.json) · [JavaScriptコード](../calculator.js) · [参照ケース](../examples.json) · [results.json](../results.json)

## 確認状況と使用条件

独立した臨床レビューは実施されていません。

このインターフェースは独自に作成した翻訳であり、公式版や認証済みの版ではありません。独立した臨床レビュー、専門家による言語レビュー、評価尺度等の権利許諾の確認は実施されていません。

式または分類の結果です。解釈、対応、適用可能性は専門家による評価と選択した出典に依存します。

## ライセンスと帰属表示

Apache-2.0はELUCENIAのコードにのみ適用されます。評価尺度等、出版物、翻訳、データの権利は、それぞれの権利者に帰属します。LICENSEとNOTICEを保持してください。

ELUCENIA · Felipe Guedes · Copyright © 2026

## 記録された結果

以下の情報は、合成例に対する手法の出力を保持したものです。独立した臨床的検証を示すものではありません。

### 1

低リスク（≥ 21点）

臨床的および社会的基準も満たす場合、経口抗菌薬と外来管理の候補。


### 2

低リスク（≥ 21点）

臨床的および社会的基準も満たす場合、経口抗菌薬と外来管理の候補。


### 3

低リスクではない（< 21点）

入院させ、広域スペクトルの静脈内抗菌薬を開始する。

