---
name: seo-geo
description: SEO & GEO (Generative Engine Optimization) for websites. Analyze keywords, generate schema markup, optimize for AI search engines (ChatGPT, Perplexity, Gemini, Copilot, Claude) and traditional search (Google, Bing). Use when user wants to improve search visibility, search optimization, search ranking, AI visibility, ChatGPT ranking, Google AI Overview, indexing, JSON-LD, meta tags, or keyword research.
---

# SEO/GEO Optimization Skill / SEO/GEO 优化技能

Comprehensive SEO and GEO (Generative Engine Optimization) for websites. Optimize for both traditional search engines (Google, Bing) and AI search engines (ChatGPT, Perplexity, Gemini, Copilot, Claude).

> 全面的 SEO 与 GEO（生成式引擎优化）技能。同时针对传统搜索引擎（Google、Bing）和 AI 搜索引擎（ChatGPT、Perplexity、Gemini、Copilot、Claude）优化网站。

## Quick Reference / 快速参考

**GEO = Generative Engine Optimization** - Optimizing content to be cited by AI search engines.

> GEO = 生成式引擎优化——优化内容，使其被 AI 搜索引擎引用。

**Key Insight:** AI search engines don't rank pages - they **cite sources**. Being cited is the new "ranking #1".

> **核心洞察：** AI 搜索引擎不对页面进行排名——它们**引用来源**。被引用，就是新的「排名第一」。

## Workflow / 工作流程

### Step 1: Website Audit / 第一步：网站审计

Get the target URL and analyze current SEO/GEO status.

> 获取目标 URL 并分析当前 SEO/GEO 状态。

**Basic SEO Audit (Free):** / **基础 SEO 审计（免费）：**
```bash
python3 scripts/seo_audit.py "https://example.com"
```
**Use this for**: Quick technical SEO check (title, meta, H1, robots, sitemap, load time). No API needed.

> **用途**：快速技术 SEO 检查（title、meta、H1、robots、sitemap、加载时间）。无需 API。

---

**Check Meta Tags:** / **检查 Meta 标签：**
```bash
curl -sL "https://example.com" | grep -E "<title>|<meta name=\"description\"|<meta property=\"og:|application/ld\+json" | head -20
```

**Use this for**: Quick check of essential meta tags and schema markup on any webpage.

> **用途**：快速检查任何网页的核心 meta 标签和 schema 标记。

---

**Check robots.txt:** / **检查 robots.txt：**
```bash
curl -s "https://example.com/robots.txt"
```

**Use this for**: Verify which bots are allowed/blocked. Critical for ensuring AI search engines can crawl your site.

> **用途**：验证哪些爬虫被允许/屏蔽。对于确保 AI 搜索引擎能抓取你的网站至关重要。

---

**Check sitemap:** / **检查 sitemap：**
```bash
curl -s "https://example.com/sitemap.xml" | head -50
```

**Use this for**: Verify sitemap structure and ensure all important pages are included for search engine discovery.

> **用途**：验证 sitemap 结构，确保所有重要页面都被搜索引擎发现。

**Verify AI Bot Access:** / **验证 AI 爬虫访问权限：**
```
# These bots should be allowed in robots.txt:
# 以下爬虫应在 robots.txt 中允许访问：
- Googlebot (Google)
- Bingbot (Bing/Copilot)
- PerplexityBot (Perplexity)
- ChatGPT-User (ChatGPT with browsing) / ChatGPT-User（带浏览功能的 ChatGPT）
- ClaudeBot / anthropic-ai (Claude)
- GPTBot (OpenAI)
```

### Step 2: Keyword Research / 第二步：关键词研究

Use **WebSearch** to research target keywords:

> 使用 **WebSearch** 工具研究目标关键词：

```
WebSearch: "{keyword} keyword difficulty site:ahrefs.com OR site:semrush.com"
WebSearch: "{keyword} search volume 2026"
WebSearch: "site:{competitor.com} {keyword}"
```

