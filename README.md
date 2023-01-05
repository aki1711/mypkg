# mypkg
![test](https://github.com/aki1711/mypkg/actions/workflows/test.yml/badge.svg)

## このリポジトリについて
このリポジトリはロボットシステム学の講義で使用したROS2のパッケージです。
`talker`と`listener`の2つのノード、`talk_listen.launch.py`というlaunchファイルが使用できます。

## インストール
* 以下のコマンドを実行して、リポジトリをクローンします。
```
$ git clone https://github.com/aki1711/mypkg.git
```

* そのあと、クローンしたリポジトリに移動します。
```
$ cd mypkg
```

## 実行方法(talker,listener)
`talker`:数字をカウントし、countupというトピックを通じてメッセージを送信します。

`listener`:countupからメッセージを受信し、表示します。
* まず、`talker`を実行します。
```
$ ros2 run mypkg talker
```

* 次に、別の端末で`listener`を実行します。
```
$ ros2 run mypkg listener
```

`listener`の実行結果は以下の通りです。
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

## 実行方法(launch)
launchファイルを使用することで、`talker`,`listener`2つのノードを一度に立ち上げることができます。

* 次のコマンドを実行します。
```
$ ros2 launch mypkg talk_listen.launch.py
```
実行結果は以下のとおりです。
```
[listener-2] [INFO] [1672921671.815461500] [listener]: Listen: 0
[listener-2] [INFO] [1672921672.291424700] [listener]: Listen: 1
[listener-2] [INFO] [1672921672.791102600] [listener]: Listen: 2
[listener-2] [INFO] [1672921673.291155000] [listener]: Listen: 3
[listener-2] [INFO] [1672921673.790726200] [listener]: Listen: 4
[listener-2] [INFO] [1672921674.291036900] [listener]: Listen: 5
[listener-2] [INFO] [1672921674.791428600] [listener]: Listen: 6
[listener-2] [INFO] [1672921675.290901700] [listener]: Listen: 7
[listener-2] [INFO] [1672921675.791202000] [listener]: Listen: 8
[listener-2] [INFO] [1672921676.291066500] [listener]: Listen: 9
[listener-2] [INFO] [1672921676.790190100] [listener]: Listen: 10
[listener-2] [INFO] [1672921677.290877000] [listener]: Listen: 11
[listener-2] [INFO] [1672921677.790889400] [listener]: Listen: 12
```
## 動作環境
* Ubuntu 20.04.5 LTS
* ROS2

## ライセンス
* このソフトウェアパッケージは，3条項BSDライセンスの下，再頒布および使用が許可されます.
* このパッケージのコードは，下記のスライド（CC-BY-SA 4.0 by Ryuichi Ueda）のものを，本人の許可を得て自身の著作としたものです．
    * [ryuichiueda/my_slides robosys_2022](https://github.com/ryuichiueda/my_slides/tree/master/robosys_2022)
* © 2022 Akiya Wakaumi
