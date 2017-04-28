|Catalog                    |Official Site                 |Source Version  |Specific Version Docs|
|:--------------------------|:-----------------------------|:---------------|:--------------------|
|App Framework              |[Angular.js][ng-1]            |[1.5.11][ng-2]   |[API Reference][ng-3]|
|Data Table                 |[md-data-table][mddt-1]       |[0.10.10][mddt-2]|[API Documentation][mddt-3]<br/>[Change Log][mddt-4]|
|File Uploader              |[ng-file-upload][ngfu-1]      |[12.2.13][ngfu-2]|[Full reference][ngfu-3]|
|Hotkeys                    |[angular-hotkeys][ah-1]       |1.7.0           |
|Icons                      |[material-design-icons][mdi-1]|[3.0.1][mdi-2]  |[Icons List][mdi-3]
|Material Design            |[Specification][md-1]<br>无需翻墙访问官网方式见下 |December 2016   |[Offline docs (March 2016)][md-2]<br>[Docker image (March 2016)][md-3]|
|Material Design for Angular|[Angular Material][am-1]      |[1.1.3][am-2]   |[Documentation][am-3]|
|Router                     |[ui-router][uir-1]            |[0.4.2][uir-2] |[Documentation][uir-3]|
|sortable                   |[ng-sortable][ns-1]           |[1.3.7][ns-2]   |[Documentation][ns-3]|

### 无需翻墙访问 Material Design 官网

使用浏览器插件 [gooreplacer4chrome](https://github.com/jiacai2050/gooreplacer4chrome)，添加如下重定向规则：

* `https://www.gstatic.com/feedback/api.js` => `https://alphahinex.github.io/proxy/gstatic/feedback/api.js`
* `https://www.gstatic.com/external_hosted/picturefill/picturefill.min.js` => `https://alphahinex.github.io/proxy/gstatic/external_hosted/picturefill/picturefill.min.js`

### 升级文档下载路径 ###
- [Angular.js API](https://code.angularjs.org/1.6.1/angular-1.6.1.zip)，修改url内的版本号，将压缩包内docs路径得文件放入对应路径下
- [md-data-table API](https://github.com/daniel-nagy/md-data-table/tree/v0.10.10)，修改url内的版本号，将README.md和CHANGELOG.md放入对应路径下
- [Angular Material API](https://github.com/angular/material/blob/master/docs/README.md)，下载对应版本的源码，build出API文档放入对应路径下
```
# 修改文档的index.html
# 添加
<script type="text/javascript">
  (function() {
    var baseUrl = '/projects/material/1.1.3/';
    if (location.hostname === 'propersoft-cn.github.io') {
      baseUrl = '/pea-refs' + baseUrl;
    }
    document.querySelector('base').href = baseUrl;
  })();
</script>
# 修改angular.js的路径
<script src="../../angular/1.5.11/angular.min.js"></script>
...
```
- [ui-router API](https://github.com/angular-ui/ui-router/wiki)，下载对应版本wiki文档放入对应路径下
- [ng-sortable API](https://github.com/a5hik/ng-sortable/tree/1.3.7)，修改url内的版本号，将README.md放入对应路径下


[ah-1]: http://chieffancypants.github.io/angular-hotkeys/
[am-1]: https://material.angularjs.org/latest/
[am-2]: https://github.com/angular/material/tree/v1.1.3
[am-3]: projects/material/1.1.3/index.html
[md-1]: https://material.io/guidelines/material-design/introduction.html
[md-2]: http://192.168.1.182:9101/www.google.com/design/spec/material-design/introduction.html
[md-3]: https://github.com/propersoft-cn/material-design-docs
[mddt-1]: https://github.com/daniel-nagy/md-data-table
[mddt-2]: https://github.com/daniel-nagy/md-data-table/tree/v0.10.10
[mddt-3]: projects/md-data-table/0.10.10/README.md
[mddt-4]: projects/md-data-table/0.10.10/CHANGELOG.html
[mdi-1]: http://google.github.io/material-design-icons/
[mdi-2]: https://github.com/google/material-design-icons/tree/3.0.1
[mdi-3]: https://material.io/icons/
[ng-1]: https://angularjs.org/
[ng-2]: https://github.com/angular/angular.js/tree/v1.5.11
[ng-3]: projects/angular/1.5.11/docs/index.html
[ngfu-1]: https://angular-file-upload.appspot.com/
[ngfu-2]: https://github.com/danialfarid/ng-file-upload/tree/12.2.13
[ngfu-3]: projects/ng-file-upload/README.md
[uir-1]: https://angular-ui.github.io/ui-router/site/
[uir-2]: https://github.com/angular-ui/ui-router/tree/0.4.2
[uir-3]: projects/ui-router/0.4.2/Home.md
[ns-1]: http://a5hik.github.io/ng-sortable/#/kanban
[ns-2]: https://github.com/a5hik/ng-sortable/tree/1.3.7
[ns-3]: projects/ng-sortable/1.3.7/README.md
