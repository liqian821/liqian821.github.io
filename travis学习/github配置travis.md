# 开启 Travis 服务
https://github.com/marketplace/travis-ci



### 安装gitbook失败

```bash
info: installing plugin "todo" 
info: install plugin "todo" (*) from NPM with version 0.1.3 
/home/travis/.gitbook/versions/3.2.3/node_modules/npm/node_modules/aproba/index.js:25
    if (args[ii] == null) throw missingRequiredArg(ii)
                          ^
Error: Missing required argument #1
    at andLogAndFinish (/home/travis/.gitbook/versions/3.2.3/node_modules/npm/lib/fetch-package-metadata.js:31:3)
    at fetchPackageMetadata (/home/travis/.gitbook/versions/3.2.3/node_modules/npm/lib/fetch-package-metadata.js:51:22)
    at resolveWithNewModule (/home/travis/.gitbook/versions/3.2.3/node_modules/npm/lib/install/deps.js:490:12)
    at /home/travis/.gitbook/versions/3.2.3/node_modules/npm/lib/install/deps.js:491:7
    at /home/travis/.gitbook/versions/3.2.3/node_modules/npm/node_modules/iferr/index.js:13:50
    at /home/travis/.gitbook/versions/3.2.3/node_modules/npm/lib/fetch-package-metadata.js:37:12
    at addRequestedAndFinish (/home/travis/.gitbook/versions/3.2.3/node_modules/npm/lib/fetch-package-metadata.js:67:5)
    at returnAndAddMetadata (/home/travis/.gitbook/versions/3.2.3/node_modules/npm/lib/fetch-package-metadata.js:121:7)
    at pickVersionFromRegistryDocument (/home/travis/.gitbook/versions/3.2.3/node_modules/npm/lib/fetch-package-metadata.js:138:20)
    at /home/travis/.gitbook/versions/3.2.3/node_modules/npm/node_modules/iferr/index.js:13:50
The command "gitbook install" failed and exited with 1 during .
```

解决方法：

book.json文件中将todo插件删除。