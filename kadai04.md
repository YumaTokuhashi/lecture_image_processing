 課題４　画像のヒストグラム
標準画像「https://www.jp.playstation.com/blog/20151112-gundambf-02.jpg 」を原画像とする．この画像は縦512画像，横512画素による正方形のディジタルカラー画像である．

ORG=imread('Lenna.png'); % 原画像の入力
ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換
imagesc(ORG); colormap(gray); colorbar;
![原画像](https://raw.githubusercontent.com/YumaTokuhashi/lecture_image_processing/master/1-1.bmp)  
図1 原画像の白黒濃淡画像

imhist(ORG); % ヒストグラムの表示

![原画像](https://raw.githubusercontent.com/YumaTokuhashi/lecture_image_processing/master/1-1.bmp)  
図2 ヒストグラム





