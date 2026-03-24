# パーソナライズ版：色彩・配色・背景 上書き

<!--
  このカプセルはパーソナライズ版（/create-prompt-p）でのみ読み込まれる。
  共通カプセル coloring.md / composition.md の一部ルールを上書きする。
-->

## メタデータ
- priority: 9
- conflicts: []
- overrides: [coloring, composition]

## 上書きルール

### 白背景の扱い（共通カプセルからの変更）
- 共通カプセルでは「白背景禁止」だが、パーソナライズ版では以下を許容する：
  - **紙の地**として白が大きく残ることを許容する
  - ただし「白い壁」「白い空間」としてではなく、「塗り残された紙の地」として扱う
  - 色面が浮遊するように存在し、紙の地がその間を埋める構成
- 白背景＝「何も描かなかった」ではなく「描かないことを選んだ余白」として解釈する

### 背景の構成
- 写真的なボケ表現禁止
- 実在空間の再現ではなく、色面として構成する
- 背景は物体として描かない → 色面の重なりとして扱う
- 背景の高密度描写は禁止

### 影色（共通と同じだが強調）
- 影は灰色ではなく、必ず別色相を混ぜる（共通と同じ）
- 影色は「染み」のように自然に発生した状態として扱う

### 光の扱い
- 光は形を読む補助に留める
- 顔に強い光パターンを乗せない
- 白飛びや強い帯光を避ける
- 光はあくまで色面の明度差として表現する

### 色相バランス（共通からの調整）
- 共通カプセルの面積比ルール（主色60%/副色25%/アクセント10-15%）は目安として維持
- ただしパーソナライズ版では「紙の地（白）」が大きな面積を占めることを許容する
- 色面の面積が少なくても、存在感のある色なら成立する

## キーワード
- 推奨: paper ground showing through, floating color planes, watercolor stains on white, selective rendering
- 回避: photographically blurred background, detailed environmental rendering, white wall, white room

## 例
- 良い例: "sparse watercolor stains floating on exposed paper ground, background existing only as faint color washes"
- 悪い例: "detailed background with depth"（背景の高密度描写）
