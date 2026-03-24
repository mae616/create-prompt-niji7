# glass-pen-vivid

<!--
  ガラスペン×鮮やか透明水彩スタイル
  パーソナライズ版のデフォルトテイスト（繊細ペン画＋控えめ水彩）をベースに、
  線のインク感と水彩の発色を強化したバリエーション。
-->

## 概要
ガラスペン/つけペンのインクの質感が見える線と、発色の良い鮮やかな透明水彩の組み合わせ。
デフォルトのパーソナライズ版より「線にインクの存在感」「色に鮮やかさ」を加える。

## 上書き対象
- 線質: style-override.md / art-style.md の線質ルールを部分的に上書き
- 色面・塗り: style-override.md / painterly-texture.md の塗りルールを部分的に上書き
- 密度: style-override.md の密度ルールを部分的に上書き（細部の描き込みを増やす方向）

## 線質

### ガラスペン/つけペンのインク線
- 線はガラスペンやつけペンで引いたような、**インクの物質感が見える**線質にする
- 描き始めにインクがわずかに溜まり、引くにつれて先細りする自然なインクの流れ
- 筆圧による太さの変化が明確に出る（デフォルトの「わずかな強弱」より変化幅を大きくする）
- インクの色は純黒ではなく、周囲の色に馴染むダークトーン（共通ルール維持）
- 線の途切れ・かすれはデフォルトより少なく、構造線がしっかり視認できる状態を保つ

### デフォルトとの違い
- デフォルト: 「細く控えめなペン画的質感、線は補助」
- このスタイル: 「インクの溜まり・先細り・筆圧変化が見える、線に存在感がある」
- ただし線が主役になるわけではない（色面構造は維持する）

### 禁止（デフォルトと同じ）
- 荒ぶる線、走り書き的な線は禁止
- 均一な太さのデジタル線は禁止
- 純黒の線は禁止

## 色面・塗り

### 鮮やかな透明水彩
- デフォルトの「上品で控えめなにじみ」から、**発色が良くクリアな透明水彩**に調整する
- 顔料の彩度を上げ、色が生き生きとしている状態にする
- 透明水彩の特徴（下の色が透ける層の重なり）は維持するが、各層の色がよりはっきり見える
- くすみ・ダスティ系の色相は禁止しないが、彩度を1段階上げて「鮮やかなくすみ」にする
  - 例: ダスティローズ → ローズピンク、淡いレモンイエロー → 明るいレモンイエロー

### にじみの扱い
- にじみは制御するが、デフォルトよりわずかに色の広がりを許容する
- 背景の水彩染みも発色良く、クリアな色味にする
- キャラクター本体の形を崩さないルールは維持

### 禁止
- 油絵的な不透明の重ねは最小限（デフォルトより制限を強化）
- 均一なデジタル塗り禁止
- 色が流れすぎて形が崩れることは禁止

## 密度・細部

### 描き込みの強化
- デフォルトより細部の描き込みを1段階上げる
- **髪**: 個々の束がインクの線で分離され、毛先のカールまで一束ずつ読める
- **目**: 虹彩内の色相の層が見える程度の描写
- **衣装**: 縫い目・ボタン・プリーツなど構造的ディテールを追加する
- **団子等の小物**: 質感や色の違いが個別に読める

### 密度差のグラデーション
- デフォルトと同じく顔→髪→衣装→背景の順で落とす
- ただし全体のベースラインが1段階上がるので、衣装の端でもある程度の描き込みが残る

## キーワード
- 推奨: glass-pen-style ink lines, visible ink pooling at stroke starts, tapering thin ends, natural ink flow variation, slight thickness changes from pressure, vivid transparent watercolor, clear pigment saturation, individually defined strands, layered chroma shifts inside iris, visible stitching detail, button closures
- 回避: thin controlled pen-like strokes（デフォルトのキーワードをこのスタイル時は使わない）, faint washes（発色が弱すぎる）, gentle color transitions（色変化が控えめすぎる）, dusty（くすみが強すぎる）

## 例
- 良い例: "glass-pen-style ink lines with visible ink pooling at stroke starts and tapering thin ends showing natural ink flow variation, vivid transparent watercolor with clear pigment saturation, hair with individually defined soft strands separated by fine ink lines"
- 悪い例: "bold ink outlines"（太すぎる）、"faint gentle washes"（発色が弱すぎる）、"rough calligraphy strokes"（荒すぎる）
