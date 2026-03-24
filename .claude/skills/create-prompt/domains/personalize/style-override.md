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
- 線は鉛筆で軽く描かれたような、柔らかく控えめな質感（共通と同じ）
- 線の太さや濃さに小さなばらつきを含める（共通と同じ）
- 純黒禁止（共通と同じ）
- 以下の点のみ共通と異なる：
  - 輪郭が部分的に途切れることを許容する（ただし主役の形状が読めなくなるほどの途切れは禁止）
  - 線が色面に溶け込む度合いがやや強い
- **以下は禁止（共通より厳しい制約）：**
  - 線が荒ぶる、走り書きのような勢いのある線は禁止
  - 線が完全に消えて形状が判別できなくなる箇所は禁止
  - 顔・手・衣装の構造線が省略されすぎて記号化することを禁止

### 色面と塗り
- 塗りは均一にせず、ムラ・にじみ・濃淡差を残す
- 色の境界がやや曖昧に混ざる
- 単色ベタ塗り禁止
- 水彩/インク的な「紙に染み込む」質感を基本とする
- 油絵的な不透明の重ねは控えめに（共通カプセルの「水彩×油絵ハイブリッド」より水彩寄り）
- **ただし色面だけで形が崩壊しないこと：**
  - 衣装や髪は省略しても、形の大枠が色面として読める状態を維持する
  - 色が流れすぎて何を描いているか分からなくなる状態は禁止

### 密度差（共通カプセルより差をつける）
- 顔周辺は高密度で明確に描写する
- 髪は束ではなく塊で処理する（ただし塊の境界は色の変化で読める程度に維持）
- 衣装は細部省略、面で扱う（ただし衣装の構造・層は読み取れる程度に維持）
- 背景は物体として描かず、色面の重なりとして扱う
- **密度差は「グラデーション的に」つける：**
  - 顔 → 髪・上半身 → 衣装の裾・手先 → 背景 の順で密度を落とす
  - どの部分でも急に「何も描かれていない」状態にはしない

### 入力情報の削減
- 入力はそのまま再現せず再構成する
- 主役を阻害する情報は削減する
- 削減優先順：装飾 → 質感 → 背景 → 色数 → 細部
- **ただし削減しすぎないこと：**
  - キャラクターの特徴的な要素（ヘッドホン、リボン等の識別要素）は残す
  - 衣装の層構造は最低2層が識別できる状態を維持する

## キーワード
- 推奨: soft watercolor washes, gentle ink edges, paper texture showing through, delicate linework with occasional gaps, controlled color bleeding
- 回避: thick impasto, heavy oil paint texture, fully rendered, rough sketch lines, scribbled linework, chaotic brushwork

## 例
- 良い例: "soft watercolor washes with gentle paper texture, delicate pencil-like lines with small natural gaps at non-critical edges, face and upper body rendered with clear detail gradually softening toward periphery"
- 悪い例: "rough sketch lines with aggressive gaps"（荒すぎる）、"loose scribble-like linework"（走り書き）
