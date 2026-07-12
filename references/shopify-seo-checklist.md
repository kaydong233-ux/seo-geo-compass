# Shopify SEO Checklist / Shopify SEO 清单

> Last updated: 2026-07-12
> Targets: Shopify stores / 适用于：Shopify 店铺

## 1. Collection Pages / 合集页

> Collection 页面是 Shopify SEO 的重灾区——大多数店铺的 auto-generated collection templates 几乎没有 SEO 价值。

### ✅ Must-Have / 必须做

| Check / 检查项 | How / 怎么做 |
|---|---|
| Custom title tag / 自定义标题 | Format / 格式：`{Collection Name} — Buy {Product Type} Online | {Brand}`<br>Don't rely on Shopify's auto-generated title / 不要依赖 Shopify 自动生成的标题 |
| Custom meta description (150-160 chars) / 自定义描述 | Each collection needs a unique description. Include the primary keyword naturally. / 每个合集需要独立描述，自然包含主关键词 |
| H1 = collection name / H1 = 合集名 | Don't use generic "Products" or "Catalog" / 不要用 "Products" 或 "Catalog" |
| Collection description text (250+ words) / 合集描述正文 | Write unique intro text above products. Include FAQ-style Q&A that answers buyer questions. / 在产品上方写独立介绍文字，包含 FAQ 式问答 |
| Internal links from blog posts / 博客内链到合集 | Blog articles → link to relevant collections. This builds topical authority. / 博客文章内链到相关合集，建设主题权威度 |

### 🔶 Should-Do / 建议做

| Check / 检查项 | How / 怎么做 |
|---|---|
| Collection image alt text / 合集图片 alt 文本 | Descriptive, keyword-rich / 描述性关键词 |
| Breadcrumb schema / 面包屑导航 schema | Shopify auto-generates. Verify it's working via Rich Results Test. / Shopify 自动生成，用 Rich Results Test 验证 |
| URL structure / URL 结构 | Keep it clean: `/collections/summer-dresses` ✅ — `/collections/all/summer-dresses` ❌ |

### ❌ Avoid / 避免

- Duplicate collection descriptions (Google penalty) / 合集描述重复（Google 惩罚）
- Empty collection pages with only products / 只有产品没有文字的合集页
- Thin content (< 50 words) / 内容过少（< 50 词）

---

## 2. Product Pages / 产品页

### ✅ Must-Have / 必须做

| Check / 检查项 | How / 怎么做 |
|---|---|
| Product schema (JSON-LD) / 产品 schema | Include: name, description, image, sku, brand, offers (price, currency, availability), aggregateRating, review. Shopify auto-generates basic Product schema — customize it. |
| Unique product description / 独立产品描述 | Never copy manufacturer descriptions. Write original content. / 不要复制厂家描述，写原创内容 |
| Alt text on ALL product images / 所有产品图 alt 文本 | Descriptive + keyword. Every single image. / 描述性 + 关键词，每张图都要 |
| Product title format / 产品标题格式 | `{Product Name} — {Key Feature} | {Brand}`<br>60-70 chars max / 最多 60-70 字符 |
| URL handle / URL 路径 | Clean, keyword-rich: `/products/wool-throw-blanket-grey` ✅ — `/products/copy-of-wool-throw-blanket-grey-1` ❌ |

### 🔶 Should-Do / 建议做

| Check / 检查项 | How / 怎么做 |
|---|---|
| FAQ section per product / 每个产品的 FAQ 区块 | Material, sizing, care, shipping. Wrap in FAQPage schema. / 材质、尺寸、保养、物流，用 FAQPage schema 包裹 |
| Customer review integration / 评价系统 | Use Loox, Judge.me, or Yotpo. Reviews = fresh content + social proof + aggregateRating schema. |
| Video content / 视频内容 | Host product videos (YouTube embed or Shopify-hosted). Video rich results are underused. |
| Variant SEO / 变体 SEO | Each variant should have a unique, crawlable URL with canonical back to main product page. / 每个变体应有独立可抓取的 URL，canonical 指向主产品页 |

---

## 3. Blog / 博客

> Shopify's blog is your SEO engine. Don't waste it.

