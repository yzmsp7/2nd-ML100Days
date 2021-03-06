
# 第二屆機器學習百日馬拉松 2nd-ML100Days

![Marathon Flow](/marathon.png)

## 資料清理數據前處理

[[Day1]資料介紹與評估資料](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_001_HW.ipynb)

[[Day2]讀取資料EDA: Data summary](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_002_HW.ipynb)

[[Day3]如何新建一個 dataframe?如何讀取其他資料? (非 csv 的資料)](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_003_HW.ipynb)

[[Day4]EDA: 欄位的資料類型介紹及處理](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_004_HW.ipynb)

	- 拿到資料的第一步，通常就是看我們有什麼，觀察有什麼欄位，這些欄位代表什麼意義、以什麼樣的資料類型來儲存
	- 資料原來是字串/類別的話，如果要做進⼀步的分析時（如訓練模型），⼀般需要轉為數值的資料類型，轉換的⽅式通常有兩種
		• Label encoding：使用時機通常是該資料的不同類別是有序的，例如該資料是年齡分組，類別有⼩孩、年輕⼈、老人，表⽰示為 0, 1, 2 是合理理的，因為年齡上老人 > 年輕人 > 小孩
		• One Hot encoding：使用時機通常是該資料的不同類別是無序的，例如國家

[[Day5]EDA資料分佈](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_005_HW.ipynb)

[[Day6]EDA與Outlier檢查]()

[[Day7]常用數值取代：中位數與分位數連續數值標準化]()

## 資料科學特徵工程技術

[[Day23]類別型特徵 - 均值編碼](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_023_HW.ipynb)  

[[Day24]類別型特徵 - 其他進階處理理](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_024_HW.ipynb)  

[[Day25]時間型特徵](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_025_HW.ipynb) 

[[Day26]特徵組合 - 數值與數值組合](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_026_HW.ipynb)  

	- 數值與數值的特徵組合，最關鍵的部分是領域知識
	- 機器學習的關鍵是特徵工程，當然其餘部分仍然很重要，但是各部分都熟悉之後，最有效提升模型預測⼒的部分就是特徵工程

[[Day27]特徵組合 - 類別與數值組合](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_027_HW.ipynb)  

	- 類別特徵與數值特徵，可以使⽤用群聚編碼組合出新的特徵
	- 群聚編碼最常使⽤用的運算是 mean, 除此之外還有median、mode、max、min、count等統計量量可以使⽤
	- 用群聚編碼與之前的均值編碼最主要的差異異，⼀個是特徵彼此之間與特徵⽬目標值之間的差異異，另⼀個最⼤的差異是 : 
	群聚編碼因為與目標值無關，因此不容易Overfitting，也因此比均值編碼使⽤頻率高得多


[[Day28]特徵選擇](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_028_HW.ipynb)  

	- 相對於特徵組合在增加特徵，特徵選擇就是在減少特徵
	- 特徵選擇主要包含：過濾法(Filter)、包裝法(Wrapper)與嵌入法(Embedded)
	- 特徵選擇中，計算時間較長，但是能排除共線性且比較穩定的方式是梯度提升樹嵌入法

[[Day29]特徵評估](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_029_HW.ipynb)  

	- 樹狀狀模型的特徵重要性，可以分為分⽀次數、特徵覆蓋度、損失函數降低量三種
	- sklearn 樹狀狀模型與 Xgboost 的特徵重要性，最大差異就是在sklearn 只有精準度最低的「分⽀支次數」
	- 特徵重要性本身的重要性，是在於本⾝身是增刪特徵的重要判定準則，在領域知識不⾜時，成為改善模型的最⼤幫手

[[Day30]分類型特徵優化 - 葉編碼](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_030_HW.ipynb)  

	- 多個分類預測結果，需要先將機率到推回對應數值，相加後再由sigmoid函數算回機率，類似邏輯斯回歸的算法
	- 葉編碼的目的是重新標記資料，以擬合後的樹狀模型分歧條件，將資料離散化，這樣比人為寫作的判斷條件更精確，更符合資料的分佈情形
	- 葉編碼完後，因為特徵數量較多，通常搭配邏輯斯回歸或者分解機做預測，其他模型較不適合

## 機器學習基礎模型建立

[[Day31]機器學習概論](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_031_HW.ipynb)

