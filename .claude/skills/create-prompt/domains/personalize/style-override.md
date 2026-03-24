# パーソナライズ版：画風・線質・色面 上書き

<!--
  このカプセルはパーソナライズ版（/create-prompt-p）でのみ読み込まれる。
  共通カプセル art-style.md / painterly-texture.md の一部ルールを上書きする。
  上書きされないルールはそのまま共通カプセルに従う。
-->

## メタデータ
- priority: 9
- conflicts: []
- overrides: [art-style, painterly-texture]

## 上書きルール

### テイスト固定（最重要）
- 「画材」ではなく「見え方」で統一する
- 画材名・技法名での指定よりも、視覚的な結果の記述を優先する
- 具体的な画材ブロック（`visually interpreted as` 形式）は必須としない
  → 代わりに見え方の直接記述で代替してよい

### 線の扱い（共通カプセルより緩い）
- 線はさらにラフで途切れが多い
- 輪郭は部分的に途切れてよい（共通カプセルの「必要箇所にのみ」をさらに極端に）
- 線は「描き残し」「走り書き」のような勢いを許容する
- 線が完全に消えて色面だけになる箇所があってもよい
- 純黒禁止は共通と同じ

### 色面と塗り
- 塗りは均一にせず、ムラ・にじみ・濃淡差を積極的に残す
- 色の境界がやや曖昧に混ざる
- 単色ベタ塗り禁止
- 水彩/インク的な「紙に染み込む」質感を基本とする
- 油絵的な不透明の重ねは控えめに（共通カプセルの「水彩×油絵ハイブリッド」より水彩寄り）

### 密度差（共通カプセルより極端）
- 顔周辺のみ高密度で明確に描写する
- 髪は束ではなく塊で処理する
- 衣装は細部省略、面で扱う
- 背景は物体として描かず、色面の重なりとして扱う
- 背景の最低限の色面のみ（共通カプセルの「省略」をさらに強める）

### 入力情報の削減
- 入力はそのまま再現せず再構成する
- 主役を阻害する情報は積極的に削減する
- 削減優先順：装飾 → 質感 → 背景 → 色数 → 細部

## キーワード
- 推奨: loose watercolor washes, ink-stained edges, paper texture showing through, minimal linework with deliberate gaps
- 回避: thick impasto, heavy oil paint texture, fully rendered

## 例
- 良い例: "loose watercolor stains bleeding into paper surface, lines appearing only at key facial features with deliberate gaps and trailing ends"
- 悪い例: "gouache painting visually interpreted as matte opaque pigment layers"（油絵的すぎる）
