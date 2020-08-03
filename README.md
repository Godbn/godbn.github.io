# Godbn.github.io
这是一个博客,地址请前往:www.pwdsec.top

## git上传插件

必须需要下面插件

```
npm install --save hexo-deployer-git
```

## 百度和google 收录

```
npm install hexo-generator-sitemap --save
npm install hexo-generator-baidu-sitemap --save
```
配置:在 _config.yml 中添加：

```
Plugins:
- hexo-generator-baidu-sitemap
- hexo-generator-sitemap

baidusitemap:
    path: baidusitemap.xml
sitemap:
    path: sitemap.xml
```

## 文章标题转成拼音

```
npm i hexo-permalink-pinyin --save
```

配置:在 _config.yml 中配置

```
# https://github.com/viko16/hexo-permalink-pinyin
permalink_pinyin:
  enable: true
  separator: '-' # default: '-'
```

注: enable :是否启用插件 separator :词自己的间隔符

## Security 文章加密

```
npm install --save hexo-blog-encrypt
```

配置:在 _config.yml 中配置

``` code
encrypt: # hexo-blog-encrypt
  abstract: 有东西被加密了, 请输入密码查看.
  message: 您好, 这里需要密码.
  template: <div id="hexo-blog-encrypt" data-wpm="{{hbeWrongPassMessage}}" data-whm="{{hbeWrongHashMessage}}"><div class="hbe-input-container"><input type="password" id="hbePass" placeholder="{{hbeMessage}}" /><label>{{hbeMessage}}</label><div class="bottom-line"></div></div><script id="hbeData" type="hbeData" data-hmacdigest="{{hbeHmacDigest}}">{{hbeEncryptedData}}</script></div>
  wrong_pass_message: 抱歉, 这个密码看着不太对, 请再试试.
  wrong_hash_message: 抱歉, 这个文章不能被校验, 不过您还是能看看解密后的内容.  
```