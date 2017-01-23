#課題１０レポート
「gravure_41_mikarika.jpg」を原画像とする。

次のプログラムを参考にして、エッジ抽出を体験する。

![課題１](https://github.com/NishiharaYuuki/Matlab/blob/master/image/kadai10-1.png)

図１　原画像

IMG = edge(ORG,'prewitt'); % エッジ抽出（プレウィット法）

imagesc(IMG); colormap('gray'); colorbar;% 画像表示

![課題１](https://github.com/NishiharaYuuki/Matlab/blob/master/image/kadai10-2.png)

図２　エッジ抽出（プレウィット法）　

IMG = edge(ORG,'sobel'); % エッジ抽出（ソベル法）

imagesc(IMG); colormap('gray'); colorbar;% 画像表示

![課題１](https://github.com/NishiharaYuuki/Matlab/blob/master/image/kadai10-3.png)

図３　エッジ抽出（ソベル法）　

IMG = edge(ORG,'canny'); % エッジ抽出（キャニー法）

imagesc(IMG); colormap('gray'); colorbar;% 画像表示

![課題１](https://github.com/NishiharaYuuki/Matlab/blob/master/image/kadai10-4.png)

図４　エッジ抽出（キャニー法）