**Analyze:** / **分析：**
- Search volume and difficulty / 搜索量和难度
- Competitor keyword strategies / 竞品关键词策略
- Long-tail keyword opportunities / 长尾关键词机会
- International keyword conflicts (e.g., "OPC" = industrial automation in English markets) / 国际关键词冲突（例如 "OPC" 在英文市场 = 工业自动化）

### Step 3: GEO Optimization (AI Search Engines) / 第三步：GEO 优化（AI 搜索引擎）

Apply the **9 Princeton GEO Methods** (see [references/geo-research.md](./references/geo-research.md)):

> 应用 **9 种普林斯顿 GEO 方法**（参见 [references/geo-research.md](./references/geo-research.md)）：

| Method / 方法 | Visibility Boost / 可见性提升 | How to Apply / 如何应用 |
|--------|-----------------|--------------|
| **Cite Sources** / 引用来源 | +40% | Add authoritative citations and references / 添加权威引用和参考文献 |
| **Statistics Addition** / 添加统计数据 | +37% | Include specific numbers and data points / 包含具体数字和数据点 |
| **Quotation Addition** / 添加引言 | +30% | Add expert quotes with attribution / 添加带署名的专家引言 |
| **Authoritative Tone** / 权威语气 | +25% | Use confident, expert language / 使用自信、专业的语言 |
| **Easy-to-understand** / 易于理解 | +20% | Simplify complex concepts / 简化复杂概念 |
| **Technical Terms** / 专业术语 | +18% | Include domain-specific terminology / 包含领域专有术语 |
| **Unique Words** / 独特词汇 | +15% | Increase vocabulary diversity / 增加词汇多样性 |
| **Fluency Optimization** / 流畅度优化 | +15-30% | Improve readability and flow / 提升可读性和流畅度 |
| ~~Keyword Stuffing~~ / ~~关键词堆砌~~ | **-10%** | **AVOID - hurts visibility** / **避免——会降低可见性** |

**Best Combination:** Fluency + Statistics = Maximum boost

> **最佳组合：** 流畅度 + 统计数据 = 最大提升

**Generate FAQPage Schema** (+40% AI visibility) / **生成 FAQPage Schema**（+40% AI 可见性）：
```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [{
    "@type": "Question",
    "name": "What is [topic]?",
    "acceptedAnswer": {
      "@type": "Answer",
      "text": "According to [source], [answer with statistics]."
    }
  }]
}
```

**Optimize Content Structure:** / **优化内容结构：**
- Use "answer-first" format (direct answer at top) / 使用「答案前置」格式（直接答案放在顶部）
- Clear H1 > H2 > H3 hierarchy / 清晰的 H1 > H2 > H3 层级
- Bullet points and numbered lists / 项目符号和编号列表
- Tables for comparison data / 用表格展示对比数据
- Short paragraphs (2-3 sentences max) / 短段落（最多 2-3 句）

### Step 4: Traditional SEO Optimization / 第四步：传统 SEO 优化

**Meta Tags Template:** / **Meta 标签模板：**
```html
<title>{Primary Keyword} - {Brand} | {Secondary Keyword}</title>
<meta name="description" content="{Compelling description with keyword, 150-160 chars}">
<meta name="keywords" content="{keyword1}, {keyword2}, {keyword3}">

<!-- Open Graph -->
<meta property="og:title" content="{Title}">
<meta property="og:description" content="{Description}">
<meta property="og:image" content="{Image URL 1200x630}">
<meta property="og:url" content="{Canonical URL}">
<meta property="og:type" content="website">

<!-- Twitter Cards -->
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="{Title}">
<meta name="twitter:description" content="{Description}">
<meta name="twitter:image" content="{Image URL}">
```

**JSON-LD Schema** (see [references/schema-templates.md](./references/schema-templates.md)):
> **JSON-LD Schema**（参见 [references/schema-templates.md](./references/schema-templates.md)）：

