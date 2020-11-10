# 建立Telegram ChatBot in Django2.0
### 前言:
>本篇內容需要以下的材料:
>>  * python 3.6以上
>>  * 安裝 Git
>>  * 下載 Ngrok
>>  * 申請 Heroku 帳號 & 安裝 Heroku CLI
>>  * 申請 Telegram Bot

 ### 快速懶人包:
直接使用本篇的範例程式:

    $ git clone https://github.com/rs6000/01-TelegramBotQuickStart.git
    $ cd mysite
    $ pip install -r requirements.txt

填入TelegramBot的token:

    # mysite/myapp/views.py
    bot=telebot.TeleBot('請輸入你的token!!!')

執行Ngrok取得測試用網址:

![圖片1](https://smilehsu.cc/wp-content/uploads/2020/05/9d8168520a8a904fd7a09390d8e77f40.png)

設定Telegram Bot所需的webhook:

    格式:
    https://api.telegram.org/bot{TOKEN}/setwebhook?url={URL}

    本篇範例所使用的網址格式:
    https://api.telegram.org/bot{TOKEN}/setwebhook?url={URL}/api/telegram

    把token跟Ngrok給的網址複製貼上到上面的格式中，再把整串貼到瀏覽器上
    開啟。正確的話會得到回應如下:
    {"ok":true,"result":true,"description":"Webhook was set"}

    ps:如果之前已經設定過webhook，請先刪除舊的再換上新的。Ngrok每次
    的網址都是不同的。

    格式:
    https://api.telegram.org/bot{$token}/deleteWebhook

    輸入正確會得到下面的回應:
    {"ok":true,"result":true,"description":"Webhook was deleted"}

打開Telegram Bot對話視窗 & 測試:

![圖片2](https://smilehsu.cc/wp-content/uploads/2020/05/c7a7dc02ff6507856d29a2847f092200.png)

### 最後:
如果電腦內已經有安裝python &編輯器的話，把這篇提供範例檔
下載到電腦，建立環境到測試Telegram ChatBot，應該不超過10分鐘
網路上有很多Telegram ChatBot的範例(Python版)
但大多是單檔或用Flask。用Telegram + Django
相關的關鍵字在Google底下，找不到適合起步的範例
...最後在Youtube看到教學影片，才把內容寫成這篇。

剩下佈署到Heroku的內容留到下篇文章。

---
### Reference:
- [ heroku-deploy-django-telegrambot-webhook](https://www.youtube.com/watch?v=bWDKUl1OgJk) 作者來自烏茲別克
- [pyTelegramBotAPI](https://github.com/eternnoir/pyTelegramBotAPI) 本篇所使用的套件，範例程式就很好用了
- [Python Telegram Bot 機器人 教學文章](https://bit.ly/2WcSmH2) 使用Flask
