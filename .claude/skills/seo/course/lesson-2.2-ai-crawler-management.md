# 2.2 AI Crawler Management
Your technical audit includes a robots.txt analysis that shows which AI crawlers can access your site. Understanding the difference between training crawlers and search crawlers is critical for your AI visibility strategy.
Key distinction: GPTBot collects training data. OAI-SearchBot powers ChatGPT search results. ChatGPT-User is when a human asks ChatGPT to browse a URL. Blocking GPTBot does NOT block you from ChatGPT search.
Three Strategies
1. Block training, allow search (recommended for most sites):
User-agent: GPTBotDisallow: /User-agent: ClaudeBotDisallow: /User-agent: Google-ExtendedDisallow: /User-agent: OAI-SearchBotAllow: /User-agent: ChatGPT-UserAllow: /
2. Block all AI crawlers (maximum protection):
User-agent: GPTBotDisallow: /User-agent: ClaudeBotDisallow: /User-agent: PerplexityBotDisallow: /User-agent: BytespiderDisallow: /User-agent: Google-ExtendedDisallow: /User-agent: Meta-ExternalAgentDisallow: /
3. Allow all (maximum AI visibility):
# No AI-specific blocks in robots.txt
Check your robots.txt right now. Which AI crawlers are blocked? Which are allowed? Decide on your strategy: block training but allow search, block all, or allow all.
Which AI crawler strategy did you choose and why? Are you prioritizing training protection or maximum AI search visibility?
