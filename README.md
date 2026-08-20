# texttextstext · 哲学的慰藉

两个独立模块，纯前端实现，可直接部署到 GitHub Pages / Netlify / Vercel。

## 项目结构

```
.
├── index.html      # 入口导航页
├── sirius.html     # 哲学对话 Agent（深色主题）
├── designer.html   # POD 排版设计器（浅色主题）
└── README.md
```

## 模块一：Sirius 哲学对话

**文件**: `sirius.html`

### 功能
- 与 AI 哲学 Agent Sirius 对话
- 六位哲学家人格：苏格拉底、伊壁鸠鲁、塞内加、蒙田、叔本华、尼采
- 自动情绪检测切换人格
- 金句提炼与复制
- 一键跳转到设计器排版

### 使用
1. 打开 `sirius.html`
2. 在左侧设置面板粘贴 DeepSeek API Key（仅保存在浏览器本地）
3. 开始对话
4. 说「给我一句话」触发金句生成
5. 点击「去设计器排版 →」跳转

### API 配置
```javascript
// 默认使用 DeepSeek API
const API_URL = 'https://api.deepseek.com/chat/completions';
```

如需更换其他兼容 OpenAI 格式的 API，修改 `sirius.html` 中的 `API_URL` 即可。

---

## 模块二：排版设计器

**文件**: `designer.html`

### 功能
- 6 种载体：方巾、短袖、陶瓷杯、袜子、海报、帆布袋
- 5 种字体风格：经典宋体、现代黑体、手写风、活版印刷、英文衬线
- 文字颜色 / 背景颜色自由调整
- 水平 / 垂直位置滑块调节
- 字号 20-100px 可调
- 导出 PNG 预览图

### 使用
1. 打开 `designer.html`
2. 输入文字内容（或从 Sirius 跳转自动填入）
3. 选择载体、字体、颜色
4. 调整位置和大小
5. 点击「下载 PNG」

---

## 本地使用

无需服务器，直接双击打开 HTML 文件即可使用。

```bash
# 或用本地静态服务器（可选）
npx serve .
# 或
python -m http.server 8080
```

## 部署到 GitHub Pages

1. 创建 GitHub 仓库
2. 上传这 3 个 HTML 文件
3. Settings → Pages → Source 选择 main branch
4. 访问 `https://你的用户名.github.io/仓库名/`

## 关于 Sirius

Sirius（天狼星）的性格原型来自《哈利波特》中的 Sirius Black：
- 忠诚于真实
- 叛逆于世俗规训
- 在黑暗中依然闪耀

## License

MIT
