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

业务分布版：沙盘覆盖东经 24–72°、北纬 10–40°，标注振华石油 8 个已公开油气项目（伊拉克 4 / 阿联酋 2 / 埃及 1 / 巴基斯坦 1），含引线卡片与避让。实测 1440×900 下 60 FPS、0 控制台报错、8 张卡片全部可见且无重叠。项目坐标为公开资料近似落点，汇报前需向客户核对；第 5 个国家与第 9 个项目暂无公开信息。全球灰度高程不是精确 DEM，侧壁底边的台阶来自 1° 量级的边界数据。

## 数据来源

卫星影像来自 Esri World Imagery；国家边界来自 holtzy/D3-graph-gallery；灰度高程来自 turban/webgl-earth；早期地球纹理来自 Three.js examples。正式发布前请核查各资产许可和署名要求。没有为这些第三方素材声明统一开源许可。

## GitHub

本地使用 main 分支。配置仓库地址后推送：

```powershell
git remote add origin https://github.com/YOUR_ACCOUNT/middle-east-terrain-atlas.git
git push -u origin main
```

GitHub 身份验证由 Git Credential Manager 或个人已有的 SSH 配置处理，请勿把令牌写入代码或仓库。
