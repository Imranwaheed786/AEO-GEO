# 2.4 JavaScript SEO
How your site renders JavaScript determines whether search engines and AI crawlers can see your content. If your content only exists after JavaScript executes, you have a visibility problem.
CSR vs SSR Detection
Client-Side Rendering (CSR): The server sends an empty HTML shell. JavaScript runs in the browser and builds the page content. Search engines see a blank page until they execute your JS.
Server-Side Rendering (SSR): The server sends fully rendered HTML. Content is visible immediately, no JS execution needed. This is what you want for SEO.
Claude detects this by analyzing the initial HTML response. If the <body> contains only a <div id="root"> or <div id="app"> with no meaningful content, it is CSR.
SPA Frameworks and Their Defaults
AI Crawlers Do NOT Execute JavaScript
This is the most important point. GPTBot, ClaudeBot, PerplexityBot, and every other AI crawler reads your raw HTML. They do not run JavaScript. If your content is CSR-only, AI crawlers see nothing. SSR is the minimum requirement for AI visibility.
Right-click your site and "View Page Source." Is your main content visible in the raw HTML, or do you see an empty div? Post the framework your site uses and whether it is CSR or SSR.
What framework does your site use, and is it CSR or SSR? If CSR, what is your plan to switch to server-side rendering?
