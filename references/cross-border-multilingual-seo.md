# Cross-Border & Multilingual SEO / 跨境多语言 SEO

> Last updated: 2026-07-12
> Target audience: Chinese brands going global / 面向：中国出海品牌

## 1. hreflang: The #1 Mistake / hreflang：最常见的错误

### What hreflang does / hreflang 的作用

Tells Google: "this page is the English version for US users; that page is the Japanese version for JP users." Without it, Google treats all language versions as duplicate content.
> 告诉 Google：「这页是美国英文版，那页是日本日文版」。没有 hreflang，Google 会把所有语言版本当重复内容处理。

### Implementation / 实现方式

```html
<link rel="alternate" hreflang="en-us" href="https://brand.com/us/" />
<link rel="alternate" hreflang="en-gb" href="https://brand.com/uk/" />
<link rel="alternate" hreflang="ja" href="https://brand.com/jp/" />
<link rel="alternate" hreflang="ko" href="https://brand.com/kr/" />
<link rel="alternate" hreflang="x-default" href="https://brand.com/" />
```

`x-default` = fallback for users whose language/region doesn't match any declared hreflang.
> `x-default` = 当用户语言/地区不匹配任何已声明 hreflang 时的回退页面。

### Common hreflang Pitfalls / 常见 hreflang 坑

| Mistake / 错误 | Why It Hurts / 为什么有问题 |
|---|---|
| Missing return tag / 缺少返回标签 | If `/us/` declares hreflang to `/jp/`, then `/jp/` MUST declare back to `/us/`. Missing return = Google ignores both. / 如果 `/us/` 声明 hreflang 到 `/jp/`，那 `/jp/` 必须声明回来。缺一不可。 |
| Using country code without language / 只用国家码不用语言码 | `hreflang="us"` ❌ — must be `hreflang="en-us"` ✅ |
| hreflang to non-canonical URLs / hreflang 指向非 canonical URL | All hreflang URLs must be canonical. / 所有 hreflang URL 必须是 canonical |
| hreflang pointing to redirects / hreflang 指向跳转页 | Google won't follow. Use final destination URLs. / Google 不会跟踪跳转，用最终目标 URL |

---

## 2. URL Structure for Multi-Language / 多语言 URL 结构

| Approach / 方案 | Format / 格式 | SEO Strength / SEO 强度 | When to Use / 适用场景 |
|---|---|---|---|
| ccTLD / 国家顶级域名 | `brand.fr`, `brand.de` | 🏆 Strongest / 最强 | Large budget, separate teams per country / 大预算，各国独立团队 |
| Subdirectory / 子目录 | `brand.com/fr/`, `brand.com/de/` | 🥇 Strong / 强 | **Recommended for most brands** / **推荐大多数品牌** |
| Subdomain / 子域名 | `fr.brand.com`, `de.brand.com` | 🥈 Moderate / 中等 | When CMS can't handle subdirectories / CMS 不支持的备选 |

> **Recommendation for Chinese export brands:** Subdirectory (`brand.com/en/`, `brand.com/jp/`). One domain authority, clean structure, Google treats it naturally.
> **给中国出海品牌的建议：** 用子目录（`brand.com/en/`、`brand.com/jp/`）。单一域名权威度、结构清晰、Google 自然处理。

---

## 3. Translation vs Localization / 翻译 vs 本地化

> This is where most Chinese brands fail: they machine-translate their Chinese content into English and call it "international." That's not SEO — it's a penalty waiting to happen.
> 这是大多数中国品牌踩的坑：把中文内容机翻成英文就当「国际化」了。这不叫 SEO——这是等着被惩罚。

### Translation / 翻译：❌

- Keyword-for-keyword conversion / 逐词转换
- Ignores search intent differences / 忽略搜索意图的差异
- May use terms no one searches / 可能用了没人搜的词
- Example: 翻译 "数据中台" as "data middle platform" — nobody searches that. The English term is "data platform" or "CDP."
- 例：将"数据中台"翻译成 "data middle platform"——没人搜。英文是 "data platform" 或 "CDP"。

### Localization / 本地化：✅

- Research what the target market actually searches / 研究目标市场实际搜什么
- Adapt terminology, tone, and cultural references / 调整术语、语气、文化指涉
- Write original content in the target language (or human-edit machine translation) / 用目标语言写原创内容（或人工修改机翻）
- Example: "双十一大促" → not "Double 11 sale" → "Black Friday-level sale" for US, "Singles' Day sale" for global
- 例："双十一大促" → 不是 "Double 11 sale" → 美国用 "Black Friday-level sale"，全球用 "Singles' Day sale"

