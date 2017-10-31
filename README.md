# 形象首頁版型

0. BootStrap基本Html架構複製，並加font-awesome:https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css

1. Navbar 實作
    * 複製 Navbar 語法 [Navbar](https://getbootstrap.com/docs/4.0/components/navbar/)
    * 改 Navbar 顏色：改class navbar-dark bg-dark
    * 將 a.navbar-brand標題換為img並設定高度寬度
    * 改選單文字並於form-inline增加登入、註冊( .btn.btn-outline-primary.mr-1 登入 、.btn.btn-primary 註冊)
    * btn 寬度增加 .btn{ border-width: 2px;}
    * Navbar 上方增加灰底並加入兩個白色社群按鈕 .bg-secondary.py-1>.container >( <a href="#" class="text-white"><i class="fa ..></i></a> <a href="#" class="text-white"><i class="fa ..></i></a> )

2. 製作滿版的背景圖及文字輪播
    * Components > carousel 找語法
    * 用header包起來
    * 於carousel-item 增加 header-carousel-item
    * .header-carousel-item{height:450px;}
    * 改用背景圖 style="background-image: url(...)"
    * 於carousel-item 再增加 bg-cover
    * bg-cover{background-size: cover;background-position:center center;}
    * 增加文字描述(但字顏色容易不明顯)  
    * < div class="corousel-caption d-none d-md-block px-3"><h3>...></h3></div >
    * 於文字底增加底色 .carousel-caption{background-color:rgba(0,0,0,.6)}

3. 常見的三欄式排版

4. 使用格線做混合式排版

5. 充滿自由的 Flex 排版

6. 網頁上置放 Google Map 及表單

7. Bootstrap 簡易表單驗證

8. 格線系統及背景效果

9. 網頁中不同 Modal 互相切換的手法

