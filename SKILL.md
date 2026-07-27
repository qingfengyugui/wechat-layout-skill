---
name: wechat-layout-zhijian
description: 志坚劳动实践基地公众号版式 Skill。当用户需要为该号（或同风格的研学/汉文化/非遗类推文）排版、套用版式模板、生成可粘贴的公众号 HTML、或询问"公众号排版规范/版式/格式"时使用。触发词：公众号排版、版式、研学推文、志坚排版、公众号格式规范、套模板、排版风格。基于单篇真实推文逆向提取，参数为实测内联样式。
agent_created: true
license: 内部规范，允许学习与非商用复用，商用需授权
metadata:
  adapted_from: 逆向自 https://mp.weixin.qq.com/s/oc7HTtyIENpbpEx5LwMmNQ
---

# 志坚劳动实践基地 · 公众号版式 Skill

当你需要为「志坚劳动实践基地」公众号（或同风格的研学 / 汉文化 / 非遗类推文）做排版时，遵循本规范。

> 数据来源：对样本文章 `js_content` 原始 HTML 的内联样式**实测**，参数均为观察值，非推测。唯一例外见文末「校准缺口」。

## 触发场景
用户说：排一篇研学推文 / 按志坚风格排版 / 套用版式模板 / 生成公众号 HTML / 公众号格式规范。

## 使用方法
1. 确认文章结构：封面 → 主题短句 → 英文点缀 → 导语框 → 编号章节 → 升华结尾 → 署名。
2. 复制「可粘贴 HTML 模板」，替换 `【】` 占位即可（公众号编辑器 / 秀米 / 135 直粘）。
3. 发布前过一遍「校验清单」。

---

## 一、公众号整体画像（调研结论）

- **定位**：丰县志坚中小学素质教育劳动实践基地官方号，面向中小学生及研学团体。
- **内容主题**：研学实践、汉文化溯源、非遗体验（剪纸 / 传拓）、劳动教育、红色思政、基地活动报道。
- **跨篇共性（多篇印证）**：
  - 署名块高度一致：`图文：X ／ 编辑：志坚宣 ／（审核：校长室）／（邮箱）`。
  - 结构稳定：封面大图 + 主题短句 + 英文点缀 + 导语框 + 编号站点章节 + 图文混排 + 升华结尾 + 署名。
  - 语言风格：公文式 + 抒情升华，结尾必有"知行合一…成长永不停步"式总结段。

---

## 二、视觉基调（实测）

| 维度 | 实测值 |
|---|---|
| 页面底色 | `rgb(251, 253, 240)` 暖米白 |
| 正文颜色 | `rgb(0, 0, 0)` 黑 |
| 次级文字 | `rgb(62, 62, 62)` 深灰 |
| 主题装饰标题色 | `rgb(174, 210, 222)` 浅蓝 |
| 章节胶囊底色 | `rgb(255, 243, 219)` 米色 |
| 导语/内容框底色 | `rgb(227, 246, 251)` / `rgb(231, 244, 255)` 浅蓝 |
| 金色点缀 | `rgb(255, 215, 120)`（用途待确认，见缺口） |
| 正文字号 | `15px` |
| 外层基准字号 | `16px` |
| 装饰标题字号 | `32px` |
| 英文点缀字号 | `14px`，`letter-spacing: 2px` |
| 行高 | `2`（正文） |
| 段落对齐 | 正文 `justify` 两端对齐 + `text-indent: 2em` 首行缩进 |
| 标题/署名对齐 | `center` 居中 |
| 图片 | 满宽 `width:100%`，无图注，章节间 `margin:10px 0` |
| 强调方式 | 仅 `<b>` 加粗：装饰标题、章节胶囊文字；无变色强调 |

### 配色 Token（建议固化为变量）
```css
--bg-page:   rgb(251, 253, 240);  /* 页面米白底 */
--blue-title:rgb(174, 210, 222);  /* 主题短句浅蓝 */
--cream-pill:rgb(255, 243, 219);  /* 章节胶囊米色 */
--box-blue:  rgb(227, 246, 251);  /* 导语/内容浅蓝框 */
--gold:      rgb(255, 215, 120);  /* 金色点缀（用途待定） */
--text:      rgb(0, 0, 0);        /* 正文黑 */
--text-2:    rgb(62, 62, 62);     /* 次级灰 */
```

---

## 三、文章骨架（照此顺序排）

1. **封面大图**：满宽横幅（建议比例 ≈ 0.30，即 1080×330 左右），无图注。
2. **主题装饰短句**：浅蓝 `32px` 居中加粗，如 `-夏日研学时光-`（破折号包裹的 4–8 字诗意短句）。
3. **英文点缀**：黑 `14px`、`letter-spacing:2px` 居中，如 `Summer Beauty Good time`。
4. **导语框**：浅蓝底 `padding:20px`，内文两端对齐、行高 2、首行缩进 2em。常以"读万卷书，行万里路…"式金句开题，概述活动时间 / 对象 / 意义。
5. **编号章节 ×N**：每章 = 左侧小装饰图标(≈59px) + 右侧米色胶囊(`0X. 站点名`) + 首段 `text-indent:2em` 引语 + 正文 + 满宽配图。
6. **升华结尾段**：无编号，总结式抒情（"知行合一促成长…"），呼应导语。
7. **署名块**：居中四行 `图文 / 编辑 / 审核 / 邮箱`。
8. **公众号名片**：平台自动追加，无需手排。

