# naïve Bayes model和generative model的關係是?
老師:應該是說 naïve Bayes model 是 generative model 的一種，generative model 假設 data 來自某個 probabilistic distribution ，但至於這個 distribution 是什麼需要由人來決定，如果我們所選的 distribution 產生每個 feature 的機率是 independent 的，那我們用的是 naïve Bayes model

* [Anomaly Detection 看了之後就搞清楚老師講的1-D guassian distribution，重點在feature間是否相依，有相依就用Multivariate guassian，沒有就用1-D guassian] (https://marcovaldong.github.io/2016/04/11/Machine-Learning%E7%AC%AC%E4%B9%9D%E5%91%A8%E7%AC%94%E8%AE%B0%EF%BC%9A%E5%BC%82%E5%B8%B8%E6%A3%80%E6%B5%8B%E5%92%8C%E6%8E%A8%E8%8D%90%E7%B3%BB%E7%BB%9F/)

# model-playground

* keras玩玩
* pca是什麼東西
* L1 (python machine learning書上例子練習)
* L1 (kaggle/advanced house prices regression例子練習)
* L2 (python machine learning書上例子練習)

# cool demo

* https://arogozhnikov.github.io/2016/04/28/demonstrations-for-ml-courses.html


# corss-validation

From: Chun-Min Chang [mailto:cmchang@iis.sinica.edu.tw] 
Sent: Tuesday, December 20, 2016 5:19 PM
To: allen_chien / 簡嘉懋
Subject: Re: 投影片第46頁問題一問

Hi 你好,

一般會作 cross-validation 的原因是，擔心切 training/validation set 時會有 bias，所以才作 cross-validation 來避免這種情況。cross-validation 是協助驗證 model 表現的穩定性，而不是在尋找好的 model。

你說的沒錯，要做 cross-validation 會比較好，以免錯誤評估模型 :)

但大多時候 training NN 遇到的問題，都不是因為 cross-validation，而是 model 的架構不適合。加上 NN training 大多都需要一段時間，對一個架構就做 cross-validation 很耗時，所以我傾向於:
先切一份 training/validation set -> 用這份 training/validation set 找到一個好的網絡架構 -> 再做 cross-validation 驗證其穩定性。

希望有清楚的回答到你的問題 :)

Thanks,
Chun-Min Chang

2016-12-20 16:55 GMT+08:00 allen_chien / 簡嘉懋 <allen_chien@motech.com.tw>:
張老師 你好,
 
請問一下為何評估NN的架構沒有提到用Cross Validation K-Fold的方式
 
是否因為這整個過程太花時間，不如用直覺 + try and error能更快找到好的NN架構

