
# parcel 文档

[Parcel](https://parceljs.docschina.org/getting_started.html) 是 Web 应用打包工具，适用于经验不同的开发者。它利用多核处理提供了极快的速度，并且不需要任何配置。



## 快速开始

```bash
yarn add parcel-bundler -D 

yarn init -y
```



## 开发环境

`rm -rf dist && parcel src/index.html --no-source-maps` 



## 生产环境

`rm -rf dist && parcel NODE_ENV=production build src/index.html -p 2345 --public-url ./ --no-cache --no-source-maps`



## 转换

### 加 babel

```bash
yarn add babel-preset-env -D
```

接着，创建一个 `.babelrc` 文件:

```json
{
  "presets": ["env"]
}
```

### 加 postcss 

```bash
yarn add postcss-modules autoprefixer -
```

接着，创建一个 `.postcssrc` 文件:

```json
{
  "modules": false, // true 使用 cssModule 模式
  "plugins": {
    "autoprefixer": {
      "browsers": ["> 0.5%", "last 2 versions", "ie > 8"]
    }
  }
}
```



## 注意

1. `parcel index.html -p 8888` 重新设置端口号

2. `parcel watch index.html` 监听文件变化，但是不会启动 web 服务，需要自己建一套服务器

3. `rm -rf dist` 删除 dist 包 

4. `--public-url ./` 设置资源引用路径

5. `--out-dir build/output || --out-dir build/output` 输出路径，默认 dist

6. `--no-cache` 禁用缓存系统

7. `--no-source-maps` 去掉 sourceMap

8. Parcel 在模块中找到配置文件 (例如 .babelrc ，.postcssrc) 时会自动运行并进行转换
