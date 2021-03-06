# 画像処理100本ノック!!

画像処理の初学者のための問題１００問。

これは画像処理の基本的処理の知識を身に着け、アルゴリズムを理解するための100本ノックです。

ここに載っている問題はOpenCVでAPIが用意されているものが殆どですが、あえてそれを自分の手で実装してください。

**まだ作成中なので、随時更新していきます。なので問題の難易度の順番もめちゃくちゃです。**

**なるべくポピュラーなものを採用していますが、たまにネタ切れであんまり聞かないものもあります笑**

## Recent

**【New!】2019.1.9. Q.47-50 モルフォロジー処理　を追加**

## 環境設定

Python-3.6でやって下さい。
(解答はPython-3.6です)

### 1. Minicondaのインストール

https://conda.io/miniconda.html
のサイトからMinicondaをインストールします。

Minicondaがインストールできたら、以下コマンドで仮想環境を作成します。

```bash
$ conda create python=3.6 -n gasyori100
```

作成できたら、以下コマンドで仮想環境を動作します。

```bash
$ source actiavte gasyori100
```

するとこうなります。

```bash
(gasyori100) :~/work_space/Gasyori100knock/ :$ 
```

### 2. パッケージのインストール

以下のコマンドで必要なパッケージをインストールします。


```bash
$ pip install -r requirement.txt
```

### 3. 画像処理チュートリアル

以下のファイルを作成し sample.py という名前で保存し、実行します。

```python
import cv2

img = cv2.imread("assets/imori.jpg")
cv2.imshow("imori", img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

```bash
$ python sample.py
```

これで以下の画像が表示されれば成功です！
何かボタンを押せば消えます。


![](assets/sample.png)

次に画像処理に関するnumpyの扱い方のために**Tutorial**フォルダを見てみて下さい。（もう知ってるという人はスキップして下さい。）

これからは問題を解いていってください。それぞれのフォルダに問題内容が入っています。
問では assets/imori.jpg を使用して下さい。

- チュートリアル >> Tutorial
- 問題1-10  >> Quetion_01_10
- 問題11-20 >> Question_11_20
- 問題21-30 >> Question_21_30
- 問題31-40 >> Question_31_40
- 問題41-50 >> Question_41_50
- 問題51-60 >> Question_51_60
- 問題61-70 >> Question_61_70
- 問題71-80 >> Quesiton_71_80
- 問題81-90 >> Question_81_90
- 問題91-100 >> Question_91_100


## 注意

- 本稿は画像処理の基礎的な知識・理論を学ぶための教材です。
- 解答ではなるべくコードを簡易化するために、main( )などを使用してしません。
- numpyを使用しますが、numpyに関する基本知識は載せません。各自調べて下さい。


## 問題

- 無印は画像処理をやる上での基礎知識
- &#9734;は応用問題。基礎を組み合わせて、実際に論文で用いられるような手法の理解

**未**になっている問題は解答未作成

|番号|問題|備考||番号|問題|備考|
|:---:|:---|:---:|:---:|:---:|:---|:---:|
|1|チャネル入れ替え|  ||21|ヒストグラム正規化 |
|2|グレースケール化 | ||22|ヒストグラム操作 |
|3|二値化 | || 23|ヒストグラム平坦化 |
|4|大津の二値化 | || 24|ガンマ補正|
|5|HSV変換 | ||25|最近傍補間|
|6|減色処理 | ||26|Bi-linear補間|
|7|平均プーリング | ||27|Bi-cubic補間|
|8|Maxプーリング | ||28|アフィン変換(平行移動)|
|9|ガウシアンフィルタ | ||29|アフィン変換(拡大縮小)|
|10|メディアンフィルタ | ||30|アフィン変換(回転)|
|11|平滑化フィルタ | ||31|アフィン変換(スキュー)|
|12|モーションフィルタ | ||32**未**|フーリエ変換 ||
|13|MAX-MINフィルタ | ||33**未**|フーリエ変換 ローパスフィルタ|
|14|微分フィルタ | ||34**未**|フーリエ変換 ハイパスフィルタ|
|15|Sobelフィルタ | ||35**未**|フーリエ変換 バンドパスフィルタ|
|16|Prewittフィルタ | || 36&#9734;| **JPEG圧縮** (Step.1)離散コサイン変換 |
|17|Laplacianフィルタ | ||37| PSNR|
|18|Embossフィルタ | ||38&#9734;| **JPEG圧縮**(Step.2)DCT+量子化|
|19|LoGフィルタ | ||39|**JPEG圧縮**(Step.3)YCbCr表色系|
|20|ヒストグラム表示 ||| 40&#9734;|**JPEG圧縮**(Step.4)YCbCr+DCT+量子化 |


|番号|問題|備考||番号|問題|備考|
|:---:|:---|:---:|:---:|:---:|:---|:---:|
| 41&#9734; | **Cannyエッジ検出** (Step.1) エッジ強度 |
| 42&#9734; | **Cannyエッジ検出** (Step.2) 細線化 |
| 43&#9734; | **Cannyエッジ検出** (Step.3) ヒステリシス閾処理 |
| 44&#9734; | **Hough変換・直線検出** (Step.1) Hough変換 |
| 45&#9734; | **Hough変換・直線検出** (Step.2) NMS |
| 46&#9734; | **Hough変換・直線検出** (Step.3) Hough逆変換 |
| 47 |モルフォロジー処理(膨張) |
| 48 |モルフォロジー処理(収縮) |
| 49 |オープニング処理 |
| 50 |クロージング処理 |

## TODO

Hough, Gabor, HOG

## 注意

このページを利用して、または関して生じた事に関しては、私は一切責任を負いません。
すべて**自己責任**でお願い致します。
"# Gasyori100knock" 
"# Gasyori100knock" 
"# Gasyori100knock" 
