課題６　画像の二値化
標準画像「https://www.jp.playstation.com/blog/20151112-gundambf-02.jpg 」を原画像とする．この画像は縦512画像，横512画素による正方形のディジタルカラー画像である．

clear; % 変数のオールクリア
ORG=imread('https://www.jp.playstation.com/blog/20151112-gundambf-02.jpg'); % 原画像の入力  
ORG = rgb2gray(ORG);
imagesc(ORG); colormap(gray); colorbar; % 画像の表示
![原画像](https://raw.githubusercontent.com/YumaTokuhashi/lecture_image_processing/master/6-1.bmp)  
図1 原画像


IMG = ORG>128; % 128による二値化
imagesc(IMG); colormap(gray); colorbar; % 画像の表示
pause;
![原画像](https://raw.githubusercontent.com/YumaTokuhashi/lecture_image_processing/master/6-2.bmp)  
図2 128による二値化

IMG = dither(ORG); % ディザ法による二値化
imagesc(IMG); colormap(gray); colorbar; % 画像の表示
![原画像](https://raw.githubusercontent.com/YumaTokuhashi/lecture_image_processing/master/6-3.bmp)  
図3 ディザ法による二値化

