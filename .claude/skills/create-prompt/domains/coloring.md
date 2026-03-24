# 色彩・配色

## メタデータ
- priority: 7
- conflicts: []

## ルール

### 基本方針
- 彩度を意図的に抑えることは目的にしない
- 色は十分な存在感を持たせ、画面内で生きている状態を優先する
- 鮮やかさは「強弱」や「密度」で制御し、彩度そのものを一律に下げない
- 白飛びや過剰な発光表現による色抜けは避ける
- 色は整理されていても、無難にまとまりすぎない配色を許容する

### 色面による空間成立
- 明度差だけでなく、色相差によって形が認識できること
- 線がなくても、色面だけで大まかな構造が読み取れること
- 色が薄い・少ない・限定的な場合でも「線画として成立している状態」にはしない
- 配色が決まらない場合は、彩度を下げる方向ではなく色層を増やす方向で調整する
- 色面が先に認識され、その上に線が補助的に存在する構成を必ず維持する
- 線だけで画面が成立する状態にならない

### 色相バランス制御
#### 面積比
- 主色 約60%
- 隣接色 約25%
- 補色アクセント 10〜15%
- それ以上の分散禁止

#### 彩度
- 背景は主役より低彩度
- 最高彩度は焦点周辺のみ
- 全体高彩度禁止

#### 影色
- 影は隣接または補色を微量混合
- 単色影禁止
- 影色は「その物の色を暗くしたもの」として扱わず、別の色相がわずかに混ざった状態として解釈してよい
- 髪の影に黄緑、灰紫、くすんだ青などが微量に混ざってよい
- 服や小物の影にも周囲の空気色が侵食することを許容する

#### 禁止
- 単一色相支配
- 全面補色対立
- 均一高コントラスト

### 配色指定における誤解防止ルール
- 「落ち着いた」「穏やか」「暖色寄り」などの表現は、彩度を下げる・色数を減らす・単色化する指示として解釈しない
- 落ち着きは「彩度の低下」ではなく、色相差・明度差・密度差の整理によって表現する
- 暖色寄りの配色であっても、寒色や中間色を補助色として必ず画面内に含める（主張せず、空気や影、奥行きとして使用）
- 穏やかなコントラストとは、明度差を消すことではなく、極端な白黒対比を避けることを意味する

### 彩度の分散
- 彩度の高さは主役だけに集中させず、画面内に分散させることで全体の圧を下げる
- 高彩度部分は、形やディテールを整理することで視認性を保つ

### 色の逸脱と主役色の侵食
- 主役色は対象の外に静かに滲み出して構わない
- その侵食に物語的・論理的な理由付けは不要
- 色は支配せず、あくまで痕跡や残り香のように存在させる
- 一部の色は光源や物理的正しさではなく、感情・空気感・偶然によって置かれているように見せてよい
- 局所的に「なぜこの色がここにあるのか」一瞬考えさせる色のズレを許容する

### 肌の影の解釈
- 肌の影は血色や立体説明を最優先にせず、絵の具が溜まった結果として現れているように扱う
- 肌の影に必ずしも赤みや暖色を入れなくてよい
- くすんだ色、濁り、偶然混ざった色が残っていても構わない
- ただし顔の可愛さや表情の読み取りは損なわないよう制御する

### 禁止事項
- 無彩色のみの配色は禁止
- 白背景は禁止
- 色面で空間が成立する前提を保つ

### 統合プロンプトへの必須追加文
以下をプロンプト生成時に必ず含める：
- color harmony controlled by dominant hue with adjacent support and limited complementary accent
- dominant hue covering majority area
- secondary hue supporting without equal saturation
- small complementary accent restricted to focal zone
- background saturation lower than subject

## キーワード
- 推奨: layered colors, color-defined forms, chromatic depth, visible color planes, shadow mixed with secondary hue
- 回避: monochrome, desaturated, white background, flat color, uniform digital shading

## 例
- 良い例: "forms defined by overlapping warm and cool color planes, shadow mixed with muted orange into teal-based forms, color harmony controlled by dominant hue with adjacent support and limited complementary accent"
- 悪い例: "simple flat colors on white background"、"shadows are just darker versions of base color"
