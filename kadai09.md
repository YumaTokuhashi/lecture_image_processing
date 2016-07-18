課題９ メディアンフィルタと先鋭化
標準画像「https://www.jp.playstation.com/blog/20151112-gundambf-02.jpg 」を原画像とする．この画像は縦512画像，横512画素による正方形のディジタルカラー画像である．

ORG=imread('https://www.jp.playstation.com/blog/20151112-gundambf-02.jpg'); % 原画像の入力ORG = rgb2gray(ORG); % 白黒濃淡画像に変換
imagesc(ORG); colormap(gray); colorbar; % 画像の表示
![原画像](https://raw.githubusercontent.com/YumaTokuhashi/lecture_image_processing/master/9-1.bmp)  
図1 原画像の白黒濃淡画像
ORG = imnoise(ORG,'salt & pepper',0.02); % ノイズ添付
imagesc(ORG); colormap(gray); colorbar; % 画像の表示
![原画像](https://raw.githubusercontent.com/YumaTokuhashi/lecture_image_processing/master/9-2.bmp)  
図2 ノイズ添付
IMG = filter2(fspecial('average',3),ORG); % 平滑化フィルタで雑音除去
imagesc(IMG); colormap(gray); colorbar; % 画像の表示
![原画像](https://raw.githubusercontent.com/YumaTokuhashi/lecture_image_processing/master/9-3.bmp)  
図3 平滑化フィルタで雑音除去
IMG = medfilt2(ORG,[3 3]); % メディアンフィルタで雑音除去
imagesc(IMG); colormap(gray); colorbar; % 画像の表示
![原画像](https://raw.githubusercontent.com/YumaTokuhashi/lecture_image_processing/master/9-4.bmp)  
図4 メディアンフィルタで雑音除去
f=[0,-1,0;-1,5,-1;0,-1,0]; % フィルタの設計
IMG = filter2(f,IMG,'same'); % フィルタの適用
imagesc(IMG); colormap(gray); colorbar; % 画像の表示
![原画像](https://raw.githubusercontent.com/YumaTokuhashi/lecture_image_processing/master/9-5.bmp)  
図5 フィルタの適用
