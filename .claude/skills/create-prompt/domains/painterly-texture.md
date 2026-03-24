# 絵画的質感・画材表現

## メタデータ
- priority: 7
- conflicts: []

## ルール

### 絵画的質感の基本
- にじみ、塗りムラ、筆致、かすれを積極的に残す
- 水彩の透明層の上に、油絵的な不透明色や強い筆跡が後から重ねられている印象を持たせる
- 制作過程が感じられる画面構成を優先する
- すべてを整えすぎず、わずかな未完成さを許容する
- 完成度よりも「描いている途中の勢いが残っている」印象を優先する

### 着彩スタイル：水彩×油絵のハイブリッド
- 水彩的なにじみ、滲出、透明感をベースにする
- その上から、油絵的な不透明色や強い筆跡を部分的に重ねる
- すべてを均一なタッチで仕上げない
- 筆跡、かすれ、塗りムラ、簡略化された描画を積極的に許容する
- 水彩っぽさが強く出すぎて軽くなる場合は以下を優先：
  - 色の層を増やす
  - 一部に重みのある不透明色を置く
  - ストロークの存在感を強める

### 色層構造
- 一色で均一に塗らず、複数の色層を重ねて深みを作る
- 透明な色の重なり、不透明色の差し込みによって彩度が自然に揺らいで見える状態を目指す
- 透明層＋不透明層を重ねる
- 均一塗り禁止
- 筆致を残す

### 強弱と余白
- 線・色・筆致には必ず意図的な強弱を与える
- すべてを均一な完成度に整えない
- 一部に未整理・未完成・曖昧さが残ることを許容する
- 「上手く描けている」よりも「なぜか印象に残る」部分が一箇所以上生まれる状態を優先する

### 強弱の自然化
- 付与された強弱は「技法として目立つ」状態にならないよう制御する
- 強弱は設計されていても、結果として自然に見えることを優先する
- 色のメリハリはコントラストではなく層の重なりで表現する
- 極端な濃淡や派手な対比で強弱を示さない

### 漫画的効果の扱い
- 漫画的な効果表現（省略、強調、単純化、記号化）はあくまで補助として使用する
- 主役の感情や雰囲気を補強する目的でのみ使用する
- 線や効果が前面に出すぎないよう、必ず絵画的表現に馴染ませる
- 漫画的な処理は局所的に留め、画面全体には広げない

### 画材ブロック生成規則（プロンプト出力時必須）
画材は必ず以下形式で出力：
```
[painting medium], visually interpreted as [physical behavior]
```

例：
- gouache painting, visually interpreted as matte opaque pigment layers with visible brush drag
- mineral pigment ink wash, visually interpreted as granulating particles and uneven absorption
- oil pastel, visually interpreted as waxy pigment buildup with edge breakage
- dry pigment on textured paper, visually interpreted as powdery edge diffusion

禁止：
- "digital art" 単体使用
- style名のみの記述

### 技法ブロック生成規則（プロンプト出力時必須）
技法は必ず以下形式で出力：
```
[technique term], defined as [visual construction behavior]
```

例：
- scumbling, defined as semi-dry pigment dragged across raised texture
- wet-on-dry layering, defined as transparent stain over fully dried base
- broken color layering, defined as adjacent strokes of different hues without blending

## キーワード
- 質感系: visible brushstrokes, watercolor bleeding, paint texture, uneven pigment
- 画材系: gouache, mineral pigment ink wash, oil pastel, dry pigment on textured paper
- 技法系: scumbling, wet-on-dry layering, broken color layering
- 回避: digital art（単体）, smooth rendering, airbrushed, clean finish

## 例
- 良い例: "gouache painting, visually interpreted as matte opaque pigment layers with visible brush drag, scumbling, defined as semi-dry pigment dragged across subtle paper grain"
- 悪い例: "digital painting"（具体性なし）、"smooth airbrushed render"（均一デジタル処理）
