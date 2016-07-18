課題８ ラベリング
標準画像「https://www.jp.playstation.com/blog/20151112-gundambf-02.jpg 」を原画像とする．この画像は縦512画像，横512画素による正方形のディジタルカラー画像である．

ORG=imread('https://www.jp.playstation.com/blog/20151112-gundambf-02.jpg'); % 原画像の入力 
ORG = rgb2gray(ORG); % 白黒濃淡画像に変換
imagesc(ORG); colormap(gray); colorbar; % 画像の表示
![原画像](https://raw.githubusercontent.com/YumaTokuhashi/lecture_image_processing/master/8-1.bmp)  
図1 原画像の白黒濃淡画像
IMG = ORG > 128; % 閾値128で二値化
imagesc(IMG); colormap(gray); colorbar; % 画像の表示
![原画像](https://raw.githubusercontent.com/YumaTokuhashi/lecture_image_processing/master/8-2.bmp)  
図2 閾値128で二値化
IMG = bwlabeln(IMG);
imagesc(IMG); colormap(jet); colorbar; % 画像の表示
![原画像](https://raw.githubusercontent.com/YumaTokuhashi/lecture_image_processing/master/8-3.bmp)  
図3 ラベリング
