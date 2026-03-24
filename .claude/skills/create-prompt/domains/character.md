# キャラクター外観基礎

## メタデータ
- priority: 4
- conflicts: []

## ルール

### 基本方針
- この段階では形状・色相傾向・素材構造のみを定義する
- 画風・塗り方・線質は決定しない（art-style.mdが最優先で決定する）
- キャラクターの服装やジャンルでの連想によって画風が固定されることを禁止する

### 出力形式
- 日本語・箇条書き
- 具体色名は使用するが、色コードは禁止

### 定義する要素

#### 外見カテゴリ（生物的特徴）
- 人間／猫型特徴を持つ人物／兎型特徴を持つ人物 等、カテゴリを明示する
- 必ず直後に物理的特徴を具体的に記述する
- ジャンル的連想語（獣人系、萌え系 等）は禁止

例:
```
猫型特徴を持つ人物
→ 頭部に三角形の耳があり、耳は頭頂よりやや外側に配置
  細長い尾を持つ、体毛は持たない
```

#### 必須定義項目
- 年齢帯
- 髪色（具体色名）
- 髪の長さと外形
- 目の色（具体色名）
- 衣装色（最低3色）
- レイヤー数（最低2層）
- 異素材要素を1点以上含める

### 可変幅の確保
- 色の明度・彩度は固定しない
- 面積比を数値で固定しない
- 構図は指定しない
- 光の当たり方は指定しない

### 最低保証
- 単色衣装は禁止
- 無彩色のみは禁止
- 最低3系統以上の色相を含める

### ジャンル依存禁止
- ロリータ、ゴスロリ、制服系などのジャンルラベルは禁止
- 衣装は必ず構造と素材で記述する

### 画風優先前提
- この設定は素材情報のみを提供する
- 画風・塗り・線質は決定しない

## キーワード
- 外見記述: triangular ears on top of head, slender tail, no body fur
- 衣装記述: layered clothing structure, mixed material elements
- 回避: kemonomimi, furry, moe, anime-style, lolita, gothic（ジャンルラベル禁止）

## 例
- 良い例: "a young woman with triangular cat ears positioned slightly outward from the crown, a long slender tail, no visible body fur, shoulder-length silver hair, deep green eyes, two-layer outfit with thin long-sleeve top under loose cardigan, small suede elbow patch as mixed material accent"
- 悪い例: "a cute catgirl in a gothic lolita dress"（ジャンルラベルに依存している）
