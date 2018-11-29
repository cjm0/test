
# parcel 文档

[Parcel](https://parceljs.docschina.org/getting_started.html) 是 Web 应用打包工具，适用于经验不同的开发者。它利用多核处理提供了极快的速度，并且不需要任何配置。

## 快速开始

```bash
yarn add parcel-bundler -D 

yarn init -y
```

## 开发环境

`parcel src/index.html --no-cache` 启动 

## 生产环境

`rm -rf dist && parcel NODE_ENV=production build src/index.html -p 2345 --no-cache --public-url ./` 打包

## 转换

1. `babel yarn add babel-preset-env -D` 加 babel

2. `yarn add postcss-modules autoprefixer -D` 加 postcss

2. `parcel index.html -p 8888` 重新设置端口号

3. `parcel watch index.html` 监听文件变化，但是不会启动 web 服务，需要自己建一套服务器

4. `rm -rf dist` 删除 dist 包 

5. `--public-url ./` 设置资源引用路径

6. `--out-dir build/output || --out-dir build/output` 输出路径，默认 dist

7. `--no-cache` 禁用缓存系统



