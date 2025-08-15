#  Project Requirements Document (PRD)**





**文档版本**：v2.0（2025-08-14）

**站点基础**：GitHub Pages 用户主页仓库 longfuxu/longfuxu.github.io（主域：https://longfuxu.github.io）

**口号（副标题）**：*Dream big, act little.*

**产品负责人/内容所有者**：Longfu Xu



------





## **0. 关键结论（TL;DR）**





- **信息架构**：Research / Publications / Talks & Teaching / Projects / SciXchange / Blog / Interests / CV / Contact。

- **技术路线**（二选一，推荐 A）：

  

  - **A. Hugo + Hugo Blox Academic**：在 main 存源码，GitHub Actions 构建后推送到 gh-pages；
  - **B. Next.js + MDX + Contentlayer**：Vercel 或 GitHub Actions + gh-pages。

  

- **博客**：支持 5 种内容模板、RSS、搜索、评论。

- **学术**：Publications 从 publications.bib 自动生成；结构化数据 JSON-LD；BibTeX/APA 一键复制。

- **验收**：Lighthouse 四维 ≥90、WCAG 2.2 AA、无 404/控制台报错、冷启动 TTFB/CLS 达标。





------





## **1. 背景与目标**





以 longfuxu.github.io 为基础，将个人主页升级为**以学术为主**的研究网站，同时纳入**博客（Blog）与兴趣（Interests）**，并设置 **SciXchange** 专页（强调为个人孵化平台）。目标受众为学术同行/合作方、学生与跨学科读者。





### **1.1 可量化目标（OKR）**





- **O1：研究画像清晰可导航**

  

  - KR1：代表论文 3–5 篇在首页 1 屏内可达（≤3 次点击）；
  - KR2：Publications 覆盖率 100%，每条含 DOI/预印本/代码/数据外链（如有）。

  

- **O2：建立高频低摩擦写作出口**

  

  - KR1：至少 5 种博客模版上线，支持 RSS/全文搜索/标签；
  - KR2：评论系统就绪（默认关闭，可按文开启）。

  

- **O3：SciXchange 清晰定位**

  

  - KR1：独立落地页，含愿景/机制/FAQ/加入方式；
  - KR2：与其他同名机构 SEO 区隔（副标题/结构化数据/元描述）。

  

- **O4：质量保证**

  

  - KR1：Lighthouse Performance/Accessibility/Best Practices/SEO ≥ 90；
  - KR2：WCAG 2.2 AA 通过人工与自动化抽检；
  - KR3：Schema.org Rich Results 通过检测。

  





------





## **2. 信息架构（IA）与导航**





**顶级导航（桌面端）**：



1. Research 2) Publications 3) Talks & Teaching 4) Projects 5) SciXchange 6) Blog 7) Interests 8) CV 9) Contact





> 移动端采用汉堡菜单；首页提供 CTA：**View Publications** / **Read the Blog** / **Contact**。



**页脚**：版权/许可、ORCID、Google Scholar、GitHub、LinkedIn、Email、RSS、隐私、Sitemap。



------





## **3. 页面与模块规格**







### **3.1 首页（Home）**





- **Hero**：姓名 + 研究头衔 + 2–3 句研究概述 + 副标题“*Dream big, act little.*”；按钮（View Publications / Read the Blog）。
- **Publications Spotlight**：3–5 篇代表作卡片（标题、期刊/年份、作者前 3 名 + *et al.*, DOI/Preprint/Code/Data 链接）。
- **Research Themes**：3–4 张主题卡（≤80 字/卡 + 图标/示意图），链接到 Research。
- **Latest Blog**：最新 3 篇。
- **SciXchange Teaser**：80–120 字 + “Learn More”。
- **Identity Badges**：ORCID / Scholar / GitHub / LinkedIn。







### **3.2 Research**





- **结构**：Why → What → How → So what（叙事性段落）。
- **Themes**：每个主题包含：问题陈述、方法（如 optical tweezers、single-molecule fluorescence 等）、代表性结果图/流程图、代表论文、合作方。
- **Open Questions & Future Directions**：条目化。
- **Resources**：方法学笔记/协议（如可公开）、课程材料。







