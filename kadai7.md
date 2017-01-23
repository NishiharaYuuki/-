#課題７レポート
「gravure_41_mikarika.jpg」を原画像とする。

画素のダイナミックレンジを０から２５５にする。

![課題１](https://github.com/NishiharaYuuki/Matlab/blob/master/image/kadai7-1.png)

図１　原画像

![課題１](https://github.com/NishiharaYuuki/Matlab/blob/master/image/kadai7-2.png)

図２　濃度ヒストグラム

ORG = double(ORG);

mn = min(ORG(:)); % 濃度値の最小値を算出

mx = max(ORG(:)); % 濃度値の最大値を算出

ORG = (ORG-mn)/(mx-mn)*255;

imagesc(ORG); colormap(gray); colorbar; % 画像の表示

![課題１](https://github.com/NishiharaYuuki/Matlab/blob/master/image/kadai7-3.png)

図３　変更後画像

![課題１](https://github.com/NishiharaYuuki/Matlab/blob/master/image/kadai7-4.png)

図４　変更後濃度ヒストグラム
