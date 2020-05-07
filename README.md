
# 建立Telegram ChatBot in Django2.0
***
### 前言:
>本篇內容需要以下的材料:
>>  * python 3.6以上
>>  * 安裝 Git
>>  * 下載 Ngrok
>>  * 申請 Heroku 帳號 & 安裝 Heroku CLI
>>  * 申請 Telegram Bot
 ### 快速懶人包:
直接使用本篇的範例程式:

    $ git clone https://github.com/xxxxxxxxxxxxxx
    $ cd 
    $ pip install -r requirements.txt
填入TelegramBot的token:

    # mysite/myapp/views.py
    bot=telebot.TeleBot('請輸入你的token!!!')

執行Ngrok取得測試用網址:
圖片
設定Telegram Bot所需的webhook:
圖片
打開Telegram Bot對話視窗 & 測試:
圖片
