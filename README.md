# SRLatch in Minimalfab Contest 2024
セル設計やレイアウト設計に触れた経験がないことから、比較的なじみのあるラッチ回路かつ、複数種類の論理ゲートをそれぞれ複数個用いて設計する回路として、インバーター2つとNAND2つによって構成されるSRラッチを題材とした。

## Schematic ##
インバーターとNANDをそれぞれ単体で設計・動作検証を行い、それらを組み合わせてSRラッチの設計・動作検証を行った。今回はあえてシンボリック化を行っていない。
ツールはLTspice(Ver24.0.12)を用いた。
### inverter ###
![schematic_inverter](/images/schematic_inverter.png)

### NAND ###
![schematic_nand](/images/schematic_nand.png)

### SRLatch ###
真理値表
|S|R|Qnext|note|
|:---:|:---:|:---:|:---:|
|0|0|Qpre|hold|
|0|1|0|reset|
|1|0|1|set|
|1|1|--|unusable|

![schematic_srlatch](/images/schematic_SRLatch.png)

## *Layout* ##
PowerPointにてレイアウトの下書きを作成し、それに合わせて実際にレイアウトを行った。
ツールはKlayout(Ver0.29.10)を用いた。

![layout](/images/layout.png)

## *DRC* ##
![drc](/images/drc.png)
![drc_with_layout](/images/drc_with_layout.png)

## *LVS* ##
対応できておらず。後追いで実施予定。
