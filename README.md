# Laravel 11 確保程式碼保持乾淨和一致

引入 squizlabs 的 php_codesniffer 套件來擴增確保程式碼保持乾淨和一致，雖然程式碼風格跟設計沒有關係，但是程式碼風格不一致，對理解程式是一個很大的阻礙。

## 使用方式
- 把整個專案複製一份到你的電腦裡，這裡指的「內容」不是只有檔案，而是指所有整個專案的歷史紀錄、分支、標籤等內容都會複製一份下來。
```sh
$ git clone
```
- 將 __.env.example__ 檔案重新命名成 __.env__，如果應用程式金鑰沒有被設定的話，你的使用者 sessions 和其他加密的資料都是不安全的！
- 當你的專案中已經有 composer.lock，可以直接執行指令以讓 Composer 安裝 composer.lock 中指定的套件及版本。
```sh
$ composer install
```
- 產生 Laravel 要使用的一組 32 字元長度的隨機字串 APP_KEY 並存在 .env 內。
```sh
$ php artisan key:generate
```
- 執行 __phpcs__ 指令來檢查是否符合規範。
```sh
$ phpcs --standard=phpcs.xml {目錄（或用「.」代表目前工作目錄）|檔案}
```

----

## 畫面截圖
![](https://i.imgur.com/sGjNxeJ.png)
> 程式碼風格可以使程式碼易於閱讀