- WebPage / Article for content pages / WebPage / Article：用于内容页
- FAQPage for FAQ sections / FAQPage：用于 FAQ 区块
- Product for product pages / Product：用于产品页
- Organization for about pages / Organization：用于关于页面
- SoftwareApplication for tools/apps / SoftwareApplication：用于工具/应用

**Check Content:** / **检查内容：**
- [ ] H1 contains primary keyword / H1 包含主关键词
- [ ] Images have descriptive alt text / 图片有描述性 alt 文本
- [ ] Internal links to related content / 内链到相关内容
- [ ] External links have `rel="noopener noreferrer"` / 外链有 `rel="noopener noreferrer"`
- [ ] Content is mobile-friendly / 内容适配移动端
- [ ] Page loads in < 3 seconds / 页面加载 < 3 秒

### Step 5: Validate & Monitor / 第五步：验证与监控

**Schema Validation:** / **Schema 验证：**
```bash
# Open Google Rich Results Test / 打开 Google Rich Results 测试
open "https://search.google.com/test/rich-results?url={encoded_url}"

# Open Schema.org Validator / 打开 Schema.org 验证器
open "https://validator.schema.org/?url={encoded_url}"
```

**Check Indexing Status:** / **检查索引状态：**
```bash
# Google (use Search Console API or manual check) / Google（使用 Search Console API 或手动检查）
open "https://www.google.com/search?q=site:{domain}"

# Bing
open "https://www.bing.com/search?q=site:{domain}"
```

**Generate Report:** / **生成报告：**
```markdown
## SEO/GEO Optimization Report / SEO/GEO 优化报告

### Current Status / 当前状态
- Meta Tags / Meta 标签: ✅/❌
- Schema Markup / Schema 标记: ✅/❌
- AI Bot Access / AI 爬虫访问: ✅/❌
- Mobile Friendly / 移动端适配: ✅/❌
- Page Speed / 页面速度: X seconds / X 秒

### Recommendations / 优化建议
1. [Priority 1 action / 优先级 1 操作]
2. [Priority 2 action / 优先级 2 操作]
3. [Priority 3 action / 优先级 3 操作]

### GEO Optimizations Applied / 已应用的 GEO 优化
- [ ] FAQPage schema added / 已添加 FAQPage schema
- [ ] Statistics included / 已包含统计数据
- [ ] Citations added / 已添加引用
- [ ] Answer-first structure / 答案前置结构
```

## Platform-Specific Optimization / 各平台专项优化

See [references/platform-algorithms.md](./references/platform-algorithms.md) for detailed ranking factors.

> 详细的排名因素参见 [references/platform-algorithms.md](./references/platform-algorithms.md)。

### ChatGPT
- Focus on **branded domain authority** (cited 11% more than third-party) / 关注**品牌域名权威度**（比第三方域名引用率高 11%）
- Update content within **30 days** (3.2x more citations) / 在 **30 天内**更新内容（引用量提升 3.2 倍）
- Build **backlinks** (>350K referring domains = 8.4 avg citations) / 建设**反向链接**（>35 万引用域 = 平均 8.4 次引用）
- Match content style to ChatGPT's response format / 将内容风格匹配 ChatGPT 的回答格式

### Perplexity
- Allow **PerplexityBot** in robots.txt / 在 robots.txt 中允许 **PerplexityBot**
- Use **FAQ Schema** (higher citation rate) / 使用 **FAQ Schema**（更高的引用率）
- Host **PDF documents** (prioritized for citation) / 托管 **PDF 文档**（优先被引用）
- Focus on **semantic relevance** over keywords / 关注**语义相关性**而非关键词

### Google AI Overview (SGE)
- Optimize for **E-E-A-T** (Experience, Expertise, Authority, Trust) / 优化 **E-E-A-T**（经验、专业、权威、信任）
- Use **structured data** (Schema markup) / 使用**结构化数据**（Schema 标记）
- Build **topical authority** (content clusters + internal linking) / 建设**主题权威度**（内容集群 + 内链）
- Include **authoritative citations** (+132% visibility) / 包含**权威引用**（+132% 可见性）

