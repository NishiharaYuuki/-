#課題９レポート
「gravure_41_mikarika.jpg」を原画像とする。

メディアンフィルターを適用し，ノイズ除去を体験する。

![課題１](https://github.com/NishiharaYuuki/Matlab/blob/master/image/kadai9-1.png)

図１　原画像

ORG = imnoise(ORG,'salt & pepper',0.02); % ノイズ添付

imagesc(ORG); colormap(gray); colorbar; % 画像の表示

![課題１](https://github.com/NishiharaYuuki/Matlab/blob/master/image/kadai9-2.png)

図２　ノイズ添付画像

IMG = filter2(fspecial('average',3),ORG); % 平滑化フィルタで雑音除去

imagesc(IMG); colormap(gray); colorbar; % 画像の表示

![課題１](https://github.com/NishiharaYuuki/Matlab/blob/master/image/kadai9-3.png)

図３　雑音除去画像

IMG = medfilt2(ORG,[3 3]); % メディアンフィルタで雑音除去

imagesc(IMG); colormap(gray); colorbar; % 画像の表示

![課題１](https://github.com/NishiharaYuuki/Matlab/blob/master/image/kadai9-4.png)

図４　雑音除去画像

f=[0,-1,0;-1,5,-1;0,-1,0]; % フィルタの設計

IMG = filter2(f,IMG,'same'); % フィルタの適用

imagesc(IMG); colormap(gray); colorbar; % 画像の表示

![課題１](https://github.com/NishiharaYuuki/Matlab/blob/master/image/kadai9-5.png)

図５　フィルタ適用画像
