---
title: '[C#] configuration'
date: 2024-08-21T14:00:00+08:00
draft: false
---

### Setup.ini

在C# 應用設定檔常見的配置，過去有人使用Setup.ini檔案直接讀取  
優點是易讀，缺點是Setup.ini沒辦法做加密  
個人認為兩者都可以，有需要隱藏私人資訊需求的應用，請都使用常見的.config做配置

### web.config 以及 app.config 
* * *

app.config（Windows Forms 和 Console 應用）  
web.config（ASP.NET 應用）

### ＜appSetting＞
* * *

For 靜態數值，在整個程式生命週期都不會更動的情況使用

*   簡單的鍵值對：當你需要存儲少量的鍵值對設定，例如郵件伺服器地址、文件路徑等。
*   靜態配置：設定內容在應用程序執行期間不會改變。
*   簡單易讀：方便直接透過 ConfigurationManager.AppSettings 讀取。

### ＜Package.Properties.Settings＞
* * *

可設置為依用戶不同使參數更改

*   需要更多結構化：例如複雜的設定，或者需要存儲大量的參數
*   用戶特定的設置：如果設置可能因用戶不同而不同。
*   需要自動管理：Settings 設計器可以幫助你自動生成配置代碼，並提供更好的類型安全性（例如，設定可以是 int、string 等）。