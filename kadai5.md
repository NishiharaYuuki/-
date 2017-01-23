#課題５レポート

「gravure_41_mikarika.jpg」を原画像とする。

判別分析法を用いて画像二値化する。

![課題１](https://github.com/NishiharaYuuki/Matlab/blob/master/image/kadai5-1.png)

図１　原画像
H = imhist(ORG); %ヒストグラムのデータを列ベクトルEに格納

myu_T = mean(H);

max_val = 0;

max_thres = 1;

for i=1:255

C1 = H(1:i); %ヒストグラムを2つのクラスに分ける

C2 = H(i+1:256);

n1 = sum(C1); %画素数の算出

n2 = sum(C2);

myu1 = mean(C1); %平均値の算出

myu2 = mean(C2);

sigma1 = var(C1); %分散の算出

sigma2 = var(C2);

sigma_w = (n1 *sigma1+n2*sigma2)/(n1+n2); %クラス内分散の算出

sigma_B = (n1 *(myu1-myu_T)^2+n2*(myu2-myu_T)^2)/(n1+n2); %クラス間分散の算出

if max_val<sigma_B/sigma_w

max_val = sigma_B/sigma_w;

max_thres =i;

end;

end;

IMG = ORG > max_thres;

imagesc(IMG); colormap(gray); colorbar;

![課題１](https://github.com/NishiharaYuuki/Matlab/blob/master/image/kadai5-2.png)

図２　二値画像
