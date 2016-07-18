課題10 画像のエッジ抽出 
標準画像「https://www.jp.playstation.com/blog/20151112-gundambf-02.jpg 」を原画像とする．この画像は縦512画像，横512画素による正方形のディジタルカラー画像である．

ORG=imread('https://www.jp.playstation.com/blog/20151112-gundambf-02.jpg'); % 原画像の入力  
ORG = rgb2gray(ORG); %カラーからグレイへの変換
imagesc(ORG); colormap('gray'); colorbar;% 画像表示
![原画像](https://raw.githubusercontent.com/YumaTokuhashi/lecture_image_processing/master/10-1.bmp)  
図1 原画像のグレー変換

IMG = edge(ORG,'prewitt'); % エッジ抽出（プレウィット法）
imagesc(IMG); colormap('gray'); colorbar;% 画像表示
![原画像](https://raw.githubusercontent.com/YumaTokuhashi/lecture_image_processing/master/10-2.bmp)  
図2 プレウィット法によるエッジ検出

IMG = edge(ORG,'sobel'); % エッジ抽出（ソベル法）
imagesc(IMG); colormap('gray'); colorbar;% 画像表示
![原画像](https://raw.githubusercontent.com/YumaTokuhashi/lecture_image_processing/master/10-3.bmp)  
図3 ソベル法によるエッジ検出


IMG = edge(ORG,'canny'); % エッジ抽出（キャニー法）
imagesc(IMG); colormap('gray'); colorbar;% 画像表示
![原画像](https://raw.githubusercontent.com/YumaTokuhashi/lecture_image_processing/master/10-4.bmp)  
図4 キャニー法によるエッジ検出



