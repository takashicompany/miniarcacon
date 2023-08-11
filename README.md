# miniArcacon

<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/01.jpg?raw=true" width = "600px" />

<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/02.jpg?raw=true" width = "300px" /><img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/03.jpg?raw=true" width = "300px" />

「miniArcacon(ミニアケコン)」ポケットに入れて持ち運べるレバーレスのアケコンです。  
薄く小さいため持ち運びが容易となっております。  

コンパクトながらも実用に耐えうるボタン配置となっております。  

ファームウェアはGP2040-CE等を導入することができ、多様なデバイスやプラットフォームでゲームを楽しむことができます。


## 組み立てに必要なもの

### 道具

迷った場合は[遊舎工房さんの工具セット](https://shop.yushakobo.jp/products/a9900to)を購入すると良いかと思います。  
以下の道具も基本的には上述のセットを抜粋したリストとなります。

|道具|備考|
|:--|:--|
|ハンダごて|おすすめは[HAKKO FX-600](https://www.hakko.com/japan/products/hakko_fx600.html)です。[こて台](https://www.hakko.com/japan/products/hakko_kote_board.html)もあると、より作業をスムーズに進められます。|
|ハンダ|[こちら](https://www.goot.jp/products/detail/se_06008)などを使う方が多いようです。|
|ピンセット|100均などで手に入るものでも充分利用できるかと思います。|
|ニッパー|100均などで手に入るものでも充分利用できるかと思いますが、1000円程度ものを買っても損では無いかと思います。|

### キットに含まれている部品

|部品|個数|備考|
|:--|:--|:--|
|miniArcacon基板|1||
|スイッチプレート|1||
|ミドルプレート|2||
|ボトムプレート|1||
|ネジ(M2 8mm)|8||
|ナット(M2)|8||
|[タクタイルスイッチ](https://shop.yushakobo.jp/products/a0800ts-01-1)|8||
|[ゴム足シール](https://shop.yushakobo.jp/products/a0800ur-01-6)|6||

### ご自身で用意いただく部品

|部品|個数|備考|
|:--|:--|:--|
|[RP2040-Zero](https://talpkeyboard.net/items/640ea9f3072c3c538731c515)|1||
|[Kailh Choc v1 スイッチ]([https://shop.yushakobo.jp/products/cherry-mx](https://shop.yushakobo.jp/collections/all-switches/kailh-choc-v1%E3%82%B9%E3%82%A4%E3%83%83%E3%83%81)https://shop.yushakobo.jp/collections/all-switches/kailh-choc-v1%E3%82%B9%E3%82%A4%E3%83%83%E3%83%81)|12||
|0.8u(16mm)狭ピッチキーキャップ|12||
|USB-C|1||

## 組み立て方

### 1. 基板の表裏を確認する

表  
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_5139.jpg?raw=true" width = "600px" />

裏  
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_5140.jpg?raw=true" width = "600px" />

### 2. MCU(RP2040-Zero)の取り付け

MCU(Micro Controller Unit)とは、アケコンの頭脳部分です。キーの入力をPCやゲーム機に送信します。  
miniArcaconでは、「RP2040-Zero」を用います。  
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_5141.jpg?raw=true" width = "600px" />

基板にRP2040-Zeroを載せます。基板の穴とRP2040-Zeroの穴の位置が揃うように置きます。  
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_5142.jpg?raw=true" width = "600px" />

位置がズレないようにマスキングテープで固定すると作業がスムーズに進められます。  
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_5143.jpg?raw=true" width = "600px" />

基板とRP2040-Zeroをハンダ付けします。  
RP2040-Zeroの穴ではなく、穴の外の縁をハンダ付けします。  
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_5144.jpg?raw=true" width = "600px" />

以下の写真のように基板の縁部分と基板がハンダで結合されているようにします。
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_5145.jpg?raw=true" width = "600px" />

RP2040-Zeroのハンダ付け部分を全て基板にハンダ付けしたら完了です。  
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_5146.jpg?raw=true" width = "600px" />

### 3. ファームウェアの書き込み

ファームウェアは[GP2040-CE](https://gp2040-ce.info/#/)を使用します。

[公式のインストール方法](https://gp2040-ce.info/#/installation)

[こちら](https://gp2040-ce.info/#/download)からRP2040-Zero用のファームウェアをダウンロードしてください。

RP2040-Zeroに備え付けられたBootボタンを確認してください。
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_5146.jpg?raw=true" width = "600px" />

**Bootボタンを長押ししたまま**RP2040-ZeroとPC/ゲーム機をUSBで接続します。  
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_5148.jpg?raw=true" width = "600px" />

外部ドライブとして「RPI-RP2」が表示されていることを確認します。  
<img src = "https://github.com/takashicompany/miniarcacon/assets/4215759/82e003e2-39a8-4dd5-a1a8-4bf3ccc9573b" width = "600px" />

このRPI-RP2に先程ダウンロードしたファームウェア(.uf2)をドラッグアンドドロップをします。  
<img src = "https://github.com/takashicompany/miniarcacon/assets/4215759/9e1ed5f0-506c-472b-bd95-357e8104897d" width = "600px" />

[こちらのサイト](https://hardwaretester.com/gamepad)で入力の確認ができます。  
<img src = "https://github.com/takashicompany/miniarcacon/assets/4215759/fe9534cc-9ea3-4471-a5b0-33a5fea8e025" width = "600px" />


ピンセット等を使って、RP2040-Zeroのハンダ付けが正常に行われているかを確認します。  
写真と同様に2つの穴を通電させて、入力がされているかを確認します。  
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_5450.jpg?raw=true" width = "600px" />

上述のサイトでのキー入力のマッピングは以下になります。  
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_5265_2.jpg?raw=true" width = "600px" />

### 4. タクトスイッチの取り付け

タクトスイッチはオプションボタンなどが割り当てられています。  
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_5155.jpg?raw=true" width = "600px" />

タクトスイッチは基板表側の右奥側に取り付けます。表側にスイッチの上部が来るようにタクトスイッチの足を基板の穴に差し込みます。  
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_5157.jpg?raw=true" width = "600px" />

合計8個取り付けます。  
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_5158.jpg?raw=true" width = "600px" />

各タクトスイッチの足が基板の裏側から出ていることを確認します。  
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_5159.jpg?raw=true" width = "600px" />

タクトスイッチの足と基板をハンダ付けします。  
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_5160.jpg?raw=true" width = "600px" />

### 5. スイッチプレートとキースイッチの取り付け

キースイッチを基板に取り付けます。  
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_5241.jpg?raw=true" width = "600px" />

キースイッチを取り付ける際は、スイッチプレートを用います。  
スイッチプレートに保護シートが付いている場合は剥がしてください。上手く剥がれない場合は、ピンセットを使う・水で軽く濡らすなどすると剥がしやすくなります。  
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_5152.jpg?raw=true" width = "600px" />

スイッチプレートにキースイッチを数個差します。  
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_5242.jpg?raw=true" width = "600px" />

キースイッチを差したスイッチプレートを基板の表側に載せます。  
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_5243.jpg?raw=true" width = "600px" />

基板の裏側から、キースイッチの足が穴を通って出ていることを確認します。  
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_5245.jpg?raw=true" width = "600px" />

以下の画像の赤丸の箇所(キースイッチの足と基板)をハンダ付けします。  
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_5245_2.jpg?raw=true" width = "600px" />

全部で12個のキースイッチをハンダ付けします。  
スイッチプレートが基板とキースイッチで固定されていることを確認します。  
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_5246.jpg?raw=true" width = "600px" />

### 6. ミドルプレートとボトムプレートの取り付け

ミドルプレートとボトムプレートに保護シートが貼られている場合は剥がします。  

ミドルプレート  
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_5154.jpg?raw=true" width = "600px" />

ボトムプレート  
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_5153.jpg?raw=true" width = "600px" />

ミドルプレートを取り付けます。  
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_5253.jpg?raw=true" width = "600px" />

ミドルプレートを基板の裏側に載せます。  
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_5254.jpg?raw=true" width = "600px" />

ボトムプレートをミドルプレートに重ねます。  
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_5255.jpg?raw=true" width = "600px" />

スイッチプレートとミドルプレートとボトムプレートをネジとナットで固定します。  
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_5252.jpg?raw=true" width = "600px" />

ネジ穴にネジを表側から通します。  
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_5256.jpg?raw=true" width = "600px" />

裏側からネジをナットで固定します。  
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_5257.jpg?raw=true" width = "600px" />

８箇所を固定したら完了です。  
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_5260.jpg?raw=true" width = "600px" />

### 7. ゴム足シールの取り付け

底面にゴム足シールを貼り付けます。  
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_5261.jpg?raw=true" width = "600px" />

取付箇所はお好みやプレースタイルなどで調整してください。  
以下は取り付け例です。  
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_5262.jpg?raw=true" width = "600px" />

### 8. キーキャップの取り付け  

キーキャップを取り付けて完成です。  
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_5265_2.jpg?raw=true" width = "600px" />

<!--
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_.jpg?raw=true" width = "600px" />
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_.jpg?raw=true" width = "600px" />

<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_.jpg?raw=true" width = "600px" />
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_.jpg?raw=true" width = "600px" />

<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_.jpg?raw=true" width = "600px" />

<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_.jpg?raw=true" width = "600px" />

<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_.jpg?raw=true" width = "600px" />

<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_.jpg?raw=true" width = "600px" />

<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_.jpg?raw=true" width = "600px" />
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_.jpg?raw=true" width = "600px" />

<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_.jpg?raw=true" width = "600px" />
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_.jpg?raw=true" width = "600px" />

<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_.jpg?raw=true" width = "600px" />
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_.jpg?raw=true" width = "600px" />

<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_.jpg?raw=true" width = "600px" />
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_.jpg?raw=true" width = "600px" />

<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_.jpg?raw=true" width = "600px" />
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_.jpg?raw=true" width = "600px" />

<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_.jpg?raw=true" width = "600px" />
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_.jpg?raw=true" width = "600px" />

<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_.jpg?raw=true" width = "600px" />
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_.jpg?raw=true" width = "600px" />

<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_.jpg?raw=true" width = "600px" />
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_.jpg?raw=true" width = "600px" />

<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_.jpg?raw=true" width = "600px" />
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_.jpg?raw=true" width = "600px" />

<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_.jpg?raw=true" width = "600px" />
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_.jpg?raw=true" width = "600px" />

<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_.jpg?raw=true" width = "600px" />
<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_.jpg?raw=true" width = "600px" />

<img src = "https://github.com/takashicompany/miniarcacon/blob/master/images/build/IMG_.jpg?raw=true" width = "600px" />

-->
