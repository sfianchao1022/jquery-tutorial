# jquery
- [jQuery 教程](https://www.w3school.com.cn/jquery/index.asp)

## toggle
```html
<!DOCTYPE html>
<html>

<head>
    <meta charset="utf-8">
    <script src="http://ajax.googleapis.com/ajax/libs
/jquery/1.4.0/jquery.min.js"></script>
    <script type="text/javascript">
        $(document).ready(function () {

            // slideToggle可以回復動作 
            // 結合slideUp & slideDown
            $(".flip").click(function flip_click() {
                // toggle(speed,callback) 結合 show() & hide()
                $(".panel").slideToggle("slow", function () { $(".click_again").toggle("slow") });
            });

        });
    </script>

    <style type="text/css">
        div.panel,
        p.flip,
        p.click_again {
            margin: 0px;
            padding: 5px;
            text-align: center;
            background: #e5eecc;
            border: solid 1px #c3c3c3;
        }

        div.panel {
            height: 120px;
            display: none;
        }

        p.click_again {
            display: none;
        }
    </style>
</head>

<body>

    <div class="panel">
        <p>W3School - 领先的 Web 技术教程站点</p>
        <p>在 W3School，你可以找到你所需要的所有网站建设教程。</p>
    </div>

    <div>
        <p class="flip">请点击这里</p>
        <p class="click_again">再按一次</p>
    </div>

</body>

</html>

```