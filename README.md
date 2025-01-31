# jsdelivr-auto-fallback

> 修复 cdn.jsdelivr.net 无法访问的问题

由于一些原因，`cdn.jsdelivr.net` 在一些地区无法访问。在网站里添加上 `jsdelivr-auto-fallback` 代码，可以自动检测 `cdn.jsdelivr.net` 是否可用，
如果不可用时，会自动把所有 **js, css, image** 的地址切换到其他可用的域名。

比如

- `gcore.jsdelivr.net`
- `fastly.jsdelivr.net`

## 添加方法

1. 直接复制 [index.js](index.js) 或 [index.min.js](index.min.js) 里的内容，加到网站里。强烈建议添加到 head 标签最上面。
1. 所有 `script` 标签加上 `defer` 属性。如果原来有 `async` 属性，可以跳过。这个可以避免 `pending` 状态带来的等待时间，大大提升性能。

## Release Note

### v0.0.2 (2022/5/20)

- 为了提升性能，检测方式由 `img` 标签改成 `link` 标签 (css)
- 建议 `script` 标签都加上 `defer` 属性，可以大大提升性能
- `timeout` 时间由 3 秒改成 2 秒

## 问题反馈

<https://github.com/PipecraftNet/jsdelivr-auto-fallback/issues>

## License

Copyright (c) 2022 [Pipecraft](https://www.pipecraft.net). Licensed under the [MIT license](LICENSE).

## >\_

[![Pipecraft](https://img.shields.io/badge/site-pipecraft-brightgreen)](https://www.pipecraft.net)
[![PZWD](https://img.shields.io/badge/site-pzwd-brightgreen)](https://pzwd.net)
[![BestXTools](https://img.shields.io/badge/site-bestxtools-brightgreen)](https://www.bestxtools.com)
