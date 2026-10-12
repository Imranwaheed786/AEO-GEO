# 2.8 Sitemap Analysis
Your sitemap tells search engines which pages exist and when they changed. A broken or bloated sitemap wastes crawl budget. Claude audits your sitemap for protocol compliance, quality gates, and integration issues.
Command:
/seo sitemap https://yoursite.com
Sitemap Protocol Rules
Location Page Quality Gates
For sites with location pages (franchises, multi-location businesses), Claude applies quality gates: 
Location pages with only a city name swapped out are thin content. Google penalizes this pattern aggressively.
Sitemap Index for Large Sites
If you have more than 50,000 URLs, use a sitemap index that points to multiple sitemap files:
<sitemapindex>
  <sitemap><loc>https://site.com/sitemap-posts.xml</loc></sitemap>
  <sitemap><loc>https://site.com/sitemap-pages.xml</loc></sitemap>
  <sitemap><loc>https://site.com/sitemap-products.xml</loc></sitemap>
</sitemapindex>
Robots.txt Integration
Your sitemap location should be declared in robots.txt:
Sitemap: https://yoursite.com/sitemap.xml
Claude checks for this declaration and flags it if missing. Without it, search engines may not discover your sitemap automatically.
Run /seo sitemap on your site. Check how many URLs are listed, whether lastmod dates are accurate, and if your robots.txt references the sitemap.
How many URLs are in your sitemap? Did you find any issues like missing lastmod dates, broken URLs, or a missing robots.txt declaration? Share what you found.