[[Day32]機器學習-流程與步驟](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_032_HW.ipynb)

[[Day33]機器如何學習？](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_033_HW.ipynb)

[[Day34]訓練/測試集切分的概念](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_034_HW.ipynb)

[[Day35]Regression vs. Classification](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_035_HW.ipynb)

[[Day36]評估指標選定](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_036_HW.ipynb)

	- 評估指標選擇
	    - 回歸問題：R-square
		- 類問題(二元)：AUC
		- 想特別觀察哪一類：F1-Score
		- 分類問題(多元)：top-k 
	- AUC 計算時填入每個樣本預測機率
	- F1-Score則是每個以分類結果機率>0.5視為1

[[Day37]Regression 模型](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_037_HW.ipynb)

[[Day38]Regression 模型-程式碼](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_038_HW.ipynb)

[[Day39]LASSO, Ridge Regression](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_039_HW.ipynb)

	- 為避免overfitting，我們可以加入正規化，目標函數＝損失函數＋正規化
	- 正規化可以懲罰模型的複雜度，當模型越複雜期值越大
	- LASSO＝Linear Regression + L1
	- Ridge＝Linear Regression + L2
	- LASSO之所以可以當作特徵選取的工具，是因為他是以參數稀疏化來做訓練的，因此某些特徵最後權重會變成0，達成特徵選取之功用

[[Day40]LASSO, Ridge Regression-程式碼](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_040_HW.ipynb)

[[Day41]決策樹](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_041_HW.ipynb)

	- 透過一系列的是非問題，幫助我們將資料進行切分
	- 衡量資料相似程度可以用Gini&Entropy
	- 我們可以從構建樹的過程中，透過feature被用來切分的次數來判斷哪些feature是相對有用的

[[Day42]決策樹 - 程式碼撰寫](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_042_HW.ipynb)

[[Day43]隨機森林](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_043_HW.ipynb)

	- 為了解決決策樹容易overfitting的缺點，以決策樹為基底延伸的模型
	- 隨機森林的每一棵樹在生成過程中，都是隨機使用一部分的訓練資料和特徵

[[Day44]隨機森林 - 程式碼撰寫](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_044_HW.ipynb)

[[Day45]梯度提升機](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_045_HW.ipynb)

	- RandomForest是每棵獨立的樹，前一棵樹不會影響下一棵樹
	- GradientBoosting是為了修正前一棵樹，每一棵樹都是關聯的

[[Day46]梯度提升機 - 程式碼撰寫](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_046_HW.ipynb)
## 機器學習調整參數

[[Day47]超參數調整](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_047_HW.ipynb)

	- 超參數都會影響模型訓練的結果，建議先用預設值再慢慢調整
	- 但超參數提升效果有限，最重要的還是資料清理與特徵工程
	- 超參數調整方法
		- 窮舉(Grid Search)
		- 隨機搜尋(Random Search)

[[Day48]Kaggle 競賽平台介紹](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_048_HW.ipynb)

[[Day49]混合泛化(Blending)](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_049_HW.ipynb)

[[Day50]堆疊泛化(Stacking)](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_050_HW.ipynb)

	- 堆疊泛化將模型預測當作特徵時，要避免「要編碼」的資料與訓練編碼器的資料重疊，因此設計上看起來相當複雜
	- 堆疊泛化理論上在堆疊層數上沒有限制，但如果第一層的單模不夠複雜，堆疊二三層後改善幅度就有限了
	- 混合泛化相對堆疊泛化來說，優點在於容易使用，曲點在於無法更深入地利用資料，進一步混合模型

## 非監督式機器學習

[[Day54]非監督式機器學習簡介](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_054_HW.ipynb)

	- 在不清楚資料特性、問題定義、沒有標記的情況下，非監督式學習可以幫助我們理清資料脈絡
	- 特徵數太龐大的晴望下，非監督式學習可以幫著概念抽象化，用更簡潔的特徵描述資料
	- 非監督式學習以具類算法以及降維度算法為主

[[Day55]K-means聚類算法](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_056_HW.ipynb)

	- 當問題不清楚或是資料未有標注的情況下，可以嘗試用分群算法幫助了解資料結構，而其中一個方法是運用K-means聚類算法幫助分群資料
	- 分群算法需要事先定一群數，因此評估效果只能藉由人為觀察

