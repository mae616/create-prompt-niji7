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

### 線の扱い（共通カプセルからの調整）
- 共通カプセル（art-style.md）の線質ルールを基本的に維持する
- 純黒禁止（共通と同じ）
- **パーソナライズ版の線の方向性：繊細で丁寧なペン画的質感**
  - 線は細く、繊細で、制御された筆致を基本とする
  - 細いペンや硬めの鉛筆で丁寧に描かれたような、落ち着いた線質
  - 線の太さにわずかな強弱はあるが、荒れや遊びは最小限に抑える
  - 髪の流れ、衣装の折り目、指の輪郭など、構造を伝える線は省略しすぎない
  - 線が色面に部分的に溶け込むことは許容するが、主要な構造線は視認できる状態を保つ
  - 線の途切れは背景や衣装の末端など重要度の低い箇所に限定する
- **以下は禁止：**
  - 線が荒ぶる、走り書きのような勢いのある線は禁止
  - 線が太くなりすぎる、ラフスケッチ的な筆致は禁止
  - 線が完全に消えて形状が判別できなくなる箇所は禁止
  - 顔・手・衣装の構造線が省略されすぎて記号化することを禁止

### 色面と塗り
- 水彩的な透明感と柔らかいにじみを基本とするが、にじみは上品に制御する
- 塗りは均一にせず濃淡差を残すが、色が大きく流れ出す・飛び散る表現は避ける
- 単色ベタ塗り禁止
- 油絵的な不透明の重ねは控えめに（共通カプセルの「水彩×油絵ハイブリッド」より水彩寄り）
- **にじみの制御（重要）：**
  - にじみ・色の飛沫は背景や余白に留め、キャラクター本体の形を崩さない
  - キャラクター内部の塗りは、形に沿った丁寧な着彩を基本とする
  - 衣装や髪の形の中で色がはみ出しすぎない
  - 色が流れすぎて何を描いているか分からなくなる状態は禁止

### 密度差（共通カプセルより差をつけるが、丁寧さを維持）
- 顔周辺は高密度で明確に描写する
- **髪は束の流れ・毛先のカーブが読める程度の描写を維持する**
  - 色の塊ではなく、柔らかい束が重なり合う構成
  - 束の境界は線と色の両方で示してよい
- **衣装は折り目・構造が読める程度の線と色面を維持する**
  - 完全な面の省略ではなく、折り目や重なりの線が柔らかく存在する
  - 衣装の端・裾に向かって徐々に情報を落とす
- 背景は物体として描かず、色面の重なりとして扱う
- **密度差は「グラデーション的に」つける：**
  - 顔 → 髪・上半身 → 衣装の裾・手先 → 背景 の順で密度を落とす
  - どの部分でも急に「何も描かれていない」状態にはしない
  - 密度を落とすとは「線を荒くする」ことではなく「描く要素を減らす」こと

### 入力情報の削減
- 入力はそのまま再現せず再構成する
- 主役を阻害する情報は削減する
- 削減優先順：装飾 → 質感 → 背景 → 色数 → 細部
- **ただし削減しすぎないこと：**
  - キャラクターの特徴的な要素（ヘッドホン、リボン等の識別要素）は残す
  - 衣装の層構造は最低2層が識別できる状態を維持する

## キーワード
- 推奨: fine delicate linework, thin controlled pen-like strokes, gentle watercolor washes, refined illustration quality, hair strands with soft flowing curves, carefully rendered facial features, neat clothing folds with soft lines, paper texture showing through in background
- 回避: thick impasto, heavy oil paint texture, fully rendered, rough sketch lines, scribbled linework, chaotic brushwork, loose messy lines, aggressive color bleeding over character forms

## 例
- 良い例: "fine delicate linework with thin controlled strokes, hair rendered as soft flowing strands with gentle curves, facial features carefully defined with refined detail, clothing folds drawn with light precise lines, gentle watercolor washes contained within forms, color bleeding limited to background and edges"
- 悪い例: "rough sketch lines with aggressive gaps"（荒すぎる）、"loose scribble-like linework"（走り書き）、"hair as abstract color masses"（髪が塊すぎる）
