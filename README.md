# GAN

google colaboratory上で3種類のGAN(DCGAN, BEGAN, WGAN-gp)を実装しました。

google colaboratory以外の環境で実行するときは、
・先頭に!がついているshellコマンドは使えない
・パスの設定を適宜変更する
事に気を付ければOKです。

## 環境構築

google colaboratoryで実行する際には特に必要ありません。

##学習済みパラメータ

parameterファイルの中にいくつか学習済みパラメータがあります。
ただし指定されたモデルに対応しないパラメータを読み込むことはできません(e.g.BEGAN_face.prmをDCGANやWGAN-gpで用いることはできません)
また、対応するモデルでも、ネットワークの大きさや構造を変えてしまうと使えなくなるので気を付けでください。

##カラー画像 or グレースケール画像

本プログラムはカラー画像およびグレースケール画像の両方に対応していますが、in_dimの値を変更する必要があります。
```
nz=100
ngf=32
in_dim=3 #カラー画像なら3、グレースケール画像なら1を入力する

class GNet(nn.Module):
  def __init__(self):

```

