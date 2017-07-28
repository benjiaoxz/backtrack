# backtrack
手机返回键控制

code: [https://coding.net/u/benjiaoxz/p/backtrack/git](https://coding.net/u/benjiaoxz/p/backtrack/git)

pages: [http://benjiaoxz.coding.me/backtrack/examples/index.html](http://benjiaoxz.coding.me/backtrack/examples/index.html)

## 使用

	npm install
	npm start
	
## 案例

    backtrack(function (data) {
        var self = this;

        //弹窗层，返回0
        $('.dialog').on('click.back', function () {
            self.setState(0);
        });

        //关闭弹窗层，返回-1
        $('.close').on('click.back', function () {
            self.setState(-1);
        });
    }, function (state, page) {
        this.go();
    });

## 参数
**config**：<br>
初始配置，用于设置页面其他弹窗的级别，必须为函数

**callback**：<br>
回调，可以使用当前作用域，必须为函数，返回参数为已存储的历史记录页面

## 方法
**setState**：<br>
设置其他页面的级别，参数必须为数字，默认当前页，0：表示当前页，-1：表示上一页

**go**：<br>
跳转，0：表示当前页，-1：表示上一页

**open**：<br>
开启控制

## License

[MIT](http://opensource.org/licenses/MIT)