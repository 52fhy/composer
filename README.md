# composer
composer


国内互联网某种神秘的力量让Composer变得越来越不稳定。 如果此种情况已经严重影响您的心情，请尝试在您的composer.json添加以下代码

``` js
composer config -e
{
    "repositories": [
        {   
            "packagist": false
        },  
        {   
            "type": "composer", 
            "url": "https://packagist.phpcomposer.com"
        }   
    ]
}
```
通过下面的命令，您可以观察速度提升的效果
```
$ composer update -vvv
```
但是Composer我也安装不了啊喂～

我们为composer installer也做了镜像，您可以尝试：

```
$ curl -sS http://packagist.cn/composer/installer | php
```
如果没有安装curl，尝试以下命令（PHP你总得装吧喂～）

```
$ php -r "readfile('http://packagist.cn/composer/installer');" | php
```

当然，如果您不需要检查运行环境，也可以直接下载（一般来说直接下载就可以用）:

https://github.com/52fhy/composer/raw/master/Composer-Setup.exe
https://github.com/52fhy/composer/raw/master/composer.phar

http://pan.baidu.com/s/1gfmSIbD 密码: f4vr