### **3.3 Publications**





- **数据源**：publications.bib（来源：ORCID/Scholar 导出），CI 生成 Markdown。
- **展示**：按年份分组，过滤器（Journal/Preprint/Review/Conference/Dataset/Software），支持全文搜索。
- **字段**（最小集）：标题、作者、期刊/年份、DOI/Preprint/PDF、摘要（≤120 字）、关键词、标签、资源（Code/Data/SI）。
- **功能**：一键复制 BibTeX/APA；外链图标；高亮“Corresponding/First Author”可选。







### **3.4 Talks & Teaching**





- **Talks**：题目、会议/机构、日期、Slides/PDF/Video、致谢/资助。
- **Teaching**：课程（角色/年份/材料）、学生指导/获奖、教学理念短文。







### **3.5 Projects（科研项目 & Tools）**





- 项目卡片列出状态（Active/Paused/Completed）、摘要、方法标签、资源（Repo/Docs/Data）。
- 单页模板：背景 → 目标 → 方法/管线 → 结果要点 → 资源链接。







### **3.6 SciXchange（专页）**





- **愿景**：研究材料的可信流通与复用。
- **核心机制**：身份验证、合规轨道、信用/积分、搜索与发现。
- **用户旅程**：研究者/实验室管理者。
- **当前状态**：内测/等待名单；**加入方式**（表单/邮箱）。
- **FAQ**：合规/IP、材料类型、运输与风控。
- **SEO 区隔**：副标题加注 “Scientific Materials Exchange Network（个人项目）”。







### **3.7 Blog（博客）**





- **内容类型**：

  

  1. Longform（深度方法/评论）
  2. Note（≤300 字速记）
  3. Book/ Paper Card（要点+引文）
  4. Lab Notes（默认 noindex）
  5. Talk Recap（讲稿/海报背后）

  

- **规范**：标题 ≤60 字；首段摘要；图注/引用；每 300–500 字小标题。

- **功能**：全文搜索、标签页、RSS、邮件订阅（Buttondown/Substack）、评论（Giscus 可切换）。

- **可选**：系列化（Series）、阅读时长、目录（TOC）、脚注。







### **3.8 Interests（兴趣）**





- 轻量卡片（≤6 项）：图片、50–80 字说明、相关博文/相册链接。
- 边界：凸显“促进科研与思考”的兴趣，避免隐私化生活流。







### **3.9 CV**





- 页面版 + 可下载 PDF（1–2 页）；
- 自动汇集 Publications/Talks/Teaching 精华条目；
- 打印样式优化（A4、页眉/页脚隐藏）。







### **3.10 Contact**





- 学术邮箱、社交链接；
- 轻表单（Honeypot + 延时 + 可选 reCAPTCHA）；
- 许可与版权说明（博客默认 CC BY 4.0，可覆盖）。





------





## **4. 内容模型（面向实现/自动化）**







### **4.1 Frontmatter（统一字段）**





**Publication**（content/publications/<slug>.md）

```
Title: "DNA polymerase actively and sequentially displaces SSB"
Authors: ["Xu, Longfu", "..."]
Venue: "Journal / Preprint"
Year: 2025
DOI: "10.xxxx/xxxxx"
PreprintURL: "https://..."
PDF: "files/papers/xxxx.pdf"
Code: "https://github.com/..."
Data: "https://zenodo.org/..."
Abstract: "≤120 字摘要"
Tags: [Replication, Single-Molecule]
Featured: true
Thumbnail: "images/papers/ssb.jpg"
CiteKey: "Xu2025SSB"  # 构建脚本生成/校正
```

**Post**（content/blog/<yyyy-mm-dd>-<slug>.md）

```
Title: "Why a decentralized view of replication helps"
Date: 2025-08-01
Type: [Longform]  # Longform | Note | BookCard | LabNote | TalkRecap
Tags: [Meta-Science, Methods]
Summary: "一句话摘要"
Draft: false
Cover: "images/blog/replication.jpg"
Related: ["/publications/xu2025-ssb"]
```