[[Day56]K-mean 觀察:使⽤用輪輪廓分析](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_056_HW.ipynb)

	- 輪廓分數是一種同群資料點越近 / 不同群資料點越遠時會越⼤的分數，除了可以評估資料點分群是否得當，也可以用來評估分群效果
	- 要以輪廓分析觀察 K-mean，除了可以將每個資料點分組觀察以評估資料點分群是否得當，也可⽤平均值觀察評估不同 K 值的分群效果

[[Day57]階層分群算法](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_057_HW.ipynb)

	- 階層式分群在無需定義群數的情況下做資料的分群，而後可以⽤不同的距離定義⽅式決定資料群組。
	- 分群距離計算方式有single-link, complete-link, average-link。
	- 概念簡單且容易呈現，但不適合用在⼤資料。

[[Day58]階層分群法觀察:使⽤2D樣版資料集](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_058_HW.ipynb)

	- 了解2D樣板資料集的設計著重於圖形的人機差異，用途在讓人眼以非量化的方式評估非監督模型的好壞，也因為非監督問題的類型不同，這類資料集也有分群與流形還原等不同對應類型
	- 2D樣版資料集很多套件都有，也不限於只有Python上使用的套件：如 sklearn/mathworks/mlbench 都有對應的datasets

[[Day59]降維方法：主成份分析](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_059_HW.ipynb)

	- 降低維度可以幫助我們壓縮及丟棄無用資訊、抽象化及組合新特徵、呈現高維數據。常用的算法為主成份分析
	- 在維度太大發生overfitting的情況下，可以嘗試用PCA組成的特徵來做監督式學習，但不建議一開始就做

[[Day60]PCA觀察：使用手寫辨識資料集](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_060_HW.ipynb)

[[Day61]降維方法：t-SNE](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_061_HW.ipynb)

	- 特徵間為非線性關係時(e.g. 文字、影像資料)，PCA容易underfitting
	- t-SNE對於特徵非線性資料有更好的降維能力

[[Day62] t_SNE觀察：分群與流形還原](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_062_HW.ipynb)

	- 流形還原就是在高維度到低維度的對應中，盡量保持資料點之間的遠近關係，沒有資料點的地方，就不列入考量範圍 
	- 除了 t-sne 外，較常見的流形還原還有 Isomap 與 LLE(Locally Linear Embedding) 等⼯具
	
## 初探深度學習 - 使用Keras

[[Day63]深度學習簡介](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_063_HW.ipynb)

	- 深度學習不僅在深度高於類神經，因著算法改良、硬體能力提升以及巨量量資料等因素，已經成為⽬前最熱門的技術
	- 不同的深度學習架構適用於不同種類的應⽤，如卷積神經網路(CNN)適⽤於影像處理，遞歸神經網路(RNN)適用於⾃然語言處理，⾄今這些架構仍在持續演進與改良
	- 深度神經網路巨觀結構來看，包含輸入層/隱藏層/輸出層等層次，局部則是由啟動函數轉換輸出，藉由預測與實際值差距的損失函數，⽤倒傳遞方式更新權重，以達成各種應用的學習目標

[[Day64]深度學習體驗](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_064_HW.ipynb)

	- 雖然圖像化更直覺，但是並非量化指標且可視化不容易，故深度學習的觀察指標仍以損失函數/誤差為主
	- 對於不同資料類型，適合加深與加寬的問題都有，但加深適合的問題類型較多
	- 輸入特徵的選擇影響結果甚巨，因此深度學習也需要考慮特徵工程

[[Day65]深度學習體驗:啟動函數與正規化](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_065_HW.ipynb)

	- 批次大小越小：學習曲線越不穩定、但收斂越快
	- 學習速率越大：學習曲線越不穩定、但收斂越快，但是與批次大小不同的是：學習速率大於一定以上時，可能不穩定到無法收斂
	- 當類神經網路層數不多時，啟動函數 Sigmoid/ Tanh 的效果比 Relu 好
	- L1/L2 正規化在非深度學習上效果較明顯，而正規化參數較小才有效果

[[Day66]Keras安裝與介紹](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_066_HW.ipynb)

	- Keras是將TensorFlow等後端程式封裝並優化，易學易用的深度學習基礎套件

[[Day67]Keras Embedded Dataset介紹與應用](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_067_HW.ipynb)

## 深度學習應用卷積神經網路
