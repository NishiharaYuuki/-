#課題２レポート

元画像の２階調，４階調，８階調の画像を生成する。


ORG=imread('gravure_41_mikarika.jpg'); % 原画像の入力

ORG = rgb2gray(ORG); colormap(gray); colorbar;

imagesc(ORG); axis image; % 画像の表示

これにより、原画像を入力し、カラーをグレーに変更する。

図１　原画像


IMG = ORG>128;
imagesc(IMG); colormap(gray); colorbar;  axis image;

これにより、２階調画像の生成を行う。

図２　２階調画像


IMG0 = ORG>64;

IMG1 = ORG>128;
IMG2 = ORG>192;

IMG = IMG0 + IMG1 + IMG2;

imagesc(IMG); colormap(gray); colorbar;  axis image;

これにより、４階調画像の生成を行う。

図３　４階調画像

IMG0 = ORG>32;

IMG1 = ORG>64;

IMG2 = ORG>96;

IMG3 = ORG>128;

IMG4 = ORG>160;

MG5 = ORG>192;

IMG6 = ORG>224;

IMG = IMG0 + IMG1 + IMG2 + IMG3 + IMG4 + IMG5 + IMG6;

imagesc(IMG); colormap(gray); colorbar;  axis image;

これにより、８階調画像の生成を行う。

図４　８階調画像