**Project**（content/projects/<slug>.md）

```
Title: "Single-molecule pipeline for DNA packaging"
Status: Active
Summary: "80–120 字"
Repo: "https://github.com/..."
Methods: [Optical Tweezers, Fluorescence]
Collaborators: ["Lab A", "Lab B"]
Resources: ["/files/protocols/xxx.pdf"]
```

**Talk**（content/talks/<date>-<slug>.md）

```
Title: "Mapping fast DNA polymerase exchange"
Event: "Conference/Institution"
Date: 2025-07-02
Slides: "/files/talks/2025-07-02-exchange.pdf"
Video: "https://..."
Acknowledgements: ["Funding A", "Facility B"]
```



### **4.2 标签与分类（建议）**





- **研究主题**：Replication, Packaging, Motor Proteins, Methods, Biophysics
- **博客标签**：Research, Methods, Meta-Science, SciXchange, Career, Notes, Books





------





## **5. 设计系统（Design System）**







### **5.1 视觉**





- **基调**：学术克制、轻科技、充足留白。

- **色板**（对比度≥4.5:1）：

  

  - 主色 DNA Blue #1F5FFF；
  - 中性色：Ink #0B1220、Graphite #3B4252、Silver #E5E7EB、Paper #FAFAFA；
  - 强调 Helix Green #29A68A（按钮/链接悬停）。

  

- **字体**：

  

  - 英文：标题 Inter/Source Sans 3（600/700），正文 Source Serif Pro/Literata；
  - 中文：思源宋体/Noto Serif SC（标题细字距），思源黑体/Noto Sans SC（UI）。

  

- **节奏**：8pt 网格；正文容器宽 720–880px；卡片区 1120px。







### **5.2 组件**





- Publication Card（含 DOI/Preprint/Code/Data 图标按钮）
- Theme Tile（研究主题卡）
- Figure + Caption（支持灯箱放大）
- Callout（Note/Warning/Info）
- Code Block（行号 + 复制）
- Tag/Filter Pills（组合过滤）
- Timeline（Talks/Teaching）
- TOC（文章目录）







### **5.3 交互与动效**





- 键盘可达、Skip to content、可见 :focus；
- 动效最小化（100–200ms 淡入/位移），符合 “act little”；
- 暗色模式：系统跟随 + 手动切换；
- 图像懒加载，font-display: swap。





------





## **6. 技术方案（针对** 

## **longfuxu.github.io**

## **）**





> 约束：GitHub Pages 用户主页仓库（<username>.github.io）可直接服务静态产物。若使用不在白名单内的 Jekyll 插件或其他构建框架，需 **GitHub Actions 预构建** 到 gh-pages 分支或 main 的 /docs 目录。





### **6.1 方案 A（推荐）：Hugo + Hugo Blox Academic**





- **优点**：学术组件现成、性能优秀、内容以 Markdown 为主、学习曲线低。

- **仓库布局**：

  

  - main：源码（Hugo 项目）
  - gh-pages：构建后的静态文件（GitHub Pages 指向）

  

- **关键步骤**：

  

  1. 在 longfuxu.github.io 上初始化 Hugo（extended）；
  2. 引入主题：**Hugo Blox – Academic**；
  3. 建立 content/{home,publications,projects,talks,teaching,blog,interests}；
  4. 添加 scripts/bibtex-to-md.(js|py)，CI 内解析 publications.bib 生成/更新 MD；
  5. 搜索：Pagefind；评论：Giscus；分析：Plausible/Umami；
  6. **GitHub Actions** 构建并推送至 gh-pages。

  

- **Actions 示例**（.github/workflows/deploy.yml）：



```
name: Build & Deploy (Hugo)
on:
  push:
    branches: [main]
  workflow_dispatch:
jobs:
  build-deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
        with: { submodules: true, fetch-depth: 0 }
      - uses: actions/setup-node@v4
        with: { node-version: '20' }
      - uses: peaceiris/actions-hugo@v2
        with: { hugo-version: '0.128.0', extended: true }
      - name: Generate Publications from BibTeX
        run: |
          node scripts/bibtex-to-md.js
      - name: Build
        run: hugo --minify
      - name: Deploy
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./public
          publish_branch: gh-pages
```



