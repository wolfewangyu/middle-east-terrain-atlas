# 中东三维地形沙盘

Three.js 区域沙盘原型，覆盖埃及、红海、伊拉克与周边。支持拖拽旋转、滚轮缩放、区域高亮和地名标注。

## 本地运行

在项目根目录运行：

```powershell
python -m http.server 8877 --bind 127.0.0.1 --directory dist
```

浏览器打开 http://127.0.0.1:8877/?v=5 。请通过 HTTP 访问，不要直接双击 HTML。

## 文件

- dist/index.html：页面布局与样式
- dist/app.js：Three.js 场景、地形与交互
- dist/three.js：本地 Three.js 0.170.0
- docs/开发记录.md：当前进度、数据来源与下一步

## 当前状态

这是待完善的原型。JavaScript 语法检查已通过，最新版本尚未完成浏览器视觉验收。全球灰度高程不是精确 DEM；影像范围对齐、内部侧壁、覆盖面与地形贴合、标签避让和性能仍需完善。

## 数据来源

卫星影像来自 Esri World Imagery；国家边界来自 holtzy/D3-graph-gallery；灰度高程来自 turban/webgl-earth；早期地球纹理来自 Three.js examples。正式发布前请核查各资产许可和署名要求。没有为这些第三方素材声明统一开源许可。

## GitHub

本地使用 main 分支。配置仓库地址后推送：

```powershell
git remote add origin https://github.com/YOUR_ACCOUNT/middle-east-terrain-atlas.git
git push -u origin main
```

GitHub 身份验证由 Git Credential Manager 或个人已有的 SSH 配置处理，请勿把令牌写入代码或仓库。
