# mypkg
![test](https://github.com/aki1711/mypkg/actions/workflows/test.yml/badge.svg)

## このリポジトリについて
このリポジトリはロボットシステム学の講義で使用したROS2のパッケージです。
talkerとlistenerの2つのノード、talk_listen.launch.pyというlaunchファイルが使用できます。

## インストール
* 以下のコマンドを実行して、リポジトリをクローンします。
```
$ git clone https://github.com/aki1711/mypkg.git
```

* そのあと、クローンしたリポジトリに移動します。
```
$ cd mypkg
```

## 実行方法
* まず、talkerを実行します。
```
$ ros2 run mypkg talker
```

* 次に、別の端末でlistenerを実行します。
```
$ ros2 run mypkg listener
```

listenerの実行結果は以下の通りです。
```
[INFO] [1672921294.806359800] [listener]: Listen: 82
[INFO] [1672921295.287612000] [listener]: Listen: 83
[INFO] [1672921295.787640400] [listener]: Listen: 84
[INFO] [1672921296.287317700] [listener]: Listen: 85
[INFO] [1672921296.786769600] [listener]: Listen: 86
[INFO] [1672921297.287236600] [listener]: Listen: 87
[INFO] [1672921297.787193800] [listener]: Listen: 88
[INFO] [1672921298.287389800] [listener]: Listen: 89
[INFO] [1672921298.787014000] [listener]: Listen: 90
[INFO] [1672921299.287348000] [listener]: Listen: 91
[INFO] [1672921299.787459200] [listener]: Listen: 92
```

## 動作環境
* Ubuntu 20.04.5 LTS
* ros2

## ライセンス
* このソフトウェアパッケージは，3条項BSDライセンスの下，再頒布および使用が許可されます.
* このパッケージのコードは，下記のスライド（CC-BY-SA 4.0 by Ryuichi Ueda）のものを，本人の許可を得て自身の著作としたものです．
    * [ryuichiueda/my_slides robosys_2022](https://github.com/ryuichiueda/my_slides/tree/master/robosys_2022)
* © 2022 Akiya Wakaumi
