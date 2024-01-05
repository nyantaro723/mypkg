# mypkg

### ロボットシステム学 課題２

* このパッケージは、ROSを使って、プロセス間の通信を行うものです。

<br>

![test](https://github.com/nyantaro723/mypkg/actions/workflows/test.yml/badge.svg)

## talker (パブリッシャ)

* 実行すると、0.5秒ごとにトピック'countup'を通じて数字を1ずつ増やしていきます。

## listener (サブスクライバ)

* 実行すると、トピック'countup'からメッセージを受け取り、ターミナルにログを表示します。

## トピック (countup)

* トピックとは、ノード間でやり取りするデータのことであり、メッセージの型は16ビット符号付き整数です。

## talk_listen.launch.py

* １つのターミナルで実行すると、talkerとlistenerを同時に起動することのできるlaunchファイルです。

<br>

## 使い方

### talker、listener

* talkerとlistenerの２つのターミナルを使います。

* ① まず、端末１と端末２をそれぞれ開きます。

* ② 端末１には

```bash
$ ros2 run mypkg talker
```

と入力し、

<br>

* ③ 端末２には

```bash
$ ros2 run mypkg listener
```
 
と入力します。

<br>

* ④ 端末１と端末２の２つのターミナルを立ち上げると、

```bash
[INFO] [1703753586.608854575] [listener]: Listen: 0
[INFO] [1703753587.093214417] [listener]: Listen: 1
[INFO] [1703753587.579861711] [listener]: Listen: 2
[INFO] [1703753588.091398360] [listener]: Listen: 3
[INFO] [1703753588.581506718] [listener]: Listen: 4
[INFO] [1703753589.088387901] [listener]: Listen: 5
[INFO] [1703753589.582173126] [listener]: Listen: 6
[INFO] [1703753590.092315223] [listener]: Listen: 7
```

上のようにlistener側に実行結果が出力されます。

<br>

* 閉じたい場合は、[ctrl] + C を押します。

<br>

### launch

* launchでは、１つのターミナルで実行します。

* 下のように入力すると、１つの端末でtalkerとlistenerの２つが同時に立ち上がります。

```bash
ros2 launch mypkg talk_listen.launch.py
```

と入力すると、下のような実行結果が出力されます。 

```bash
[listener-2] [INFO] [1703759848.957369808] [listener]: Listen: 0
[listener-2] [INFO] [1703759849.386230316] [listener]: Listen: 1
[listener-2] [INFO] [1703759849.894976106] [listener]: Listen: 2
[listener-2] [INFO] [1703759850.381963480] [listener]: Listen: 3
[listener-2] [INFO] [1703759850.921031700] [listener]: Listen: 4
[listener-2] [INFO] [1703759851.383820970] [listener]: Listen: 5
[listener-2] [INFO] [1703759851.887930155] [listener]: Listen: 6
[listener-2] [INFO] [1703759852.420304231] [listener]: Listen: 7
```

* 閉じる手順は上と同様です。

## 必要なソフトウェア

* Python
  * テスト済みバージョン: 3.7～3.10

* ROS2 foxy

## テスト環境

* Ubuntu 20.04

## 著作権・ライセンス
* このソフトウェアパッケージは，3条項BSDライセンス>の下，再頒布および使用が許可されます．

* このパッケージのコードは，下記のスライド（CC-BY-SA 4.0 by Ryuichi Ueda）のものを，本人の許可を得て自身の著作としたものです．
    * [ryuichiueda.github.io/my_slides robosys_2022](https://github.com/ryuichiueda/my_slides/tree/master/robosys_2022)

© 2023 Ryusei Matsuki
