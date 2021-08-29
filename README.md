# Unity uGUI アドバンスド・リファレンス

## ダウンロード方法

[Unity_uGUI_Advanced_Reference.pdf](https://github.com/heppoko/Unity_uGUI_Advance_Reference/blob/main/Unity_uGUI_Advanced_Reference.pdf) の Download ボタンを押す（GitHub のプレビューではうまく表示できない）

## 対象読者

本書は Unity の uGUI の基本原理を深く理解したいと願う読者のために書かれている。もし、すぐに効果が出る Tips や便利な UI アセットの紹介を期待しているのであれば、残念ながら期待外れになるかもしれない。だが、こんな経験はないだろうか？

- 便利な UI アセットが特定のプラットフォームに対応していない

- Unity のバージョンを上げたら便利な UI アセットが動かなくなった

- 何もしていないのに便利な UI アセットが動かなくなった

本書の内容を理解することで、そのような状況に遭遇した場合でも落ち着いて対応ができるようになるだろう。

また、本書の内容はパフォーマンス改善のためにも非常に役に立つはずである。たとえば、uGUI でのパフォーマンス最適化の手法としては

- Canvas を分割する

- 無駄な RaycastTarget を減らす

- Camera.main の利用を避ける

- Auto Layout の Layout Group をなるべく使わないようにする

- Animation や Timeline で UI をアニメーションさせない

などが一般的に知られている。本書を通読した暁には、それらの手法がなぜ有効なのかの理由を理解することができるようになるだろう。

本書では uGUI のコンポーネントのプロパティや public メソッドの解説を記述してある。これらの解説は公式リファレンスのコピーではなく、著者がソースコードを確認した上で実際に呼び出して挙動を検証を経た結果である。さらに、顕著な *GC Alloc* が発生する場合には注釈を入れている。これにより、公式リファレンスでは得られない詳細な挙動を知ることができるはずである。

プログラミング言語やゲームエンジンなどのミドルウェアを深く理解する方法として、リファレンスやソースコードを一通り全部読むという方法は非常に有用である。本書を全部読破することで uGUI のみならず Unity 全般への深い理解が得られるだろう。

## 対象 Unity バージョン

本書は基本的には Unity 2020.2 を前提に書かれている。もっとも、それ以前から追加されていた uGUI の新機能についても随時触れていくつもりである。たとえば、Unity 2020.1 で導入された `Mask` コンポーネントのソフトマスク（端をぼかす機能）や UI シェーダーの乗算済み透明、レイキャスト領域のパディングなどについては知らない読者もいるかもしれない。本書を通じてそういった新機能についても学ぶことができる。

## ライセンス

本書のサンプルコードは、Unity uGUI 由来のものもオリジナルのものも全て Unity uGUI のライセンスの下で頒布する。Unity uGUI のライセンス については Unity UI Package の LICENSE を参照のこと。大抵の場合は製品内で Unity uGUI のライセンス表記も行っているはずなので特別なことをする必要はないだろう。

## 目次

### Chapter 1 Canvas と関連コンポーネント

- Canvas の概要
- Canvas コンポーネント
- CanvasScaler コンポーネント
- GraphicRaycaster コンポーネント
- CanvasGroup コンポーネント
  
### Chapter 2 UI 要素と Canvas のリビルド

- UIBehaviour クラス
- RectTransform コンポーネント
- スマートデバイスで可変解像度を実現する
- CanvasRenderer コンポーネント
- Graphic 関連コンポーネント
- Canvas リビルド

### Chapter 3 レンダリング

- Unity における描画順
- レンダリングのパフォーマンス改善
- シェーダー
- テクスチャフォーマット
- テクスチャのインポート設定
- RenderTexture
- 画面解像度

### Chapter 4 Graphic

- Graphic コンポーネント
- VertexHelper クラス
- MaskableGraphic コンポーネント
- タッチイベントを吸収する透明なレイヤーを作成する

### Chapter 5 画像とエフェクト
- RawImage と Image の使い分け
- RawImage コンポーネント
- Image コンポーネント
- Shadow コンポーネント
- Outline コンポーネント
- PositionAsUV1 コンポーネント
- Mask コンポーネント
- RectMask2D コンポーネント

### Chapter 6 Text とフォント

- Text コンポーネント
- TextGenerator クラス
- フォントアセット
- TrueTypeFontImporter クラス
- TextMesh Pro
- TextMeshProUGUI コンポーネント

### Chapter 7 Selectable

- Selectable
- Button コンポーネント
- Toggle コンポーネント
- ToggleGroup コンポーネント
- Slider コンポーネント
- Dropdown コンポーネント
- InputField コンポーネント
- Scrollbar コンポーネント

### Chapter 8 Scroll View

- ScrollRect コンポーネント
- Scroll View のコンテンツの設定方法

### Chapter 9 Auto Layout

- Auto Layout の概要
- Layout Element のサイズ決定ルール
- Layout Element コンポーネントによる手動サイズ調整
- Layout Controller
- Layout Group
- RectTranform のドリブンプロパティ
- 独自の Auto Layout コンポーネントの作成
- レイアウトの計算
- Layout リビルドのトリガー
- ILayoutElement インターフェース
- ILayoutController インターフェース
- ILayoutSelfController インターフェース
- ILayoutIgnorer インターフェース
- LayoutElement コンポーネント
- LayoutGroup コンポーネント
- HorizontalOrVerticalLayoutGroup コンポーネント
- HorizontalLayoutGroup コンポーネント
- VerticalLayoutGroup コンポーネント
- GridLayoutGroup コンポーネント
- ContentSizeFitter コンポーネント
- AspectRatioFitter コンポーネント
- Auto Layout ではなく Anchor を活用する

### Chapter 10 EventSystem

- EventSystem コンポーネント
- Messaging System
- InputModule
- StandaloneInputModule コンポーネント
- BaseInput
- Event Trigger コンポーネント
- Raycaster
- GraphicRaycaster
- PhysicsRaycaster コンポーネント
- Physics2DRaycaster コンポーネント
- StandaloneInputModule の拡張
- 
### Chapter 11 プロファイリング

- uGUI の プロファイリングツール
- Unity Profiler
- Frame Debugger
- CPU Usage エリアの解析と原因のパターン