---

## 四、可粘贴 HTML 模板（公众号编辑器 / 秀米 / 135 直粘）

> 复制整段粘贴，替换 `【】` 占位即可。内联样式已按实测值写死。

```html
<!-- 1. 封面大图 -->
<section style="text-align:center;line-height:0;box-sizing:border-box;">
  <img src="【封面图URL】" style="width:100%;max-width:100%;vertical-align:middle;box-sizing:border-box;" />
</section>

<!-- 2. 主题装饰短句 -->
<section style="text-align:center;font-size:32px;color:rgb(174,210,222);box-sizing:border-box;">
  <b>-【夏日研学时光】-</b>
</section>

<!-- 3. 英文点缀 -->
<section style="text-align:center;font-size:14px;color:rgb(0,0,0);letter-spacing:2px;box-sizing:border-box;">
  <span>【Summer Beauty Good time】</span>
</section>

<!-- 4. 导语框 -->
<section style="background-color:rgb(227,246,251);padding:20px;box-sizing:border-box;">
  <section style="text-align:justify;color:rgb(0,0,0);line-height:2;box-sizing:border-box;">
    <p style="text-indent:2em;margin:0;padding:0;box-sizing:border-box;">【导语：读万卷书，行万里路……概述时间、对象、意义。】</p>
  </section>
</section>

<!-- 5. 章节（每章复制此块，改 0X 与名称） -->
<section style="display:flex;width:100%;box-sizing:border-box;">
  <section style="width:59px;vertical-align:top;box-sizing:border-box;">
    <img src="【章节小图标URL】" style="width:100%;vertical-align:middle;box-sizing:border-box;" />
  </section>
  <section style="background-color:rgb(255,243,219);padding:2px 19px;box-sizing:border-box;">
    <b style="color:rgb(0,0,0);font-size:15px;">01. 【汉皇祖陵】</b>
  </section>
</section>
<section style="text-align:justify;color:rgb(0,0,0);line-height:2;box-sizing:border-box;">
  <p style="text-indent:2em;margin:0;padding:0;box-sizing:border-box;">【首段引语（如：第一站，学子们走进……），不另加粗。】</p>
  <p style="text-indent:2em;margin:0;padding:0;box-sizing:border-box;">【正文段落……】</p>
</section>
<section style="margin:10px 0;line-height:0;box-sizing:border-box;">
  <img src="【章节配图URL】" style="width:100%;max-width:100%;vertical-align:middle;box-sizing:border-box;" />
</section>

<!-- 6. 升华结尾段（无编号） -->
<section style="text-align:justify;color:rgb(0,0,0);line-height:2;box-sizing:border-box;">
  <p style="text-indent:2em;margin:0;padding:0;box-sizing:border-box;">【知行合一促成长，研学赋能启新程……总结升华。】</p>
</section>

<!-- 7. 署名块 -->
<section style="text-align:center;box-sizing:border-box;">
  <p style="margin:0;padding:0;">图文：【刘 毅】</p>
  <p style="margin:0;padding:0;">编辑：志坚宣</p>
  <p style="margin:0;padding:0;">审核：校长室</p>
  <p style="margin:0;padding:0;">邮箱：fxzjjd2025@126.com</p>
</section>
```

---

## 五、署名规范（固定写法）
- 格式：`图文：X ／ 编辑：志坚宣 ／ 审核：校长室 ／ 邮箱：fxzjjd2025@126.com`
- 居中、`15px`、黑色、各占一行。
- 图片与文案作者按实际填写；编辑固定「志坚宣」。

---

## 六、排版校验清单（发布前过一遍）
- [ ] 页面底色为暖米白（编辑器默认白底时需手动加外层米白 section）
- [ ] 主题短句浅蓝 32px 居中加粗、破折号包裹
- [ ] 英文点缀 14px、字间距 2px、居中
- [ ] 导语在浅蓝框内、首行缩进 2em、行高 2
- [ ] 每章：左侧小图标 + 米色胶囊(`0X. 名称`) + 首段缩进 2em
- [ ] 正文 15px、黑、两端对齐、行高 2、首行缩进 2em
- [ ] 图片满宽、无图注、章节间留 10px
- [ ] 结尾有升华段，不编号
- [ ] 署名块四行居中、编辑固定「志坚宣」
- [ ] 无彩色变色强调正文（仅 `<b>` 加粗标题与胶囊）

---

## 七、校准缺口（务必人工核对）
1. **金色 `rgb(255,215,120)` 的真实用途**未能从样本定位（可能在封面标题条或分隔元素），套用时先在原号找一处金色元素确认后再用。
2. **字体族未知**：公众号渲染不保留 `font-family`，全文使用系统默认（手机端多为系统无衬线）。不要手动指定字体。
3. **章节小图标**为外链装饰图，需自备素材（建议叶脉 / 汉纹类，与汉文化主题一致）。
4. 本规范基于单篇样本 + 多篇署名共性推导；若后续出现明显风格变体，以最新一篇为准重测。
