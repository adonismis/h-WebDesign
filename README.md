# 形象首頁版型

## 0. BootStrap基本
   Html架構複製，並加font-awesome:https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css

## 1. Navbar 實作

    * 複製 Navbar 語法 [Navbar](https://getbootstrap.com/docs/4.0/components/navbar/)
    * 改 Navbar 顏色：改class navbar-dark bg-dark
    * 將 a.navbar-brand標題換為img並設定高度寬度
    * 改選單文字並於form-inline增加登入、註冊( .btn.btn-outline-primary.mr-1 登入    .btn.btn-primary 註冊)
    * btn 寬度增加 .btn{ border-width: 2px;}
    * Navbar 上方增加灰底並加入兩個白色社群按鈕 
    
    ```
    .bg-secondary.py-1
        .container 
            ( <a href="#" class="text-white"><i class="fa ..></i></a> <a href="#" class="text-white"><i class="fa ..></i></a> )
    ```

## 2. 製作滿版的背景圖及文字輪播

    * Components > carousel 找語法
    * 用header包起來
    * 於carousel-item 增加 header-carousel-item
    * 改用背景圖 style="background-image: url(...)"
    * 於carousel-item 再增加 bg-cover
    ```
    <style>
        .header-carousel-item{height:450px;}
        .bg-cover{background-size: cover;background-position:center center;}
    </style>
    ```
    * 增加文字描述，但字顏色容易不明顯，故增
    ```
    <div class="corousel-caption d-none d-md-block px-3">
        <h3>...  </h3 >
    </div>
    ```
    
    * 於文字底增加底色 .carousel-caption{background-color:rgba(0,0,0,.6)}

## 3. 常見的三欄式排版
```
     .container>.row>
        .col-md-4
            .mb-2 <i class="fa...></i>
            <h3>....</h3>
            <p>...</p>
        .col-md-4
            .mb-2 <i class="fa...></i>
            <h3>....</h3>
            <p>...</p>
        .col-md-4
            .mb-2 < i class="fa...>< /i>
            <h3>....</h3>
            <p>...</p>
```
    * 於container外層增加 session 將底色改掉、換白字色及內距向內推
      section.bg-info.py-5.text-white

## 4. 使用格線做混合式排版

注意事項：
 * section 增加 style="position:relative"
 * row > col-md-5 增 style="position:absolute;top:0;bottom:0;background-image:url(..)"
 * 增container>row>col-md-7 
 * row 增 justify-content-end 並增 text-md-dark

```
    <style>
        @media (min-width: 768px) { 
            .text-md-dark{
                color:#333;
            }
        }
    </style>
    <section class="container-fluid py-5 bg-light text-white" style="position:relative">
        <div class="row">
            <div class="col-md-5 bg-cover" style="position:absolute;top:0;bottom:0;background-image:url(https://images.unsplash.com/photo-1481185103603-1dc844ef51db?dpr=2&auto=format&fit=crop&w=1080&h=718&q=80&cs=tinysrgb&crop=);"></div>
            <div class="container">
                <div class="row justify-content-end text-md-dark">
                    <div class="col-md-7">
                        <h3>歡迎來到六角學院</h3>
                        <p>沒有遺憾的愛過、支持過他們，在商言商，他們總是假設：喔，但相信我。可是已經晚了……請你以後不要</p>
                        <a href="#" class="btn btn-outline-info">查看更多..</a>
                        <div class="row mt-3">
                            <div class="col-md-6">
                                <h3>歡迎來到六角學院</h3>
                                <p>沒有遺憾的愛過、支持過他們，在商言商，他們總是假設：喔，但相信我。可是已經晚了……請你以後不要</p>
                            </div>
                            <div class="col-md-6">
                                <h3>歡迎來到六角學院</h3>
                                <p>沒有遺憾的愛過、支持過他們，在商言商，他們總是假設：喔，但相信我。可是已經晚了……請你以後不要</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
```


## 5. 充滿自由的 Flex 排版

## 6. 網頁上置放 Google Map 及表單

## 7. Bootstrap 簡易表單驗證

## 8. 格線系統及背景效果

## 9. 網頁中不同 Modal 互相切換的手法