### Microsoft Copilot / Bing
- Ensure **Bing indexing** (required for citation) / 确保 **Bing 索引**（被引用的必要条件）
- Optimize for **Microsoft ecosystem** (LinkedIn, GitHub mentions help) / 优化 **Microsoft 生态**（LinkedIn、GitHub 提及有帮助）
- Page speed **< 2 seconds** / 页面速度 **< 2 秒**
- Clear **entity definitions** / 清晰的**实体定义**

### Claude AI
- Ensure **Brave Search indexing** (Claude uses Brave, not Google) / 确保 **Brave Search 索引**（Claude 使用 Brave 而非 Google）
- High **factual density** (data-rich content preferred) / 高**事实密度**（偏好数据丰富的内容）
- Clear **structural clarity** (easy to extract) / 清晰的**结构层次**（易于提取）

## Cross-Border Brand Modules / 出海品牌专属模块

These three modules are designed specifically for Chinese brands going global — AI SaaS, consumer products, DTC e-commerce. Use these when the target site is a cross-border brand.

> 以下三个模块专为中国出海品牌设计——AI SaaS、消费品、DTC 电商。当目标网站是跨境品牌时使用。

### 🚀 Quick Diagnostic Path (15 min) / 快速诊断路径（15 分钟）

If you're a brand owner with limited time, run these three checks first. Each catches the most expensive mistakes.

> 如果你是品牌方、时间有限，先跑这三步。每一步排查最贵的错误。

| Step / 步骤 | Check / 检查 | Why / 为什么 | Time / 耗时 |
|---|---|---|---|
| 1 | Does your robots.txt allow AI bots? / robots.txt 放了 AI 爬虫吗？ | If no, your site is invisible to ChatGPT/Perplexity. The #1 cheapest fix. / 不放 = 你的网站对 ChatGPT/Perplexity 不可见。最便宜的第一修复。 | 2 min |
| 2 | Do you have FAQPage schema? / 有 FAQPage schema 吗？ | Without it, you lose +40% AI citation rate. This is the single highest-ROI GEO action. / 不加 = 损失 +40% AI 引用率。GEO 里 ROI 最高的单项操作。 | 5 min |
| 3 | Is your homepage answering "what is this, where is it from, and who trusts it" in plain text? / 首页有没有用纯文本回答「这是什么、来自哪里、谁信任它」 | AI engines extract plain-text meaning, not hero images. If a visitor skims your homepage in 5 seconds and can't answer these three questions, neither can AI. / AI 搜索引擎提取的是纯文本语义，不是 hero 图。如果一个访客 5 秒扫完首页答不出这三个问题，AI 也答不出。 | 8 min |

> If all three pass → dig into the modules below. If any fail → fix them before doing anything else.
>
> 三步全过 → 进入下方模块深入优化。有任何一个不过 → 先改它，别的都排后面。

### Shopify SEO Checklist / Shopify SEO 清单

Full checklist for Shopify stores: collection pages, product pages, blog, technical SEO, app warnings, and quick audit commands.
> Shopify 店铺完整清单：合集页、产品页、博客、技术 SEO、App 避坑指南、快速审计命令。

📄 → [references/shopify-seo-checklist.md](./references/shopify-seo-checklist.md)

### Cross-Border & Multilingual SEO / 跨境多语言 SEO

hreflang implementation, URL structure strategy (subdirectory vs subdomain vs ccTLD), translation vs localization, international keyword research, Google Search Console targeting, and common anti-patterns for Chinese brands.
> hreflang 实现、URL 结构策略、翻译 vs 本地化的区别、国际关键词研究、GSC 定向、中国品牌常见反模式。

