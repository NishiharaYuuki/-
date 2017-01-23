#課題３レポート
「gravure_41_mikarika.jpg」を原画像とする。

閾値を4パターン設定し,閾値処理した画像を示す。


ORG=imread('gravure_41_mikarika.jpg'); % 原画像の入力

ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換

imagesc(ORG); colormap(gray); colorbar; % 画像の表示

これにより、原画像を入力し、カラー画像を白黒濃淡画像へ変換する

![課題１](https://github.com/NishiharaYuuki/Matlab/blob/master/image/kadai3-1.png)

図１　原画像

IMG = ORG > 64; % 輝度値が64以上の画素を1，その他を0に変換

imagesc(IMG); colormap(gray); colorbar;

![課題１](https://github.com/NishiharaYuuki/Matlab/blob/master/image/kadai3-2.png)

図２　閾値パターン１

IMG = ORG > 96;

imagesc(IMG); colormap(gray); colorbar;

![課題１](https://github.com/NishiharaYuuki/Matlab/blob/master/image/kadai3-3.png)

図３　閾値パターン２
IMG = ORG > 128;

imagesc(IMG); colormap(gray); colorbar;

![課題１](https://github.com/NishiharaYuuki/Matlab/blob/master/image/kadai3-4.png)

図４　閾値パターン３

IMG = ORG > 192;

imagesc(IMG); colormap(gray); colorbar;

![課題１](https://github.com/NishiharaYuuki/Matlab/blob/master/image/kadai3-5.png)

図５　閾値パターン４
