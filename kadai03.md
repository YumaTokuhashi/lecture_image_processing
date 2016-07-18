課題３　閾値処理

標準画像「https://www.jp.playstation.com/blog/20151112-gundambf-02.jpg 」を原画像とする．この画像は縦512画像，横512画素による正方形のディジタルカラー画像である．

ORG=imread('Lenna.png'); % 原画像の入力
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換

imagesc(ORG); colormap(gray); colorbar; % 画像の表示
![原画像](https://raw.githubusercontent.com/YumaTokuhashi/lecture_image_processing/master/3-1.bmp)  
図1 原画像の白黒濃淡画像

IMG = ORG > 64; % 輝度値が64以上の画素を1，その他を0に変換
imagesc(IMG); colormap(gray); colorbar;
![原画像](https://raw.githubusercontent.com/YumaTokuhashi/lecture_image_processing/master/3-2.bmp)  
図2 閾値64

IMG = ORG > 96;
imagesc(IMG); colormap(gray); colorbar;
![原画像](https://raw.githubusercontent.com/YumaTokuhashi/lecture_image_processing/master/3-3.bmp)  
図3 閾値96

IMG = ORG > 128;
imagesc(IMG); colormap(gray); colorbar;
![原画像](https://raw.githubusercontent.com/YumaTokuhashi/lecture_image_processing/master/3-4.bmp)  
図4 閾値128

IMG = ORG > 192;
imagesc(IMG); colormap(gray); colorbar;
![原画像](https://raw.githubusercontent.com/YumaTokuhashi/lecture_image_processing/master/3-5.bmp)  
図5 閾値192