📄 → [references/cross-border-multilingual-seo.md](./references/cross-border-multilingual-seo.md)

### Global Brand GEO Templates / 出海品牌 GEO 模板

Ready-to-use FAQPage JSON-LD templates for AI SaaS and consumer brands, "Trust-First" landing page structure, comparison page template, GEO checklist, and a real scored example (AhaCreator 71/100).
> 开箱即用的 FAQPage JSON-LD 模板（AI SaaS / 消费品）、信任优先落地页结构、竞品对比页模板、GEO 检查清单、真实评分案例。

📄 → [references/global-brand-geo-templates.md](./references/global-brand-geo-templates.md)

## Skill Dependencies / 技能依赖

This skill works best with: / 本技能与以下工具配合最佳：
- **twitter skill** - Search SEO experts for latest tips / 搜索 SEO 专家的最新建议
- **reddit skill** - Search r/SEO, r/bigseo for discussions / 搜索 r/SEO、r/bigseo 的讨论
- **WebSearch** - Keyword research and competitor analysis / 关键词研究和竞品分析

## Operating Modes / 操作模式

### Mode 1: Free Mode (Default) / 模式一：免费模式（默认）

Uses `web_search` + `web_fetch` for keyword research, `curl` for meta/robots/sitemap checks, and `seo_audit.py` for basic audits. No API key required.

> 使用 `web_search` + `web_fetch` 进行关键词研究，`curl` 进行 meta/robots/sitemap 检查，`seo_audit.py` 进行基础审计。无需 API key。

### Mode 2: API Mode (Optional) / 模式二：API 模式（可选）

For precise search volume, keyword difficulty scores, and SERP feature analysis, register a free DataForSEO account (1,000 free API calls/month) and add your credentials to `scripts/credential.py`. The scripts in `scripts/` will automatically use the API when credentials are configured.

> 如需精确搜索量、关键词难度分和 SERP 特征分析，注册 DataForSEO 免费账户（每月 1,000 次免费调用），将凭证填入 `scripts/credential.py`。配置后 scripts/ 中的脚本将自动使用 API。

**How it affects results:** / **对判断结果的影响：**
- Without API: Directional insight from public data — you'll know whether a keyword is competitive, but not the exact difficulty score / 没有 API：从公开数据获得方向性判断——你会知道某个词是否竞争激烈，但拿不到精确难度分
- With API: Precise metrics (search volume, KD score, SERP features) enabling data-driven prioritization / 有 API：精确指标（搜索量、KD 分、SERP 特征），支持数据驱动的优先级排序

### Step 6: Score & Benchmark / 第六步：评分与行业对标

After the audit is complete, calculate a composite score out of 100 and estimate the site's percentile ranking against industry peers.

> 审计完成后，计算满分 100 的综合评分，并估算网站在行业中的百分位排名。

#### Scoring Rubric (100 Points) / 评分标准（100 分）

**1. Meta & Social Tags (15 pts) / Meta 与社交标签（15 分）**

| Factor / 因素 | Points / 分值 | Condition / 条件 |
|---|---|---|
| Title length / 标题长度 | 5 | 40-60 chars = 5, 60-70 or 30-40 = 3, < 30 or > 70 = 1 |
| Description quality / 描述质量 | 5 | 130-160 chars with keyword = 5, 100-130 = 3, < 100 or > 160 or missing = 1 |
| OG + Twitter Cards / OG + Twitter 标签 | 5 | Both present with image = 5, one set only = 3, missing = 0 |

**2. Schema Markup (15 pts) / 结构化数据（15 分）**

| Factor / 因素 | Points / 分值 | Condition / 条件 |
|---|---|---|
| Organization schema / 组织 schema | 5 | ✅ / ❌ |
| WebPage or Article schema / WebPage 或 Article schema | 3 | ✅ / ❌ |
| FAQPage schema / FAQ schema | 5 | ✅ / ❌ |
| Product or SoftwareApplication schema / 产品或应用 schema | 2 | ✅ / ❌ (only if applicable / 仅当适用时) |

