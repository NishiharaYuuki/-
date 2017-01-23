#課題６レポート
「gravure_41_mikarika.jpg」を原画像とする。

二階調、ディザ法によって画像を二値化する。

図１　原画像

IMG = ORG>128; % 128による二値化

imagesc(IMG); colormap(gray); colorbar; % 画像の表示

図２ 128による二値化画像

IMG = dither(ORG); % ディザ法による二値化

imagesc(IMG); colormap(gray); colorbar; % 画像の表示

図３　ディザ法による二値化画像
