#課題８レポート
「gravure_41_mikarika.jpg」を原画像とする。

二値化された画像の連結成分にラベルをつける。

図１　原画像

図２　二値化画像

IMG = bwlabeln(IMG);

imagesc(IMG); colormap(jet); colorbar; % 画像の表示

図３　ラベル付け画像