**3. AI Bot Access (10 pts) / AI 爬虫访问（10 分）**

| Factor / 因素 | Points / 分值 | Condition / 条件 |
|---|---|---|
| robots.txt exists / robots.txt 存在 | 2 | ✅ / ❌ |
| Explicit AI bot rules / 显式 AI 爬虫规则 | 5 | All of PerplexityBot, ChatGPT-User, ClaudeBot, GPTBot = 5, partial = 2, none = 0 |
| Proper disallow rules / 合理屏蔽规则 | 3 | Admin/API paths blocked = 3, no blocking = 1 |

**4. Content Structure (10 pts) / 内容结构（10 分）**

| Factor / 因素 | Points / 分值 | Condition / 条件 |
|---|---|---|
| H1 quality / H1 质量 | 3 | Keyword-rich, descriptive = 3, generic = 1 |
| Heading hierarchy / 标题层级 | 2 | Clear H1 > H2 > H3 = 2, flat or missing = 0 |
| Answer-first format / 答案前置格式 | 2 | Direct answer at top = 2, buried = 0 |
| Statistics present / 包含数据 | 3 | Specific numbers in body = 3, none = 0 |

**5. Performance (10 pts) / 性能（10 分）**

| Load Time / 加载时间 | Points / 分值 |
|---|---|
| < 1 second / < 1 秒 | 10 |
| 1-2 seconds / 1-2 秒 | 8 |
| 2-3 seconds / 2-3 秒 | 5 |
| > 3 seconds / > 3 秒 | 2 |

**6. Mobile Friendly (10 pts) / 移动端适配（10 分）**

| Factor / 因素 | Points / 分值 | Condition / 条件 |
|---|---|---|
| Responsive design / 响应式设计 | 5 | Mobile breakpoints visible = 5 |
| Mobile performance / 移动端性能 | 5 | No mobile-specific issues detected = 5 |

**7. Indexing & Crawling (10 pts) / 索引与抓取（10 分）**

| Factor / 因素 | Points / 分值 | Condition / 条件 |
|---|---|---|
| Sitemap / 站点地图 | 4 | XML sitemap present and updated ≤ 30 days = 4, stale = 2, missing = 0 |
| Canonical URL / 规范链接 | 2 | ✅ / ❌ |
| Meta robots tags / Meta robots 标签 | 2 | Correct index/follow = 2, missing = 0 |
| Search Console verified / Search Console 已验证 | 2 | ✅ / ❌ |

**8. GEO Optimization (20 pts) / GEO 优化（20 分）**

| Princeton Method / 普林斯顿方法 | Points / 分值 | Condition / 条件 |
|---|---|---|
| Cite Sources / 引用来源 | 4 | Authoritative citations visible in content |
| Statistics Addition / 统计数据 | 4 | Specific data points visible |
| Quotation Addition / 引用引言 | 3 | Expert quotes present |
| Authoritative Tone / 权威语气 | 3 | Confident, expert language |
| Easy-to-understand / 易于理解 | 2 | Plain language for complex concepts |
| Technical Terms / 专业术语 | 2 | Domain-specific terminology used |
| Unique Words / 独特词汇 | 1 | Vocabulary diversity visible |
| Fluency Optimization / 流畅度 | 1 | Natural readability |

> **Note on GEO scoring / GEO 评分说明：** The GEO section is scored based on what is observable from the page content itself (statistics, citations, tone). For sites that provide these signals clearly in their homepage content, the score reflects that. For minimalist landing pages that link to sub-pages for detail, score based on the most visible content layer.
>
> GEO 部分基于页面内容本身可观察到的内容评分（统计数据、引用、语气）。对于在首页内容中清晰展示这些信号的网站，分数反映实际情况。对于将详情放在子页面的极简落地页，基于首页可见内容层评分。

#### Industry Benchmarking / 行业对标

