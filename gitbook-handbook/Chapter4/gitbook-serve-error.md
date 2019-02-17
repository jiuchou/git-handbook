# 4.1.gitbook serve报错

1.报错信息

```bash
d:\book>gitbook serve
Live reload server started on port: 35729
Press CTRL+C to quit ...

info: 7 plugins are installed
info: loading plugin "livereload"... OK
info: loading plugin "highlight"... OK
info: loading plugin "search"... OK
info: loading plugin "lunr"... OK
info: loading plugin "sharing"... OK
info: loading plugin "fontsettings"... OK
info: loading plugin "theme-default"... OK
info: found 5 pages
info: found 4 asset files

Error: ENOENT: no such file or directory, stat 'd:\book\_book\gitbook\gitbook-plugin-fontsettings\fontsettings.js'
```

2.原因分析

https://github.com/GitbookIO/gitbook/issues/1309#issuecomment-273584516

3.解决方案

Edit: C:\Users\Administrator\.gitbook\versions\3.2.3\lib\output\website\copyPluginAssets.js

Steps:

1.  Edit file: `C:\Users\Administrator\.gitbook\versions\3.2.3\lib\output\website\copyPluginAssets.js`

2.  Modify in two places *copyAssets(output, plugin)* and *copyResources(output, plugin)*, the line:

   `confirm: true` 

   by

   `confirm: false`