### **6.2 方案 B：Next.js + MDX + Contentlayer**





- **优点**：高度可定制、组件化强、MDX 适合图文/公式/交互。
- **要点**：@next/mdx + contentlayer 建立类型安全数据层；next/image 优化；Pagefind 静态搜索；导出静态站点（next export）或服务端（Vercel）。
- **Actions 示例**：



```
name: Build & Deploy (Next.js)
on:
  push:
    branches: [main]
  workflow_dispatch:
jobs:
  build-deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-node@v4
        with: { node-version: '20' }
      - run: npm ci
      - run: npm run build && npm run export  # out/
      - name: Deploy
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./out
          publish_branch: gh-pages
```



### **6.3 GitHub Pages 设置**





- **Pages Source**：gh-pages 分支（根目录）。
- **自定义域（可选）**：当前使用 longfuxu.github.io；如后续绑定自定义域，需配置 CNAME、A/AAAA 记录。
- **强制 HTTPS**：开启。





------





## **7. 搜索、订阅、评论与分析**





- **搜索**：Pagefind（构建时生成索引；不依赖第三方服务）。
- **RSS**：/index.xml（全站）+ /blog/index.xml（博客）。
- **订阅**：邮件订阅集成（Buttondown/Substack 二选一）。
- **评论**：Giscus（基于 GitHub Discussions；默认关闭，文级别开启）。
- **分析**：Plausible/Umami（无 Cookie、GDPR 友好）。





------





## **8. SEO、结构化数据与可访问性**





- **基础**：每页自定义 <title>、<meta name="description">、canonical、OG/Twitter 卡片。

- **结构化数据（JSON-LD）**：

  

  - Person（含 affiliation、sameAs：ORCID/Scholar/GitHub/LinkedIn）；
  - ScholarlyArticle（Publications 列表与详情）；
  - Project（Projects/SciXchange）。

  

- **站点地图**：sitemap.xml + robots.txt。

- **可访问性**：键盘可达、焦点可见、语义标签、表单标签、图像 alt、MathJax/KaTeX 的可读替身，WCAG 2.2 AA。





------





## **9. 内容迁移与上稿（基于现有仓库）**





1. **备份与分支**：给当前 main 打 tag（如 pre-redesign），新建分支 redesign。

2. **选择技术方案**（A 或 B），搭框架与目录。

