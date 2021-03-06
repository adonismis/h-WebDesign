# 形象首頁版型

## 0. BootStrap基本
   Html架構複製，並加font-awesome:https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css

## 1. Navbar 實作

注意事項：   
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

注意事項： 
* Components > carousel 找語法
* 用header包起來
* 於carousel-item 增加 header-carousel-item
* 改用背景圖 style="background-image: url(...)"
* 於carousel-item 再增加 bg-cover
* 於文字底增加底色 .carousel-caption{background-color:rgba(0,0,0,.6)}

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

## 3. 常見的三欄式排版

注意事項：
* 於container外層增加 session 將底色改掉、換白字色及內距向內推
      section.bg-info.py-5.text-white

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
注意事項：
* d-flex 

```
    <section class="py-5 bg-light">
        <div class="container">
            <h2 class="text-center my-3">如何這麼美味</h2>
            <div class="row">
                <div class="col-md-6">
                    <div class="d-flex">
                        <div class="mr-3"><i class="text-info fa fa-4x fa-assistive-listening-systems" aria-hidden="true"></i></div>
                        <div>
                            <h3>紅襪挖角 對59轟重砲手沒興趣</h3>
                            <p>波士頓紅襪希望能夠提升球隊的火力，看上響尾蛇隊的自由球員J.D. Martinez（馬丁尼茲），不過對於馬林魚重砲「怪力男」Giancarlo Stanton則是興致缺缺。</p>
                        </div>
                    </div>
                </div>
                <div class="col-md-6">
                    <div class="d-flex">
                        <div class="mr-3"><i class="text-info fa fa-4x fa-calculator" aria-hidden="true"></i></div>
                        <div>
                            <h3>紅襪挖角 對59轟重砲手沒興趣</h3>
                            <p>波士頓紅襪希望能夠提升球隊的火力，看上響尾蛇隊的自由球員J.D. Martinez（馬丁尼茲），不過對於馬林魚重砲「怪力男」Giancarlo Stanton則是興致缺缺。</p>
                        </div>
                    </div>
                </div>
                <div class="col-md-6">
                    <div class="d-flex">
                        <div class="mr-3"><i class="text-info fa fa-4x fa-birthday-cake" aria-hidden="true"></i></div>
                        <div>
                            <h3>紅襪挖角 對59轟重砲手沒興趣</h3>
                            <p>波士頓紅襪希望能夠提升球隊的火力，看上響尾蛇隊的自由球員J.D. Martinez（馬丁尼茲），不過對於馬林魚重砲「怪力男」Giancarlo Stanton則是興致缺缺。</p>
                        </div>
                    </div>
                </div>
                <div class="col-md-6">
                    <div class="d-flex">
                        <div class="mr-3"><i class="text-info fa fa-4x fa-binoculars" aria-hidden="true"></i></div>
                        <div>
                            <h3>紅襪挖角 對59轟重砲手沒興趣</h3>
                            <p>波士頓紅襪希望能夠提升球隊的火力，看上響尾蛇隊的自由球員J.D. Martinez（馬丁尼茲），不過對於馬林魚重砲「怪力男」Giancarlo Stanton則是興致缺缺。</p>
                        </div>
                    </div>
                </div>
            </div>

        </div>
    </section>
```

## 6. 網頁上置放 Google Map 及表單 &&　7. Bootstrap 簡易表單驗證