Apply this tier map to determine the site's percentile rank:

> 使用以下等级对照表确定网站的百分位排名：

| Score / 分数 | Percentile / 百分位 | Label / 评级 | What It Means / 含义 |
|---|---|---|---|
| 92-100 | Top 1% / 前 1% | 🏆 World-class / 世界级 | Enterprise-grade SEO + full GEO; cited by AI search engines. / 企业级 SEO + 全量 GEO；被 AI 搜索引擎引用。 |
| 82-91 | Top 5% / 前 5% | 🥇 Excellent / 卓越 | Strong SEO foundations + partial GEO; ready for AI visibility. / 强 SEO 基础 + 部分 GEO；AI 可见性就绪。 |
| 70-81 | Top 15% / 前 15% | 🥈 Good / 良好 | Solid traditional SEO, GEO gaps exist. / 扎实的传统 SEO，GEO 有短板。 |
| 55-69 | Top 40% / 前 40% | 🥉 Average / 中等 | Basic SEO present but incomplete; no GEO awareness. / 基础 SEO 存在但不完整；无 GEO 意识。 |
| 40-54 | Bottom 40% / 后 40% | ⚠️ Below Average / 低于平均 | Significant SEO gaps; urgent fixes needed. / 明显 SEO 缺陷；急需修复。 |
| 25-39 | Bottom 15% / 后 15% | 🔴 Poor / 较差 | Minimal optimization; essentially invisible to search. / 极少优化；对搜索引擎基本不可见。 |
| < 25 | Bottom 5% / 后 5% | ❌ Critical / 严重 | No SEO at all; urgent from zero. / 完全无 SEO；需从零开始。 |

#### Output Format / 输出格式

After scoring, produce a summary card:

> 评分完成后，输出以下摘要卡片：

```markdown
## SEO/GEO Scorecard / SEO/GEO 评分卡

### Overall / 综合
**[XX/100]** — Top **X%** of industry peers / 行业前 **X%**

### Breakdown / 分项
- Meta & Social Tags / Meta 与社交标签: X/15
- Schema Markup / 结构化数据: X/15
- AI Bot Access / AI 爬虫访问: X/10
- Content Structure / 内容结构: X/10
- Performance / 性能: X/10
- Mobile Friendly / 移动端适配: X/10
- Indexing & Crawling / 索引与抓取: X/10
- GEO Optimization / GEO 优化: X/20

### Quick Wins / 快速提升
1. [Highest-impact fix / 最高杠杆修复] (+X pts / +X 分)
2. [Second fix / 第二项修复] (+X pts / +X 分)
```

## References / 参考资料

- [references/platform-algorithms.md](./references/platform-algorithms.md) - Detailed ranking factors for each platform / 各平台详细排名因素
- [references/geo-research.md](./references/geo-research.md) - Princeton GEO research (9 methods) / 普林斯顿 GEO 研究（9 种方法）
- [references/schema-templates.md](./references/schema-templates.md) - JSON-LD templates / JSON-LD 模板
- [references/seo-checklist.md](./references/seo-checklist.md) - Complete SEO audit checklist / 完整 SEO 审计清单
- [references/tools-and-apis.md](./references/tools-and-apis.md) - Tools and API reference / 工具和 API 参考
- [references/shopify-seo-checklist.md](./references/shopify-seo-checklist.md) - Shopify SEO: collection, product, blog, app warnings / Shopify SEO 全集
- [references/cross-border-multilingual-seo.md](./references/cross-border-multilingual-seo.md) - Cross-border SEO: hreflang, localization, pitfalls / 跨境 SEO 全攻略
- [references/global-brand-geo-templates.md](./references/global-brand-geo-templates.md) - GEO templates: AI SaaS + consumer brands with scoring / 出海品牌 GEO 模板
- [examples/opc-skills-case-study.md](./examples/opc-skills-case-study.md) - Real-world optimization example / 真实优化案例
