## Problem

https://leetcode.com/problems/best-time-to-buy-and-sell-stock/

## Problem Description
You are given an array `prices` where `prices[i]` is the price of a given stock on the $i^{th}$ day.

You want to maximize your profit by choosing a **single day** to buy one stock and choosing a **different day in the future** to sell that stock.

Return *the maximum profit you can achieve from this transaction*. If you cannot achieve any profit, return `0`.

 

**Example 1**:

**Input**: prices = [7,1,5,3,6,4]  </br>
**Output**: 5  </br>
**Explanation**: Buy on day 2 (price = 1) and sell on day 5 (price = 6), profit = 6-1 = 5.  </br>
Note that buying on day 2 and selling on day 1 is not allowed because you must buy before you sell.




## Approach
我被這題難倒了。一開始採取的方式是計算每個點買入會有的最大利潤，但因為會計算太多次而超時。那究竟要怎麽樣才能減少計算呢？怎樣才快呢？
假設有兩個上漲段，A->B 和 C->D，如果 C 點的位置比 A 高，那其實 A 買入抱到 D點再賣出即可。然而，如果 C 點的位置比 A 低，C買入D賣出有可能比
A買入D賣出、或是A買入B賣出獲利的多。因此，真的需要關注的是買入點的變化，不需要計算每個點買入時的最大利潤。
1. 以起點為買入點，計算最大獲利。
2. 若出現更低的買入點，則重新計算最大獲利 (可以在賣出點比買入點高時，才計算獲利)。
3. 重覆2的動作，並比較及記錄最大獲利。



## Code

- Support Language: Java, Python

Python Code:

```py

```

Java Code:

```

```

**_Complexity Anlysis_**

- _Time Complexity_: 
- _Space Complexity_：
