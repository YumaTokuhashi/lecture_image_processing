課題２　階調数と疑似輪郭

標準画像「https://www.jp.playstation.com/blog/20151112-gundambf-02.jpg」を原画像とする．この画像は縦512画像，横512画素による正方形のディジタルカラー画像である．


ORG=imread('https://www.jp.playstation.com/blog/20151112-gundambf-02.jpg'); % 原画像の入力
ORG = rgb2gray(ORG); colormap(gray); colorbar;
imagesc(ORG); axis image; % 画像の表示
によって現画像をモノクロで読み込み、表示結果を図1に示す。

![原画像](https://raw.githubusercontent.com/YumaTokuhashi/lecture_image_processing/master/2-1.bmp)  
図1 原画像

２階調画像の生成
IMG = ORG>128;
imagesc(IMG); colormap(gray); colorbar;  axis image;

![原画像](https://raw.githubusercontent.com/YumaTokuhashi/lecture_image_processing/master/2-2.bmp)  
図2 2階調画像

% ４階調画像の生成
IMG0 = ORG>64;
IMG1 = ORG>128;
IMG2 = ORG>192;
IMG = IMG0 + IMG1 + IMG2;
imagesc(IMG); colormap(gray); colorbar;  axis image;
![原画像](https://raw.githubusercontent.com/YumaTokuhashi/lecture_image_processing/master/2-3.bmp)  
図3 4階調画像


IMG0 = ORG>32;
IMG1 = ORG>64;
IMG2 = ORG>96;
IMG3 = ORG>128;
IMG4 = ORG>160;
IMG5 = ORG>192;
IMG6 = ORG>224;
IMG = IMG0 + IMG1 + IMG2 + IMG3 + IMG4 + IMG5 + IMG6;
imagesc(IMG); colormap(gray); colorbar;  axis image;

![原画像](https://raw.githubusercontent.com/YumaTokuhashi/lecture_image_processing/master/2-4.bmp)  
図4 8階調画像