### Keyword Localization Checklist / 关键词本地化清单

- [ ] Research target-market keywords separately (don't translate from Chinese) / 独立研究目标市场关键词（不要从中文翻译）
- [ ] Check search volume in target country (not global) / 检查目标国搜索量（不要用全球搜索量）
- [ ] Identify local competitors' keywords / 识别本地竞品关键词
- [ ] Check for cultural false friends / 检查文化假对应词
- [ ] Test your keywords: would a local actually type this? / 测试你的关键词：本地人真会这么搜吗？

---

## 4. Google Search Console: International Targeting / GSC 国际定向

If you use a generic TLD (`.com`), tell Google which country you're targeting:
> 如果用通用 `.com` 域名，告诉 Google 目标国家：

1. GSC → Legacy tools → International Targeting → Country tab
2. Set country for each subdirectory or subdomain
3. Don't set country for truly global pages

> ⚠️ This is a signal, not a directive. Google may still rank you elsewhere.

---

## 5. Cross-Border Content Strategy / 跨境内容策略

### Localized FAQ Pages / 本地化 FAQ 页

Don't translate FAQ — create market-specific FAQ:
> 不要翻译 FAQ——创建市场专属 FAQ：

| Market / 市场 | FAQ Topic Example / FAQ 话题示例 |
|---|---|
| US / 美国 | "Does this ship from a US warehouse?" / 是否从美国仓库发货？ |
| EU / 欧洲 | "Is this CE certified? What about WEEE recycling?" / 是否有 CE 认证？WEEE 回收政策？ |
| Japan / 日本 | "返品・交換の条件は？" / 退换货条件是？ |
| Southeast Asia / 东南亚 | "COD available? What payment methods?" / 支持货到付款吗？支付方式有哪些？ |

### Localized Landing Pages / 本地化落地页

For each target market, create a dedicated landing page:
> 每个目标市场建独立落地页：

- Title: `{Brand} — {Product Category} for {Country} Market | Buy Online` / `{品牌} — {品类}专为{国家}市场 | 线上购买`
- Content: Explain why your product works for this market specifically / 解释为什么你的产品适合这个市场
- Trust signals: Local certification, local warehouse, local customer reviews / 信任信号：本地认证、本地仓、本地客户评价

---

## 6. Market Prioritization: Which Language First / 先做哪个市场

> For brands with limited resources: don't localize into 5 languages at once. Prioritize by TAM, then validate with data.
> 资源有限的品牌：不要一口气做 5 个语言版本。用 TAM 排序，再用数据验证。

### Framework / 框架

| Step / 步骤 | Action / 操作 | Example / 示例 |
|---|---|---|
| 1. List target markets by TAM / 按目标市场可服务市场规模排序 | Rank countries by addressable market size for YOUR product. Not global TAM — YOUR product's TAM. / 按你的产品在该市场的可服务规模排序。不是全球 TAM，是你的产品在该市场的 TAM。 | Smart home brand: US ($12B) → DE ($3.5B) → JP ($2.8B) → UK ($2B) → KR ($1.2B) |
| 2. Launch English first as a single source of truth / 先做英文站作为唯一内容源 | English serves as your global baseline. AI engines index it regardless of user location. Other languages are expansions, not starting points. / 英文站是全局基线。AI 搜索引擎不管用户在哪都索引它。其他语言是扩展，不是起点。 | `brand.com/en/` → canonical source / 规范来源 |
| 3. Watch GSC for organic demand / 用 GSC 观察自然需求 | After 3-6 months, check which countries drive impressions even without localized content. Those are your expansion candidates. / 3-6 个月后看哪些国家没有本地化内容也有 impressions，那就是扩展候选。 | GSC → Performance → Countries tab → filter by impressions |
| 4. Add one language at a time / 一次加一个语言 | Each new language = ongoing maintenance cost (content updates, hreflang sync, localized keywords). Go slow. / 每个新语言 = 持续的维护成本（内容更新、hreflang 同步、本地化关键词）。慢慢来。 | Launch JP → stabilize for 2-3 months → then launch KR |

> **The trap:** Launching 5 languages at once because "we're a global brand." Result: 5 half-baked language versions, none ranking, maintenance nightmare. One language done well beats five done poorly.
> **最常见的坑：** 「我们是全球品牌」所以一口气上 5 个语言版本。结果：5 个半成品版本，没有一个能排名，维护噩梦。一个语言做扎实胜过五个半吊子。

---

## 7. Translation Solutions Comparison / 翻译方案对比

| Solution / 方案 | Cost / 成本 | SEO Safety / SEO 安全性 | Best For / 适合 |
|---|---|---|---|
| **Manual translation** / 人工翻译 | $$$ (专业译者 ¥0.3-0.8/字) | 🏆 Safest / 最安全 | Core pages: homepage, product pages, key landing pages / 核心页面：首页、产品页、关键落地页 |
| **Weglot** | $$ ($15-50/month depending on word count / $15-50/月按字数) | 🥇 Good — creates SEO-friendly subdirectories, manages hreflang / 好——自动创建 SEO 友好的子目录、管理 hreflang | Stores/brands that need auto-translation + professional editing workflow / 需要自动翻译 + 人工编辑流程的店铺 |
| **Translate.com / DeepL API** | $ ($10-15/month + API fees) | 🥈 Moderate — needs manual review on key pages / 中等——关键页面需人工复核 | Blog posts, resource pages, FAQ / 博客、资源页、FAQ |
| **Google Translate widget** / 谷歌翻译小组件 | Free / 免费 | ❌ NOT SEO-friendly — content stays in original language for search engines / 对 SEO 无效——搜索引擎看到的是原语言 | ❌ Never use for SEO / 绝对不要用于 SEO |
| **Shopify Translate & Adapt** | Free (built into Shopify) / 免费（Shopify 内置） | 🥈 Moderate — needs manual review / 中等——需人工复核 | Shopify stores with existing human translators / 已有译者团队的 Shopify 店铺 |

> **Recommendation:** Manual translation for homepage + top 5 product pages. Weglot for everything else. Never use auto-translate without human review on pages you want to rank.
> **建议：** 首页 + Top 5 产品页人工翻译。其余用 Weglot。想排名的页面绝对不要机翻不校。

---

## 8. hreflang via XML Sitemap (for Large Sites) / XML Sitemap 方式实现 hreflang（大规模站点）

For sites with 50+ pages per language, use XML sitemap instead of HTML `<link>` tags. It's more maintainable and Google prefers it at scale.

> 每语言 50+ 页的站点用 XML sitemap 方式，比 HTML `<link>` 标签更易维护，Google 在规模化时也更偏好这种方式。

### Sitemap Implementation / Sitemap 实现

```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9"
        xmlns:xhtml="http://www.w3.org/1999/xhtml">
  <url>
    <loc>https://brand.com/en/product/smart-light</loc>
    <xhtml:link rel="alternate" hreflang="en" href="https://brand.com/en/product/smart-light"/>
    <xhtml:link rel="alternate" hreflang="ja" href="https://brand.com/jp/product/smart-light"/>
    <xhtml:link rel="alternate" hreflang="ko" href="https://brand.com/kr/product/smart-light"/>
    <xhtml:link rel="alternate" hreflang="x-default" href="https://brand.com/en/product/smart-light"/>
  </url>
  <url>
    <loc>https://brand.com/jp/product/smart-light</loc>
    <xhtml:link rel="alternate" hreflang="en" href="https://brand.com/en/product/smart-light"/>
    <xhtml:link rel="alternate" hreflang="ja" href="https://brand.com/jp/product/smart-light"/>
    <xhtml:link rel="alternate" hreflang="ko" href="https://brand.com/kr/product/smart-light"/>
    <xhtml:link rel="alternate" hreflang="x-default" href="https://brand.com/en/product/smart-light"/>
  </url>
</urlset>
```

> **Key rule:** Every URL in the sitemap must list ALL language versions (including itself). Reciprocal linking is still required — just at the sitemap level instead of HTML level.
> **核心规则：** sitemap 里的每个 URL 必须列出**所有**语言版本（包括自己）。返回链接规则仍然适用——只是从 HTML 层移到了 sitemap 层。

---

## 9. Multi-Language SEO Anti-Patterns / 多语言 SEO 反模式

| Anti-Pattern / 反模式 | Fix / 修复 |
|---|---|
| Same content, multiple URLs / 相同内容多 URL | Use hreflang + canonical / 用 hreflang + canonical |
| IP-based auto-redirect / 基于 IP 的自动跳转 | ❌ Googlebot crawls from US IPs — it'll never see your non-US pages. Use a country selector popup (user-initiated). / Googlebot 从美国 IP 抓取——永远看不到非美页面。改用国家选择弹窗（用户主动选择）。 |
| Machine-translated meta tags / 机翻 meta 标签 | Manually write title + description for each language / 手动写每个语言版本的 title + description |
| Mixing languages on one page / 一页混用多语言 | One page = one language. Use hreflang to connect variants. / 一页一语言，用 hreflang 连接变体。 |
