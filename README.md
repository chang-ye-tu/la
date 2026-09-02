# 線性代數

## 教科書

教師編纂講義。

## 參考書

- Abadir, K., Magnus, J. R., 2005. *Matrix Algebra*. Cambridge University Press.
- [Harville, D., 1997. *Matrix Algebra From a Statistician's Perspective*. Springer.](https://link.springer.com/book/10.1007/b98818)
- [Harville, D., 2001. Matrix Algebra: Exercises and Solutions. Springer.](https://link.springer.com/book/10.1007/978-1-4613-0181-3)
- 教師講義
  - [Notes on the Classical Theory of Linear Models](https://github.com/chang-ye-tu/mva/blob/master/note/clm.pdf)
  - [Introduction to Matrix Calculus: Expanded "A Gentle Introduction to Matrix Calculus" by Jan R. Magnus](https://github.com/chang-ye-tu/mva/blob/master/note/mc.pdf)

<!--
- Magnus, J. R., Neudecker, H., 2019. Matrix Differential Calculus with Applications in Statistics and Econometrics. 3rd ed., John Wiley & Sons.
- Serre, D., 2010. *Matrices: Theory and Applications*. 2nd ed., Springer GTM 216.
-->

## 評分標準

- 期中考（40%） 11/04
- 期末考（40%） 12/23
- 平時成績 (20%)

## 授課時程

| 上課時間 |   課程進度                                                                                                             |
|----------|------------------------------------------------------------------------------------------------------------------------|
| 09/09    | <a href="https://github.com/chang-ye-tu/la/blob/master/note/unit01.pdf">**Unit 1** 向量、矩陣與資料矩陣</a><br>1.1 向量：內積、範數、Cauchy–Schwarz 不等式、正交性<br>1.2 矩陣：乘法的四種讀法、跡、特殊矩陣<br>1.3 資料矩陣：分塊乘法、中心化矩陣、Gram 矩陣與樣本共變異數 |
| 09/16    | <a href="https://github.com/chang-ye-tu/la/blob/master/note/unit02.pdf">**Unit 2** 向量空間、基底與維度</a><br>2.1 向量空間與子空間：生成、線性獨立<br>2.2 基底與維度：座標、基底變換、直和與維度公式<br>2.3 矩陣的子空間：行空間與零空間、秩—零度定理、模型空間與可識別性 |
| 09/23    | <a href="https://github.com/chang-ye-tu/la/blob/master/note/unit03.pdf">**Unit 3** 秩、反矩陣與行列式</a><br>3.1 秩：各種等價刻畫、Sylvester 不等式、rank(X′X) = rank(X)<br>3.2 反矩陣：唯一性、正交矩陣、非奇異性判準<br>3.3 行列式：排列定義、乘法定理、餘因子與伴隨矩陣、Cramer 法則 |
| 09/30    | <a href="https://github.com/chang-ye-tu/la/blob/master/note/unit04.pdf">**Unit 4** 分塊矩陣與 Schur 補</a><br>4.1 分塊因子：分塊三角矩陣及其代數、分塊 LDU 分解<br>4.2 Schur 補的推論：秩、非奇異性、分塊反矩陣與行列式<br>4.3 行列式與反矩陣更新：小矩陣行列式、Woodbury、Sherman–Morrison 與邊框矩陣 |
| 10/07    | <a href="https://github.com/chang-ye-tu/la/blob/master/note/unit05.pdf">**Unit 5** 線性方程組與消去法</a><br>5.1 基本運算與階梯形：基本矩陣、列等價、RREF、樞紐與秩標準形<br>5.2 線性方程組：相容性、完整解集合、列關係與增廣消去法<br>5.3 三角求解與分解：前代與回代、LDU、LU、列選軸與多個右端項 |
| 10/14    | <a href="https://github.com/chang-ye-tu/la/blob/master/note/unit06.pdf">**Unit 6** 正交性與投影</a><br>6.1 正交標準基底與 QR：Gram–Schmidt、正交座標、薄 QR 分解<br>6.2 正交補與投影：四個基本子空間、最佳近似、互補投影矩陣<br>6.3 最小平方法：所有最小化解與唯一擬合值、帽子矩陣、槓桿值與 Frisch–Waugh–Lovell 分解 |
| 10/21    | <a href="https://github.com/chang-ye-tu/la/blob/master/note/unit07.pdf">**Unit 7** 特徵值與特徵向量</a><br>7.1 特徵值問題：特徵多項式、代數與幾何重數、跡與行列式<br>7.2 相似與對角化：相似不變量、可對角化的判準、AB 與 BA 的特徵值<br>7.3 三角化：Schur 分解定理、Cayley–Hamilton 定理 |
| 10/28    | <a href="https://github.com/chang-ye-tu/la/blob/master/note/unit08.pdf">**Unit 8** 譜定理</a><br>8.1 對稱矩陣：實特徵值、正交特徵向量、譜定理與譜分解<br>8.2 變分刻畫：Rayleigh 商、Courant–Fischer 極小極大與擾動界<br>8.3 不變子空間與同時結構：可交換矩陣、壓縮與交錯、主成分分析初探 |
| 11/04    | **期中考**（Unit 1–8）                                                                                                 |
| 11/11    | <a href="https://github.com/chang-ye-tu/la/blob/master/note/unit09.pdf">**Unit 9** 正定與半正定矩陣</a><br>9.1 正定性：定義與等價判準、Sylvester 判準、Cholesky 分解<br>9.2 平方根與 Löwner 序：對稱平方根、偏序的性質、廣義特徵值問題<br>9.3 結構與統計應用：分塊矩陣的正定性、共變異數矩陣、白化與 Mahalanobis 距離 |
| 11/18    | <a href="https://github.com/chang-ye-tu/la/blob/master/note/unit10.pdf">**Unit 10** 冪等矩陣與二次型</a><br>10.1 一般冪等矩陣：值域—核空間分解、標準相似形、斜投影與正交投影<br>10.2 二次型：極化、合同與配方法、Sylvester 慣性定律<br>10.3 代數分解與二階動差：Cochran 秩判準、迴歸平方和、E(y′Ay) 與 MSE 的不偏性 |
| 11/25    | <a href="https://github.com/chang-ye-tu/la/blob/master/note/unit11.pdf">**Unit 11** 奇異值分解</a><br>11.1 奇異值分解：存在性、四個基本子空間、矩形矩陣的極分解<br>11.2 範數與逼近：譜範數、Frobenius 範數、Eckart–Young–Mirsky 定理、條件數與數值秩<br>11.3 Moore–Penrose 反矩陣：四個 Penrose 條件、最小範數最小平方解、中心化資料與脊迴歸 |
| 12/02    | <a href="https://github.com/chang-ye-tu/la/blob/master/note/unit12.pdf">**Unit 12** Kronecker 乘積、vec 與型樣矩陣</a><br>12.1 Kronecker 乘積：混合乘法律、特徵值、行列式與秩<br>12.2 vec 運算子：vec(AXB) = (B′⊗A)vec X、線性矩陣方程、多變量迴歸<br>12.3 型樣矩陣：交換矩陣 K、對稱化矩陣 N、vech 與複製矩陣 D |
| 12/09    | <a href="https://github.com/chang-ye-tu/la/blob/master/note/unit13.pdf">**Unit 13** 矩陣微分（一）</a><br>13.1 微分：偏導數排成矩陣為何不是導數、微分的定義與規則、第一辨識定理<br>13.2 Jacobian：矩陣函數的 Jacobian、標準微分公式、特徵值與特徵向量的微分<br>13.3 變數變換與駐點：Jacobian 行列式、駐點條件、最小平方與特徵值問題 |
| 12/16    | <a href="https://github.com/chang-ye-tu/la/blob/master/note/unit14.pdf">**Unit 14** 二階微分與線性模型</a><br>14.1 二階理論：二階微分與第二辨識定理、二階連鎖律、凸性與駐點分類<br>14.2 線性模型：最小平方法與 Gauss–Markov 定理、GLS 與 Aitken 定理、受限最小平方與一般線性假設<br>14.3 概似與敏感度：常態概似的分數與訊息矩陣、迴歸敏感度、刪除觀測值與影響量 |
| 12/23    | **期末考**（Unit 9–14）                                                                                                |

## 授課教師

changytu @ o365.fcu.edu.tw
