# パーソナライズ版：キャラクター造形 上書き

<!--
  このカプセルはパーソナライズ版（/create-prompt-p）でのみ読み込まれる。
  共通カプセル character-form.md の一部ルールを上書きする。
-->

## メタデータ
- priority: 9
- conflicts: []
- overrides: [character-form]

## 上書きルール

### 頭身・デフォルメの許容範囲（共通より広い）
- 共通カプセルでは「デフォルメは記号化しない範囲に留める」だが、
  パーソナライズ版では以下を許容する：
  - 極端な低頭身（2〜3頭身のちびキャラ的比率）もOK
  - 頭部が身体に対して大きい比率を許容する
  - ただし記号的な顔表現（●目、3口 等）は引き続き禁止
  - 顔の可読性（目・頬・顎・首の連続した面）は必ず維持する

### 主役の成立条件
- 顔は必ず一目で認識できる
- 目、頬、顎、首の形が連続した面として読める
- 髪や光で顔を分断しない
- デフォルメが強くても、上記の顔の成立条件は絶対に崩さない

### 造形の方向性
- 共通カプセルの「漫画と絵画の中間」を維持しつつ、
  よりカジュアルでラフなスケッチ感を許容する
- 「挿絵的バランス」→「落書き帳のスケッチ〜挿絵」まで幅を広げる

## キーワード
- 許容: compact proportions, oversized head ratio, sketch-like figure construction
- 維持: face readable as continuous surface of eyes cheeks chin and neck
- 禁止: symbolic dot-eyes, emoticon-like expressions

## 例
- 良い例: "a small figure with compact 2.5-head proportions, face clearly readable with gentle color-defined features despite simplified body"
- 悪い例: "chibi with dot eyes and >_< expression"（記号的表現）