3. **导入学术内容**：从 ORCID/Scholar 导出 publications.bib → 运行脚本 → 生成 content/publications/*.md。

4. **创建首批页面**：Home / Research / Publications / Blog / SciXchange / Contact（最小可用）。

5. **首批博客**（建议 3–5 篇）：

   

   - 研究叙事（Why this problem）
   - 方法学（单分子测量中的常见陷阱）
   - 读书/论文卡片
   - SciXchange 初心与路线（非宣传，强调问题与边界）
   - 短札合集（Note）

   

6. **素材**：头像、实验装置/流程图、SciXchange 标识、CV PDF。

7. **搜索/评论/分析**：接入并验证。

8. **CI/CD**：Actions 打通，gh-pages 生效；开启 Pages 强制 HTTPS。

9. **验收与发布**：按 §12 验收清单；切回 main→合并→发布。

10. **维护**：每月更新 publications、每月至少 1–2 篇博客；季度做 Lighthouse 与可访问性复测。





------





## **10. 线框（文字版）**





- **Home**：导航 → Hero（左文本右图）→ Publications Spotlight（三列）→ Research Themes（四宫格）→ Latest Blog（三卡）→ SciXchange 概览 → Footer。
- **Publications**：顶部过滤（Pills）+ 年份锚点目录（右侧），列表项可展开摘要与外链。
- **Blog**：顶部分类 Tabs + 搜索框；卡片流；文章页窄栏 + 右侧 TOC + 脚注/参考文献 + 相关阅读。
- **SciXchange**：愿景横幅 → 机制流程图 → 用户旅程 → FAQ → 加入表单。
- **Interests**：2×N 图片卡片，点入合集/相关博文。
- **CV/Contact**：CV 左侧概览右侧细节；Contact 邮箱/社交/表单。





------





## **11. 文件与目录结构（建议）**



```
/ (repo root: longfuxu.github.io)
  ├─ content/
  │   ├─ home/
  │   ├─ publications/
  │   ├─ projects/
  │   ├─ talks/
  │   ├─ teaching/
  │   ├─ blog/
  │   └─ interests/
  ├─ assets/
  │   ├─ images/
  │   └─ files/
  ├─ static/            # 公共静态资源（Hugo）或 public/（Next）
  ├─ scripts/
  │   └─ bibtex-to-md.js
  ├─ layouts/           # 或 themes/...
  ├─ config/            # Hugo 配置 或 next.config.js 等
  ├─ .github/workflows/deploy.yml
  └─ README.md
```



------





## **12. 验收标准（Acceptance Criteria）**





- **导航与可用性**

  

  - 顶部导航与页脚一致；移动端汉堡菜单；Skip to content；焦点可见。
  - 首页 5 秒可理解研究主题与身份，CTA 明确。

  

- **Publications**

  

  - 年份分组、过滤与搜索可用；每条含 DOI/预印本/代码/数据（如有）；BibTeX/APA 复制按钮可用。
  - 代表作 Spotlight 正确展示且可跳转到详情。

  

- **Blog**

  

  - 五类模版可用；RSS 与全文搜索可用；评论可按文开启/关闭。
  - 文章页含 TOC、脚注、引用、阅读时长（可选）。

  

- **SciXchange**

  

  - 独立落地页，含愿景/机制/旅程/FAQ/加入方式；元信息中加入“个人项目”标注。

  

- **性能与可访问性**

  

  - Lighthouse 四维 ≥90；CLS < 0.1，LCP < 2.5s（桌面/移动）；图像懒加载；font-display: swap。
  - WCAG 2.2 AA：色彩对比、替代文本、键盘可达、表单标签、语言属性设置。

  

- **SEO**

  

  - 每页唯一 <title>/description；canonical；OG/Twitter；JSON-LD（Person/ScholarlyArticle/Project）。
  - sitemap.xml 与 robots.txt 存在且有效。

  

- **稳定性与部署**

  

  - GitHub Actions 成功触发与部署；gh-pages 正常服务；强制 HTTPS；无 404/控制台错误。
  - README 说明构建与内容写作流程。

  





------





## **13. 风险与对策**





- **同名“SciXchange”混淆** → 在页面标题/描述/JSON-LD 中追加 “Scientific Materials Exchange Network（个人项目）”，并在站内声明非隶属关系。
- **论文图像版权** → 使用自有或出版社允许再利用的图；必要时以示意图替代并注明来源。
- **GitHub Pages 插件限制** → 采用 Actions 预构建到 gh-pages，避免白名单限制。
- **内容更新负担** → 通过 publications.bib + 脚本自动增量生成；博客模板化降低写作摩擦。





------





## **14. 实施计划（以** 

## **longfuxu.github.io**

##  **为准）**







### **里程碑**





- **M1（Day 1–2）**：仓库备份与框架选型完成；Actions 跑通（空站点）。
- **M2（Day 3–5）**：IA 完整搭建；Home/Research/Publications/Blog/SciXchange MVP。
- **M3（Day 6–7）**：Publications 批量导入；样式与组件完善；搜索/订阅/评论接入。
- **M4（Day 8–9）**：可访问性与性能优化；SEO/结构化数据校验。
- **M5（Day 10）**：验收与发布；README 与维护手册完善。







### **角色分工**





- **内容**：产品负责人提供简介、publications.bib、首批博客与素材。
- **前端/建站**：开发者/AI 依据本 PRD 完成框架、组件与部署。
- **校对**：检查学术条目与外链准确性。





------





## **15. 文案模板（可直接复用）**





**首页简介（About，2–3 句）**



> I’m a biophysicist studying viral DNA replication and packaging with single-molecule approaches. My current work focuses on … I’m also building **SciXchange** — a Scientific Materials Exchange Network to make research more efficient. *Dream big, act little.*



**SciXchange 愿景（80–120 字）**



> Unlock idle research materials in labs via trusted identity, compliance rails, and a credit-based exchange network. Start with academia, expand to broader R&D.



**兴趣卡片示例**



> *Science Writing* — Notes on clarity, visuals, and evidence. 相关：#Meta-Science, #Books



------





## **16. JSON-LD 片段（示例，可按需调整）**





**Person（放在首页）**

```
<script type="application/ld+json">
{
  "@context":"https://schema.org",
  "@type":"Person",
  "name":"Longfu Xu",
  "jobTitle":"Biophysicist",
  "url":"https://longfuxu.github.io",
  "sameAs":[
    "https://orcid.org/XXXX-XXXX-XXXX-XXXX",
    "https://scholar.google.com/citations?user=XXXX",
    "https://github.com/longfuxu",
    "https://www.linkedin.com/in/XXXX"
  ],
  "affiliation":{"@type":"Organization","name":"Your Lab / Institution"}
}
</script>
```

**ScholarlyArticle（用于 Publications 详情页，构建时注入）**

```
<script type="application/ld+json">
{
  "@context":"https://schema.org",
  "@type":"ScholarlyArticle",
  "name":"DNA polymerase actively and sequentially displaces SSB",
  "author":[{"@type":"Person","name":"Longfu Xu"}],
  "datePublished":"2025",
  "isPartOf":{"@type":"Periodical","name":"Journal / Preprint Server"},
  "identifier":"https://doi.org/10.xxxx/xxxxx",
  "url":"https://longfuxu.github.io/publications/xu2025-ssb"
}
</script>
```



------





## **17. 交付物清单**





1. **源代码仓库**：完整可构建项目（Hugo 或 Next.js），含 README.md。

2. **GitHub Actions**：deploy.yml 可用，自动构建并发布到 gh-pages。

3. **设计系统**：色板、字体、组件示意（SVG/Icon 集）。

4. **内容样例**：

   

   - content/publications/xu2025-ssb.md
   - content/blog/2025-08-01-decentralized-replication.md
   - content/projects/dna-packaging-pipeline.md
   - content/talks/2025-07-02-exchange.md

   

5. **脚本**：scripts/bibtex-to-md.js（BibTeX → MD）。

6. **站点地图与法律页**：sitemap.xml、robots.txt、/legal（隐私与许可模板）。





------





## **18. 维护计划**





- **每月**：同步 publications.bib、发布 1–2 篇博文、巡检外链。
- **每季度**：Lighthouse/可访问性复测、依赖升级、备份 assets/。
- **自动化**：对 publications.bib 的改动触发生成脚本与增量构建。





------





## **19. 附：博客模版（MD/MDX 片段）**





**Longform（头部 + 结构）**

```
---
Title: "Title of the longform post"
Date: 2025-08-01
Type: [Longform]
Tags: [Methods, Meta-Science]
Summary: "一句话摘要，60–120 字"
Cover: "images/blog/cover.jpg"
---

# 引子（问题与动机）

## 背景与相关工作

## 方法/观察

## 结果/启示

## 限制与待验证

> 注：图表需配图注与来源；引用请使用标准格式。
```

**Note（速记）**

```
---
Title: "On polymerase exchange at high loads"
Date: 2025-08-03
Type: [Note]
Tags: [Notes, Replication]
Summary: "一句话速记"
---

- 关键观察 1
- 关键观察 2
- Next steps: ...
```



------



**本 PRD 针对 longfuxu.github.io 直接可实施；选择方案 A 或 B 任一即可达成 MVP。若仅实现最小集，请优先完成：Home、Publications、Blog、SciXchange + 搜索/订阅/部署与结构化数据。**