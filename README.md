# 雨夜便利店街角 · 微缩 3D 场景

同一命题下的**模型测试对照**：三个模型分别生成的单文件雨夜日式便利店街角微缩三维模型。采用三渲二（toon-shaded）卡通渲染，浓厚的二次元动画夜晚氛围，可通过鼠标自由拖拽、旋转、缩放观察整个场景。

## 在线预览

| 版本 | 生成来源 | 在线预览 | 源文件 |
| --- | --- | --- | --- |
| 版本 A（首页） | 混元 3 | 👉 **https://yukhughkui.github.io/rainy-night-convenience-corner/** | [`index.html`](./index.html) |
| 版本 B | Hy4 | 👉 **https://yukhughkui.github.io/rainy-night-convenience-corner/hy4.html** | [`hy4.html`](./hy4.html) |
| 版本 C | DeepSeek-V4-Pro | 👉 **https://yukhughkui.github.io/rainy-night-convenience-corner/deepseek-v4-pro.html** | [`deepseek-v4-pro.html`](./deepseek-v4-pro.html) |

（GitHub Pages 托管，浏览器直接打开即可。可拖拽旋转、滚轮缩放、右键平移。版本 A / B 为单文件、零外部依赖，可完全离线运行；版本 C 通过 CDN 引入 Three.js，需联网加载。）

## 生成信息（同一提示词）

| 版本 | 生成模型 | 积分 / Token | 耗时 |
| --- | --- | --- | --- |
| 版本 A | 混元 3 | 待补充 | 待补充 |
| 版本 B | Hy4 | 待补充 | 待补充 |
| 版本 C | DeepSeek-V4-Pro | 平台未直接暴露积分明细；按输出量估算约 2.5 万输出 token（最终 HTML 约 64 KB ≈ 1.6 万 token） | 约 30–50 分钟（单次会话，含场景编写、问题修复与浏览器渲染验证，估算） |

## 仓库地址

https://github.com/yukhughkui/rainy-night-convenience-corner

## 场景内容

- **便利店主体**：位于底座视觉中心，大面积玻璃橱窗可清晰看到店内。
- **店内陈设**（明亮温暖，与室外潮湿昏暗的雨夜形成对比）：整齐货架、饮料柜、便当区、饭团与零食陈列、收银台、咖啡机、杂志架、宣传海报、店内灯箱、冰柜、关东煮柜台、地面导视、储物柜与后场门。
- **街角元素**：便利店招牌、屋檐雨棚、自动门、门口地垫、自动贩卖机、自行车、雨伞架、垃圾桶、路灯、电线杆与电线、路牌、街角护栏、停车位、排水沟、积水路面、反光斑马线、小巷入口、空调外机、公告栏。
- **基础动效**：持续降雨、屋檐滴水、地面积水波纹、招牌/灯箱轻微闪烁、自动门偶尔开合、雨水沿玻璃滑落、街面积水反射灯光、远处交通信号灯微弱变化。

## 技术说明

- 纯前端 **Three.js**（WebGL），全部内联打包进单个 HTML。
- 版本 A / B 零外部依赖、可完全离线运行；版本 C 使用 ES Module import map 从 jsdelivr CDN 加载 Three.js 0.152.2，需联网。
- 三渲二风格：卡通材质 + 描边轮廓 + 柔和夜景霓虹分层。
- 三个 HTML 各自独立：`index.html` 作为 GitHub Pages 首页，`hy4.html`、`deepseek-v4-pro.html` 通过同目录路径访问；`.nojekyll` 用于禁用 GitHub Pages 的 Jekyll 处理。

## 本地运行

方式一：直接用浏览器打开 `index.html` 或 `hy4.html`（双击即可，无需联网）；`deepseek-v4-pro.html` 需联网加载 CDN 依赖。

方式二：本地起一个静态服务器后访问，例如：

```bash
python -m http.server 8899
# 浏览器打开 http://127.0.0.1:8899/
# 或        http://127.0.0.1:8899/hy4.html
# 或        http://127.0.0.1:8899/deepseek-v4-pro.html
```

## 二次开发

1. 修改对应的 `index.html`、`hy4.html` 或 `deepseek-v4-pro.html` 中的场景代码；
2. 提交并推送：

```bash
git add index.html hy4.html deepseek-v4-pro.html README.md
git commit -m "update scene"
git push
```

GitHub Pages 会在约 1 分钟后自动重新部署，三个预览链接均不变。

---

*一个被定格下来的日本动画街角场景模型——安静、治愈，带一点都市夜晚的孤独感，却依然温暖。*
