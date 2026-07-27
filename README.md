# wechat-layout-zhijian

志坚劳动实践基地公众号 **版式 Skill**（WorkBuddy 可安装 skill）。

基于该号真实推文（`mp.weixin.qq.com/s/oc7HTtyIENpbpEx5LwMmNQ`）逆向提取，**参数为实测内联样式**，非推测。

## 包含
- 视觉基调表 + 配色 Token（实测色值）
- 文章 8 段骨架（封面 → 主题短句 → 英文点缀 → 导语框 → 编号章节 → 升华 → 署名）
- 可直接粘贴到公众号编辑器 / 秀米 / 135 的 HTML 模板
- 署名固定写法 + 发布前校验清单

## 适用
研学实践 / 汉文化 / 非遗 / 劳动教育类推文的排版复用。

## 安装（两种方式，二选一）

WorkBuddy 按 `SKILL.md` 里的 `name` 字段识别 skill，**不依赖文件夹名**——所以把整个仓库克隆进 skills 目录即自动生效，无需搬运文件。

### 方式 A：直接克隆进 skills 目录（推荐，一条命令装好）

用户级（所有项目可用）：
```bash
git clone https://github.com/qingfengyugui/wechat-layout-skill.git ~/.workbuddy/skills/wechat-layout-zhijian
```

项目级（仅当前工作区）：
```bash
git clone https://github.com/qingfengyugui/wechat-layout-skill.git "<你的工作区>/.workbuddy/skills/wechat-layout-zhijian"
```

克隆后重启 / 刷新 WorkBuddy 即可。触发词：公众号排版、版式、研学推文、志坚排版。

### 方式 B：只取 SKILL.md
下载本仓库 `SKILL.md`，放到 `~/.workbuddy/skills/<任意文件夹名>/SKILL.md` 即可。

## 注意
- 金色 `rgb(255,215,120)` 用途待确认，套用前请先在原号核对。
- 字体族未知（系统默认），勿手动指定。
- 详见 `SKILL.md` 第七节「校准缺口」。

> 内部规范，允许学习与非商用复用，商用需授权。