| Check / 检查项 | How / 怎么做 |
|---|---|
| Blog article → product links / 博客内链产品 | Every blog post should link to 2-3 relevant products or collections |
| Category + tag structure / 分类标签体系 | Clean taxonomy: use categories for topics, tags for subtopics |
| Article schema / 文章 schema | Every post gets Article schema: headline, datePublished, dateModified, author, image |
| 800+ words per post / 每篇 800+ 词 | Google favors depth. Thin blog content doesn't rank. |
| Publish consistency / 发布频率 | At least 2x/month. Google rewards freshness. / 至少每月 2 篇 |

---

## 4. Technical SEO / 技术 SEO

| Check / 检查项 | How / 怎么做 |
|---|---|
| robots.txt / robots.txt | Allow crawling of pages, products, collections, blogs. Block `/cart`, `/checkout`, `/account`, `/admin`. |
| Sitemap / 站点地图 | Shopify auto-generates at `/sitemap.xml`. Verify: no 404, clean child sitemaps. |
| Canonical URLs / 规范链接 | Shopify handles this. Verify: no self-referencing canonical broken, no canonical chains. |
| Redirects / 301 跳转 | Keep < 100 redirects if possible. Redirect chains hurt crawl budget. |
| SSL / HTTPS | Shopify enforces. Verify: no mixed content warnings. |
| Mobile-first / 移动端优先 | Google indexes mobile version. Test your theme on mobile. |
| Page speed / 页面速度 | Shopify CDN handles most of it. Audit your theme + apps: <br>- Limit apps to < 15<br>- Compress images before uploading<br>- Lazy-load below-fold images |

---

## 5. Shopify App Warning List / App 避坑指南

> These apps hurt SEO. Avoid or replace:
> 以下 App 损害 SEO，避免或替换：

| App Type / App 类型 | Problem / 问题 | Alternative / 替代 |
|---|---|---|
| Heavy page builders / 重型页面编辑器 | Slow load, bloated HTML, poor Core Web Vitals / 加载慢、HTML 臃肿、Core Web Vitals 差 | Native Shopify 2.0 sections |
| Popup-heavy apps / 弹窗 App | Intrusive interstitials = Google penalty on mobile / 侵入式弹窗 = 移动端 Google 惩罚 | Delayed popups (30s+), exit-intent only |
| Auto-translate apps / 自动翻译 App | Creates duplicate/thin content across languages / 产生跨语言重复/稀薄内容 | Weglot (SEO-friendly), or manual translation |
| Quantity break / upsell overlays / 加购弹窗 | Can block crawl, hurt mobile UX / 可能阻止爬虫、影响移动端体验 | In-cart upsells only |

---

## 6. Product Review Schema: The Hidden Pitfall / 评价 Schema 的隐性坑

> ⚠️ This is the #1 Shopify SEO bug that store owners don't know about.
> ⚠️ 这是 Shopify 店主最不知道的 SEO 坑。

Shopify review apps (Judge.me, Loox, Yotpo) auto-generate `aggregateRating` schema. But they often **publish empty ratings** (0 reviews) or **aggregateRating without reviewCount**. Google treats this as spam.

> Shopify 评价 App（Judge.me、Loox、Yotpo）会自动生成 `aggregateRating` schema。但它们经常**在 0 条评价时就发布**，或**有 aggregateRating 没 reviewCount**。Google 当垃圾处理。

### Check if your reviews are broken / 检查评价 Schema 是否正常

```bash
curl -s "https://store.com/products/your-product" | grep -A 20 '"@type":"Product"'
```

Look for: / 检查：
- `reviewCount` must be > 0 if `aggregateRating` is present / 有 `aggregateRating` 则 `reviewCount` 必须 > 0
- `ratingValue` must be between 1 and 5 / `ratingValue` 必须在 1-5 之间
- `bestRating` should be 5 / `bestRating` 应为 5

### Fix / 修复

- Judge.me: Settings → JSON-LD → disable until ≥ 1 review / 设置 → JSON-LD → 在 ≥ 1 条评价前关闭
- Loox: Settings → Structured Data → check "only show when reviews exist" / 设置 → 结构化数据 → 勾选「仅有评价时显示」
- Yotpo: Widgets → SEO → toggle structured data to manual / Widgets → SEO → 切换结构化数据为手动

---

## 7. What You Can Fix in Shopify vs What Needs a Developer / 店主能改 vs 需要开发者

> For non-technical store owners: knowing what's in your control saves time and money.
> 给非技术背景的店主：知道什么在你能改的范围内，省时间也省钱。

