# robosys2023_2

### ロボットシステム学 課題２

<br>

# ROS2

![test](https://github.com/nyantaro723/robosys2023_2/actions/workflows/test.yml/badge.svg)

<br>

## 使い方

ディレクトリ:

```bash
$ cd robosys2023_2/  
```  

<br>

* talkerとlistenerの２つのターミナルを使います。

<br>


* ① まず、端末１と端末２をそれぞれ開きます。

* ② 端末１には

```bash
$ ros2 run mypkg talker
```

と入力し、

* ③ 端末２には

```bash
$ ros2 run mypkg listener
```
 
と入力します。

* ④ 端末１と端末２の２つのターミナルを立ち上げると、

```bash
[INFO] [1703742678.270138053] [listener]: Listen: 0
[INFO] [1703742678.745021817] [listener]: Listen: 1
[INFO] [1703742679.245405478] [listener]: Listen: 2
[INFO] [1703742679.745058842] [listener]: Listen: 3
[INFO] [1703742680.245325938] [listener]: Listen: 4
[INFO] [1703742680.745370106] [listener]: Listen: 5
[INFO] [1703742681.245143670] [listener]: Listen: 6
[INFO] [1703742681.745156353] [listener]: Listen: 7
```

このようにlistener側に実行結果が出力されます。

<br>

* 止めたい場合は、[ctrl] + C を押す。

<br>

## 必要なソフトウェア

* Python
  * テスト済みバージョン: 3.7～3.10


## テスト環境

* Ubuntu 20.04

## 著作権・ライセンス
* このソフトウェアパッケージは，3条項BSDライセンス>の下，再頒布および使用が許可されます．

* このパッケージのコードは，下記のスライド（CC-BY-SA 4.0 by Ryuichi Ueda）のものを，本人の許可を得て自身の著作としたものです．
    * [ryuichiueda.github.io/my_slides robosys_2022](https://github.com/ryuichiueda/my_slides/tree/master/robosys_2022)

© 2023 Ryusei Matsuki
