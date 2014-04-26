---
layout: post
category : open data
author: vincentlaucy
author_url: https://twitter.com/vincent_lcy
title: "立法會投票光譜"
tagline: "開放數據分析"
tags : [code4hk, opendata, legco]
---
{% include JB/setup %}


##立法會投票光譜 - 開放數據分析

關心時事的朋友可能有留意《立法會重要表決紀錄》網站 （<u>www.legcovotes.net</u>）的設立，令議員政黨取態一目了然。

可是類似的網站數據需要人手輸入，費時失事。上年年底立法會正式發佈投票結果的開放數據，其XML格式較其他資料如會議紀綠的PDF較適合電腦處理(Machine-readable)，令市民及新聞工作者更容易分析、了解及監察議會。

熱心參與Code for Hong Kong的中大信息工程系導師Pili Hu，便於課堂帶領學生運用立法會投票結果作數據分析實習。課程教授不同的資料探勘（Data mining）技巧、利用Python程式語言及Pandas等程式庫，以數據繪製圖像及找出有意義的資訊。

其中一種應用了的技巧，為主成分分析 (Principal Component Analysis)，可以找出投票傾向相近的議員。

投票結果數據相對簡單，每名議員為出席並投票、缺席投票或缺席，出席議員投票分贊成、否決或棄權。首先簡化數據，電腦化表示贊成為1，反對為-1，其餘為0。而紀錄包含不同議員一年半愈1000次的投票結果，難以直接分析；

PCA便能在統計學上將每人的投票傾向統整為一個數字。圖象化如下便會得出一個較易理解的「政治光譜」，每點代表議員，點越接近便代表投票傾向越接近。

![](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_VxmFIgX53qb_p.144570_1398513270115_undefined)

課程中以PCA得出的投票傾向光譜，另一嘗試是圖象化為3D圖象，詳細分析見[](http://bit.ly/1riabfV)http://bit.ly/1riabfV 

眾所周知，香港大部分議案都為泛民和建制派的對立。光譜中粗略可見不論民主黨或建制派以黨派整體來說都投票都相當一致（數字接近的直線），而若計算人力、社民連或自由黨在內，投票傾向就較建制派分散得多。這圖有助看中哪些議員較「獨立」，投票傾向和兩派都不相近。同樣的方法，也可以用予分析那些議案議員整體投票傾向會較相近。

課程中其他技巧包括推薦系統（Recommender System），以往日投票紀錄可以準確預計議員投票的取向；甚至用中央性（Centrality Analysis）、HITS等算法嘗試發掘出議員及議案的關係。

上述分析原為教學用途，要歸納出準確結論需要更細致的數據處理及專家研究。

而開放數據優點在於每人都可以參與分析，基於數據理性討論，互相進步。立法會今次起步是一好開始。促請政府今後開放更多適合電腦處理的數據。有興趣可到[課程網站](https://course.ie.cuhk.edu.hk/~engg4030/tutorial/)了解更多及嘗試參考例子分析；這次分析亦為開源項目設於[Github](http://nbviewer.ipython.org/urls/raw.githubusercontent.com/hupili/legcohk/master/LegCoHK.ipynb)。另外[Code for Hong Kong](https://www.facebook.com/groups/code4hk/) 和 [Open Data Hong Kong](http://odhk.github.io/)均會舉辦Hackathon等相關活動，使大家能實際應用立法會及其他開放數據，可密切留意！

＊主成分分析，見[維基百料](http://zh.wikipedia.org/zh-hk/%E4%B8%BB%E6%88%90%E5%88%86%E5%88%86%E6%9E%90)) 

＊[立法會xml 投票紀綠](http://www.legco.gov.hk/general/english/counmtg/yr12-16/mtg_1213.htm#cm20121010) 

＊課程分析結果詳請，以Creative Commons 4.0 發佈

[LegCoHK](http://nbviewer.ipython.org/urls/raw.githubusercontent.com/hupili/legcohk/master/LegCoHK.ipynb)  [1 PCA](http://bit.ly/1riabfV) [2 Recommender Analysis](http://nbviewer.ipython.org/urls/course.ie.cuhk.edu.hk/~engg4030/tutorial/tutorial9/Recommender-System.ipynb) [3 Graph Analysis](http://nbviewer.ipython.org/urls/course.ie.cuhk.edu.hk/~engg4030/tutorial/tutorial10/Graph-Analysis.ipynb)

＊＊鳴謝Pili Hu 提供資料

{% comment %}
Hackpad Url: https://code4hk.hackpad.com/VxmFIgX53qb
{% endcomment %}



