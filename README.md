# Xeni — Travel Agent Resource Hub (pSEO)

30 programmatic-SEO blog pages for [Xeni](https://www.xeni.com), the all-in-one white-label travel selling platform. Each page is a self-contained, brand-themed HTML file (navy/orange, Poppins/Inter) with real cited statistics, a data chart, an AI-generated hero image, FAQ schema, and Xeni CTAs.

**Live preview:** https://lasthumancoder.github.io/xeni-travel-guides/

## Clusters (5 × 6 = 30 guides)
1. **Become a Travel Agent by State** — FL, TX, CA, OH, PA, MI
2. **Become a Niche Travel Agent** — Disney, cruise, luxury, Carnival, corporate, Disney-from-home
3. **Niche Agent by City** — Disney/Orlando, luxury/LA, cruise/Miami, corporate/NYC, honeymoon/Dallas, group/Atlanta
4. **Career Guides** — how to become one, salary, license/certification, from home, is it worth it, home-based agency
5. **Build Your Travel Business** — host agency, booking software, commission, getting clients, white-label platform, starting an agency

## How it's built
Source markdown lives in `../Xeni_PSEO/`. Pipeline:
```
python3 make_charts.py        # chart_specs/*.json -> assets/*.svg
python3 gen_images.py         # image_prompts/*.txt -> _incoming_assets/*.jpg (kie.ai nano-banana-pro)
python3 build_html_v2.py      # blogs/*.md -> blogs-v2/*.html
python3 make_listing.py       # -> blogs-v2/index.html
```
See `../Xeni_PSEO/XENI_BLOG_PLAYBOOK.md` for voice, format, citation, and CTA rules.

Each page canonicalizes to `https://www.xeni.com/blog/<slug>` for when content moves onto the Xeni domain.