```
    <style>
         .form-control{
            border-width:2px;
        }
    </style>

    <section class="py-5 bg-light">
        <div class="container">
            <div class="row">
                <div class="col-md-6">
                    <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3623.1950240095175!2d121.74897431500078!3d24.75450158410405!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3467e4c364bd7dd3%3A0x2bd1e2ef01b06991!2z5paw5pyI5buj5aC0!5e0!3m2!1szh-TW!2stw!4v1510561993911" width="100%" height="450" frameborder="0" style="border:0" allowfullscreen></iframe>
                </div>
                <div class="col-md-6">
                    <form action="#"  id="needs-validation" novalidate>
                        <div class="form-group">
                            <label for="username">姓名*</label>
                            <input type="text" class="form-control" name="username" placeholder="請輸入姓名" required>
                            <div class="invalid-feedback">
                                請輸入姓名
                            </div>
                        </div>
                        <div class="form-group">
                            <label for="phone">電話*</label>
                            <input type="tel" class="form-control" name="phone" placeholder="請輸入電話" required>
                            <div class="invalid-feedback">
                                請輸入電話
                            </div>
                        </div>
                        <div class="form-group">
                            <label for="mail">E-mail*</label>
                            <input type="email" class="form-control" name="mail" placeholder="請輸入E-mail" required>
                            <div class="invalid-feedback">
                                請輸入E-mail
                            </div>
                        </div>
                        <div class="form-group">
                            <label for="number">人數</label>
                            <input type="number" class="form-control" name="number" placeholder="請輸入人數" required>
                            <div class="invalid-feedback">
                                請輸入人數
                            </div>
                        </div>                       
                        <div class="custom-controls-stacked">
                            <label class="custom-control custom-radio">
                                <input id="radioStacked3" name="radio-stacked" type="radio" class="custom-control-input" required>
                                <span class="custom-control-indicator"></span>
                                <span class="custom-control-description">需要素食</span>
                            </label>
                            <label class="custom-control custom-radio">
                                <input id="radioStacked4" name="radio-stacked" type="radio" class="custom-control-input" required>
                                <span class="custom-control-indicator"></span>
                                <span class="custom-control-description">不需要素食</span>
                            </label>
                        </div>
                        <div class="text-right">
                            <button type="button" class="btn btn-secondary">取消</button>
                            <button type="submit" class="btn btn-primary">送出</button>
                        </div>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <script>
    // Example starter JavaScript for disabling form submissions if there are invalid fields
    (function() {
    'use strict';

    window.addEventListener('load', function() {
        var form = document.getElementById('needs-validation');
        form.addEventListener('submit', function(event) {
        if (form.checkValidity() === false) {
            event.preventDefault();
            event.stopPropagation();
        }
        form.classList.add('was-validated');
        }, false);
    }, false);
    })();
    </script>
```

## 8. 格線系統及背景效果

```
    <section class="container-fluid">
        <div class="row">
            <div class="col-md-6 p-4 bg-cover text-white" style="background-image:url(https://images.unsplash.com/photo-1481185103603-1dc844ef51db?dpr=2&auto=format&fit=crop&w=1080&h=718&q=80&cs=tinysrgb&crop=)">
                <div class="row">
                    <div class="col-md-9">
                        <small>加入我們</small>
                        <h3>亞冠賽／日本隊王牌今永昇太：王柏融肯定可以站穩日職</h3>
                        <p>亞冠賽日本隊投手今永昇太，18日對中華隊6局狂飆12Ｋ，有「新台灣殺手」美名，他自己則是十分謙虛，認為這次比賽還有很多需要學習的地方，「亞冠賽每隊程度都很好，我們成長，相對的對手也成長，希望日本年輕球員能打出不服輸的棒球。」</p>
                        <a href="#" class="btn btn-outline-warning">點選</a>
                    </div>
                </div>
            </div>
            <div class="col-md-6 p-4 bg-cover text-white" style="background-image:url(https://images.unsplash.com/photo-1498309313100-e308c8946b45?dpr=2&auto=format&fit=crop&w=1500&h=2250&q=80&cs=tinysrgb&crop=)">
                <div class="row">
                    <div class="col-md-9">
                        <small>加入我們</small>
                        <h3>亞冠賽／日本隊王牌今永昇太：王柏融肯定可以站穩日職</h3>
                        <p>亞冠賽日本隊投手今永昇太，18日對中華隊6局狂飆12Ｋ，有「新台灣殺手」美名，他自己則是十分謙虛，認為這次比賽還有很多需要學習的地方，「亞冠賽每隊程度都很好，我們成長，相對的對手也成長，希望日本年輕球員能打出不服輸的棒球。」</p>
                        <a href="#" class="btn btn-outline-warning">點選</a>
                    </div>
                </div>
            </div>
        </div>
    </section>
```

## 9. 網頁中不同 Modal 互相切換的手法


