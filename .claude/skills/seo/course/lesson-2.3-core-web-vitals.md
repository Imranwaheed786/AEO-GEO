# 2.3 Core Web Vitals
Core Web Vitals are Google's page experience signals. They measure loading speed, interactivity, and visual stability. These directly affect your rankings and your users' experience.
Important: INP replaced FID (First Input Delay) in March 2024. If you see FID in old guides, ignore it.
LCP Subparts (February 2025 Update)
Google now breaks LCP into 4 subparts so you can pinpoint exactly what is slow:
What Claude Can Detect vs. What Needs Real Data
From HTML analysis: Missing width/height on images (CLS risk), render-blocking resources (LCP), heavy JS bundles (INP risk), missing lazy loading, missing fetchpriority hints.
Needs real user data (CrUX/PageSpeed): Actual LCP timing, actual INP measurements, field CLS scores. Claude flags the risks. Real monitoring confirms the numbers.
Check your Core Web Vitals using PageSpeed Insights or the technical audit. Note your LCP, INP, and CLS scores. If you fix something, post the before and after.
What are your current CWV scores? Which metric is your biggest problem, and what do you think is causing it?
