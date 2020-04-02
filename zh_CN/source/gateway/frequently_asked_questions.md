# Heltec<sup>TM</sup>网关系列常见问题

此页面包含了用户最常提出的问题。如果此页面的详细信息无法解决您的问题，您也可以在我们的论坛上留言： [community.heltec.cn](http://community.heltec.cn/)

&nbsp;

## `PicoGW_UI`软件无法选择"China"

### 原因

`PicoGW_UI`的默认安装包里面，并未包含中国使用的470~510MHz频段的配置文件。

### 解决办法

- 将此GitHub仓库克隆或者下载下来：[https://github.com/HelTecAutomation/lorasdk](https://github.com/HelTecAutomation/lorasdk)；
- 将其中的`global_conf_CN470.json`文件更名为**“default_global_conf_CN.json”**；
- 将`default_global_conf_CN.json`文件复制到`C:\Users\username\AppData\Roaming\Semtech\PicoGW_UI\Config`路径，若已存在同名文件，将其覆盖。

若一切正常，就在`PicoGW_UI`正常选择"China"了。