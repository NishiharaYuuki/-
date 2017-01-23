#課題８レポート
「gravure_41_mikarika.jpg」を原画像とする。

二値化された画像の連結成分にラベルをつける。

![課題１](https://github.com/NishiharaYuuki/Matlab/blob/master/image/kadai8-1.png)

図１　原画像

![課題１](https://github.com/NishiharaYuuki/Matlab/blob/master/image/kadai8-2.png)

図２　二値化画像

IMG = bwlabeln(IMG);

imagesc(IMG); colormap(jet); colorbar; % 画像の表示

![課題１](https://github.com/NishiharaYuuki/Matlab/blob/master/image/kadai8-3.png)

図３　ラベル付け画像
