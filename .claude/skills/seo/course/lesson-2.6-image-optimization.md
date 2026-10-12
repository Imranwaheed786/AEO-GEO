# 2.6 Image Optimization
Images are often the heaviest elements on a page. Unoptimized images slow your LCP, cause layout shifts, and hurt accessibility. Claude audits every image on the page in one command.
Command:
/seo images https://yoursite.com/page
File Size Targets
Format Priority
WebP is the safe default. AVIF gives better compression if you can handle the encoding time. Use <picture> with AVIF as first source and WebP as fallback for optimal delivery.
What Claude Checks
Alt text: Missing alt attributes hurt accessibility and image search visibility
Width and height: Missing dimensions cause CLS (layout shift) as images load
Lazy loading: Below-the-fold images should have loading="lazy"
Fetchpriority: Your LCP image should have fetchpriority="high"
Format: Still using PNG or JPEG when WebP would cut size by 30-50%
CLS prevention tip: Always set explicit width and height attributes on every image. The browser reserves space before the image loads, preventing layout shifts.
Run /seo images on your homepage. Count how many images are missing alt text, missing dimensions, or using unoptimized formats.
How many images on your homepage are missing alt text? What image format are you currently using, and are you considering switching to WebP or AVIF?