### ✅ You Can Do Yourself / 你可以自己改

| Task / 操作 | Where / 在哪改 |
|---|---|
| Edit title & meta description / 改标题和描述 | Shopify Admin → Online Store → Preferences |
| Edit page/collection/product SEO fields / 页面 SEO 字段 | Each page editor → "Search engine listing" section |
| Add alt text to images / 给图片加 alt 文本 | Click any image → "Edit alt text" |
| Edit robots.txt / 改 robots.txt | Online Store → Themes → "..." → Edit code → Templates → robots.txt.liquid |
| Write/rewrite product descriptions / 写产品描述 | Product editor — just type |
| Change URL handle / 改 URL 路径 | Product/page editor → "Search engine listing" → URL handle |
| Add FAQ section to product pages / 加产品 FAQ | Use Shopify 2.0 sections or theme customizer |
| Review app structured data / 检查 App 的 Schema | Go to each app's settings |

### 🔧 Needs a Developer or Shopify Expert / 需要开发者

| Task / 操作 | Why / 为什么 |
|---|---|
| H1 tag on collection pages hardcoded by theme / 合集页 H1 被主题硬编码 | Some themes auto-set H1 to "Products" — you can't change it in the UI. Need to edit theme Liquid. / 部分主题自动把 H1 设为 "Products"，UI 里改不了，需要改主题 Liquid |
| Canonical URLs with query strings / 带参数的 canonical URL | Shopify auto-generates canonicals but sometimes includes `?page=2` or `?variant=xxx`. Need theme-level fix. / Shopify 自动生成 canonical 但有时包含 `?page=2` 或 `?variant=xxx`，需要主题级修复 |
| JSON-LD schema customization / JSON-LD 自定义 | Shopify's auto schema is basic. Custom schema (FAQPage, advanced Product) needs Liquid or a custom app. / Shopify 自动生成的 Schema 很基础，自定义（FAQPage、高级 Product）需要 Liquid 或自定义 App |
| Lazy loading non-critical images / 非首屏图片懒加载 | Most themes handle this, but if your store is slow, need custom Liquid. / 大部分主题自带，但如果还是慢，需要自定义 Liquid |

---

## 8. More App Warnings / 更多 App 避坑

| App / Type / 类型 | Problem / 问题 | What to do / 怎么办 |
|---|---|---|
| SEO Manager App vs Yoast Shopify / SEO 管理类 App | SEO Manager overloads with features that conflict with Shopify's native SEO. Yoast Shopify is simpler but overrides manual meta edits. / SEO Manager 功能过多与原生 SEO 冲突，Yoast Shopify 简洁但会覆盖手动 meta 编辑。 | If your store is simple (<100 products), use Shopify native. If you need SEO app, test Yoast first — it's the least aggressive. / <100 个产品用原生就够。非要 App 先试 Yoast。 |
| Geolocation / Currency auto-redirect / 地理定位自动跳转 App | Googlebot crawls from US IPs — auto-redirects hide your international pages from search. / Googlebot 从美国 IP 抓取——自动跳转会隐藏你的国际页面。 | Use a country/language selector popup, never auto-redirect. / 用国家/语言选择器弹窗，不要自动跳转。 |
| Image optimization apps / 图片压缩 App | Many compress aggressively and strip alt text or rename files to gibberish. / 很多压得太狠、删 alt 文本或把文件名改成乱码。 | Compress images BEFORE uploading. TinyPNG or Squoosh (free). Skip the Shopify app. / 上传前先用 TinyPNG 或 Squoosh（免费）压缩好。别用 App。 |
| Page builders (Shogun, PageFly, GemPages) / 页面搭建器 | Add bloated HTML, break responsive layouts, create canoncial/duplicate issues. / 增加臃肿 HTML、破坏响应式、产生 canonical 冲突。 | Only use for temporary landing pages. Never for product or collection pages. / 只用在临时落地页，不要用在产品或合集页。 |

---

## 9. Quick Audit Commands / 快速审计命令

```bash
# Check meta for any page
curl -s "https://store.com/collections/dresses" | grep -E "<title>|<meta name=\"description\""

# Check Shopify sitemap
curl -s "https://store.com/sitemap.xml" | grep "<loc>" | wc -l  # count URLs

# Check robots.txt
curl -s "https://store.com/robots.txt"

# Test page speed
# Use: PageSpeed Insights API or web.dev/measure
```
