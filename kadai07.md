課題7　ダイナミックレンジの拡大
標準画像「https://www.jp.playstation.com/blog/20151112-gundambf-02.jpg 」を原画像とする．この画像は縦512画像，横512画素による正方形のディジタルカラー画像である．

ORG=imread('https://www.jp.playstation.com/blog/20151112-gundambf-02.jpg'); % 原画像の入力  
ORG = rgb2gray(ORG); % 白黒濃淡画像に変換
imagesc(ORG); colormap(gray); colorbar; % 画像の表示
![原画像](https://raw.githubusercontent.com/YumaTokuhashi/lecture_image_processing/master/7-1.bmp)  
図1 原画像の白黒濃淡画像
imhist(ORG); % 濃度ヒストグラムを生成、表示
![原画像](https://raw.githubusercontent.com/YumaTokuhashi/lecture_image_processing/master/7-2.bmp)  
図2 図1の濃度ヒストグラム
ORG = double(ORG);
mn = min(ORG(:)); % 濃度値の最小値を算出
mx = max(ORG(:)); % 濃度値の最大値を算出
ORG = (ORG-mn)/(mx-mn)*255;
imagesc(ORG); colormap(gray); colorbar; % 画像の表示
![原画像](https://raw.githubusercontent.com/YumaTokuhashi/lecture_image_processing/master/7-3.bmp)  
図3 ダイナミックレンジ拡大
ORG = uint8(ORG); % この行について考察せよ
imhist(ORG); % 濃度ヒストグラムを生成、表示
![原画像](https://raw.githubusercontent.com/YumaTokuhashi/lecture_image_processing/master/7-4.bmp)  
図4 図3の濃度ヒストグラム
