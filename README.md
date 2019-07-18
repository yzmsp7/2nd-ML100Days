# 2nd-ML100Days

![Marathon Flow](/marathon.png)

## Processing 資料清理前處理


## Feature Engineering 特徵工程

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

## Model Selection 模型選擇