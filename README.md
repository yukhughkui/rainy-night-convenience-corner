# 雨夜便利店街角 · 微缩 3D 场景

同一命题下的**模型测试对照**：两个模型分别生成的单文件、可离线运行的雨夜日式便利店街角微缩三维模型。采用三渲二（toon-shaded）卡通渲染，浓厚的二次元动画夜晚氛围，可通过鼠标自由拖拽、旋转、缩放观察整个场景。

## 在线预览

| 版本 | 生成来源 | 在线预览 | 源文件 |
| --- | --- | --- | --- |
| 版本 A（首页） | 混元 3 | 👉 **https://yukhughkui.github.io/rainy-night-convenience-corner/** | [`index.html`](./index.html) |
| 版本 B | Hy4 | 👉 **https://yukhughkui.github.io/rainy-night-convenience-corner/hy4.html** | [`hy4.html`](./hy4.html) |

（GitHub Pages 托管，浏览器直接打开即可。可拖拽旋转、滚轮缩放、右键平移。两个版本均为单文件、零外部依赖，可离线运行。）

## 仓库地址

https://github.com/yukhughkui/rainy-night-convenience-corner

## 场景内容

- **便利店主体**：位于底座视觉中心，大面积玻璃橱窗可清晰看到店内。
- **店内陈设**（明亮温暖，与室外潮湿昏暗的雨夜形成对比）：整齐货架、饮料柜、便当区、饭团与零食陈列、收银台、咖啡机、杂志架、宣传海报、店内灯箱、冰柜、关东煮柜台、地面导视、储物柜与后场门。
- **街角元素**：便利店招牌、屋檐雨棚、自动门、门口地垫、自动贩卖机、自行车、雨伞架、垃圾桶、路灯、电线杆与电线、路牌、街角护栏、停车位、排水沟、积水路面、反光斑马线、小巷入口、空调外机、公告栏。
- **基础动效**：持续降雨、屋檐滴水、地面积水波纹、招牌/灯箱轻微闪烁、自动门偶尔开合、雨水沿玻璃滑落、街面积水反射灯光、远处交通信号灯微弱变化。

## 技术说明

- 纯前端 **Three.js**（WebGL），全部内联打包进单个 HTML，**零外部依赖、可完全离线运行**。
- 三渲二风格：卡通材质 + 描边轮廓 + 柔和夜景霓虹分层。
- 两个 HTML 各自独立：`index.html` 作为 GitHub Pages 首页，`hy4.html` 通过同目录路径访问；`.nojekyll` 用于禁用 GitHub Pages 的 Jekyll 处理。

## 本地运行

方式一：直接用浏览器打开 `index.html` 或 `hy4.html`（双击即可，无需联网）。

方式二：本地起一个静态服务器后访问，例如：

```bash
python -m http.server 8899
# 浏览器打开 http://127.0.0.1:8899/
# 或        http://127.0.0.1:8899/hy4.html
```

## 二次开发

1. 修改对应的 `index.html` 或 `hy4.html` 中的场景代码；
2. 提交并推送：

```bash
git add index.html hy4.html README.md
git commit -m "update scene"
git push
```

GitHub Pages 会在约 1 分钟后自动重新部署，两个预览链接均不变。

---

*一个被定格下来的日本动画街角场景模型——安静、治愈，带一点都市夜晚的孤独感，却依然温暖。*