```
    <div class="modal fade" id="loginModal" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
        <div class="modal-dialog" role="document">
            <div class="modal-content">
                <form action="#"  id="login-validation" novalidate>
                    <div class="modal-header bg-primary text-white">
                        <h5 class="modal-title" id="exampleModalLabel">登入</h5>
                        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                        <span aria-hidden="true">&times;</span>
                        </button>
                    </div>
                    <div class="modal-body">                
                        <div class="form-group">
                            <label for="exampleInputEmail1">電子郵件</label>
                            <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="請輸入電子郵件" required>
                            <small id="emailHelp" class="form-text text-muted">請輸入電子郵件</small>
                        </div>
                        <div class="form-group">
                            <label for="exampleInputPassword1">密碼</label>
                            <input type="password" class="form-control" id="exampleInputPassword1" placeholder="請輸入密碼" required>
                        </div>
                        <div class="form-check">
                            <label class="form-check-label">
                            <input type="checkbox" class="form-check-input">
                            記住我
                            </label>
                        </div>
                    </div>
                    <div class="modal-footer">
                        <a href="#" class="mr-auto" data-dismiss="modal" data-toggle="modal" data-target="#registerModal">切換到註冊</a>
                        <button type="button" class="btn btn-secondary" data-dismiss="modal">取消</button>
                        <button type="submit" class="btn btn-primary">送出</button>
                    </div>
                </form>
            </div>
        </div>
    </div>

    <div class="modal fade" id="registerModal" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
        <div class="modal-dialog" role="document">
            <div class="modal-content">
                <form action="#"  id="register-validation" novalidate>               
                    <div class="modal-header bg-warning text-white">
                        <h5 class="modal-title" id="exampleModalLabel">註冊</h5>
                        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                        <span aria-hidden="true">&times;</span>
                        </button>
                    </div>
                    <div class="modal-body">
                        <div class="row">
                            <div class="col-md-6">
                                <h5>註冊六角西餐廳</h5>
                                <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Repudiandae consectetur eligendi nam, omnis suscipit culpa at consequatur est quam deserunt reprehenderit dolore magnam alias itaque odit quasi voluptas hic. Autem!</p>
                            </div>
                            <div class="col-md-6">
                                <div class="form-group">
                                    <label for="exampleInputEmail1">電子郵件</label>
                                    <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="請輸入電子郵件" required>
                                    <small id="emailHelp" class="form-text text-muted">請輸入電子郵件</small>
                                </div>
                                <div class="form-group">
                                    <label for="exampleInputPassword1">密碼</label>
                                    <input type="password" class="form-control" id="exampleInputPassword1" placeholder="請輸入密碼" required>
                                </div>
                                
                                <div class="form-group">
                                    <label for="exampleInputPassword1">確認密碼</label>
                                    <input type="password1" class="form-control" id="exampleInputPassword2" placeholder="請輸入確認密碼" required>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="modal-footer">
                        <a href="#" class="mr-auto" data-dismiss="modal" data-toggle="modal" data-target="#loginModal">切換到登入</a>
                        <button type="button" class="btn btn-secondary" data-dismiss="modal">取消</button>
                        <button type="submit" class="btn btn-warning">送出</button>
                    </div>
                </form>
            </div>
        </div>
    </div>
```

```
<script>
    (function() {
    'use strict';

    window.addEventListener('load', function() {

        var loginform = document.getElementById('login-validation');
        loginform.addEventListener('submit', function(event) {
        if (loginform.checkValidity() === false) {
            event.preventDefault();
            event.stopPropagation();
        }
        loginform.classList.add('was-validated');
        }, false);

        var registerform = document.getElementById('register-validation');
        registerform.addEventListener('submit', function(event) {
        if (registerform.checkValidity() === false) {
            event.preventDefault();
            event.stopPropagation();
        }
        registerform.classList.add('was-validated');
        }, false);

    }, false);
    })();
</script>
```

## 10. 頁尾
```
    <footer class="bg-light py-5 mt-5">
        <div class="container d-flex justify-content-between">
                <div>© Copyright 2017 六角西餐廳</div>
                <div><i class="fa fa-facebook-official" aria-hidden="true"></i></div>
        </div>
    </footer>
```
