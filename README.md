# HW1

Jupyter url:https://nbviewer.jupyter.org/github/baker12355/HW1/blob/master/HW1.ipynb#

Run:

    python trader.py --training training_data.csv

完成後會建立一個決定動作的csv檔。

-----


> ## 策略動機
> 
> 1. 最大獲利為考量
> 2. 交易動作沒有手續費
> 

-----

> ## 均線的邏輯
>
> 均線是一條相對大盤平滑的線，大盤上漲到一定價格時會漲破均線；
> 下跌到一定價格時會跌破均線；
> 我在這定義新的大盤為三日均線。由於在短時間多次交易會造成獲利的損失，這是因為當日收盤價往往會低於隔日開盤價。
> 

>故大盤趨勢可表示為:

        if new_close>=average: #大盤大於均線
            rising
        else:
            falling
           
>依著此邏輯進行買賣便是我的策略

>> ## 要討論的參數
>
>  1.均線的尺度
>>  均線常見的有5日均線、20日均線也稱月線、60日均線也稱季線，
>>  時間越長，相對的越平滑，這也代表著短、中、長期投資客的考量。
>>  考量訓練資料大小的情況下，我選擇20日均線。
>
>  2.均線可向上下個取一定%數為震盪緩衝
>>  此一機制主要是預防兩線在短時間內多次交叉，造成鉅額交易手續費的問題，此次問題中，不需考慮手續費。





