# ROSパッケージの作り方

## ROSチュートリアルの流れ

1. [ROSパッケージの作り方](how_to_create_pkg.md) ←今ここ
2. [トピックの書き方](how_to_write_topic.md)
3. [独自のメッセージファイルの作り方](how_to_create_msg.md)
4. [まとめて起動するやり方](how_to_use_launch.md)
5. [サービスの書き方](how_to_write_service.md)
6. [独自のサービスファイルの作り方](how_to_create_srv.md)

## はじめに

ROSチュートリアルでは、実際にROSパッケージを作成し、独自のカスタマイズをしてみたいと思います。

パッケージとは、目的に沿ったプログラムなどの集合体であり、開発はパッケージ単位で行われます。

## ROSパッケージを作る

ROSパッケージは`catkin_ws/src`の中で作成するため、`catkin_ws/src`に移動しましょう。

```text
cd ~/catkin_ws/src
```

ではROSパッケージを作っていきましょう。

まずコマンドの説明をします。

```text
<例>　catkin_create_pkg <パッケージ名> std_msgs rospy roscpp
```

`catkin_create_pkg`はパッケージを作成するときに用いるcatkinコマンドです。

std\_msgsとrospy、roscppは依存パッケージであり、以下のようになっています。

* std\_msgs : 標準のメッセージの型
* rospy : pythonをROSで使用するときに必要になるモジュール
* roscpp : C++をROSで使用するときに必要になるモジュール

今回は`ros_tutorial`というパッケージ名にします。以下のコマンドを実行してください。

```text
catkin_create_pkg ros_tutorial std_msgs rospy roscpp
```

`catkin_ws`に移動し、`catkin_make`をします。

```text
cd ../
catkin_make
```

`catkin_make`とは、`catkin_ws/src`にあるパッケージをビルドするときに使用します。 またパッケージを追加した時や、**C++**のプログラムを追加・変更したときも行います。

