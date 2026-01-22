# YouTube Web Crawling & Word Cloud Analysis — Seattle Public Safety Narratives

## Topic & Search Parameters (5 pts)
This mini-study explores how different search terms shape the YouTube video results and the language used in video snippets related to public safety issues in Seattle.

**Search terms**
- "seattle crime" (78 videos)
- "seattle safety" (79 videos)
- "seattle homeless" (77 videos)

**Data fields collected**
video_url, user_url, username, title, view_num, created_at, shortdesc, collected_at

**Method**
Used Selenium + BeautifulSoup to crawl YouTube search results pages, scrolled 5 times per query, extracted the latest ~20 videos per scroll, deduplicated by video_url, and saved results as CSV.

## Why This Comparison (5 pts)
I chose these three terms because they refer to overlapping urban issues but carry different framing:
- “crime” often implies incidents and enforcement.
- “safety” often implies prevention, advice, and policy.
- “homeless” often implies social services, encampments, and governance.
Comparing them helps reveal how framing affects what content becomes visible and what language dominates.

## Word Clouds & Comparison (5 pts)
### Seattle Crime — Key patterns
The crime word cloud is dominated by incident-oriented terms (e.g., **violent**, **shooting**, **arrest**, **robbery**, **suspect**), suggesting a focus on discrete events, policing, and breaking-news style coverage.

### Seattle Homeless — Key patterns
The homeless word cloud emphasizes governance and city response (e.g., **camp**, **encampment**, **mayor**, **crisis**, **removal**, **residents**), pointing to discussions of policy, public debate, and the management of encampments.

### Seattle Safety — Key patterns
The safety word cloud includes terms related to institutions and local context (e.g., **school**, **police**, **downtown**, **mayor**, **harrell**, **community**), which feels more like civic discussion, neighborhood concerns, and “how to stay safe” framing.

**Similarity**
All three word clouds contain location cues like **Seattle**, **downtown**, and references to local actors (police/mayor), showing that local governance and place identity are recurring anchors.

**Difference**
“Crime” leans toward incident + enforcement language; “homeless” leans toward encampment + policy language; “safety” sits between them with more prevention/community framing.

## Possible Reasons for Observed Patterns (5 pts)
1. **Algorithm & channel composition**: Different keywords may surface different types of channels (local news vs commentary vs civic discussion).
2. **Keyword framing effect**: “crime” selects for incident-driven titles/snippets; “homeless” selects for policy and encampment debates.
3. **News-driven metadata**: Snippets often mirror headlines, which can amplify sensational or conflict-heavy terms.

## How This Research Could Be Improved (5 pts)
- Increase sample size (more scrolls, more days/time windows).
- Add more neutral control terms (e.g., “living in seattle”) to compare baseline language.
- Clean text more systematically (remove generic words like “new”, “video”, “subscribe”).
- Use NLP (TF-IDF, topic modeling) instead of only word clouds.
- Compare across locations (Seattle vs Tacoma vs Olympia) and add location fields.

## What Stood Out / Different from Expectations (5 pts)
[Write 3–5 sentences: e.g., I expected “safety” to be mostly advice, but it also surfaced political names like Harrell; or “homeless” returned many governance-related words rather than human-story language.]

## Word Clouds (5 pts)
### Seattle Crime
![Seattle Crime Word Cloud](img/wordcloud-seattle-crime.png)

### Seattle Safety
![Seattle Safety Word Cloud](img/wordcloud-seattle-safety.png)

### Seattle Homeless
![Seattle Homeless Word Cloud](img/wordcloud-seattle-homeless.png)

## Download CSV Files (5 pts)
- Seattle Crime: https://raw.githubusercontent.com/<YOUR_GITHUB_USERNAME>/<YOUR_REPO>/main/assets/seattle-crime.csv
- Seattle Safety: https://raw.githubusercontent.com/<YOUR_GITHUB_USERNAME>/<YOUR_REPO>/main/assets/seattle-safety.csv
- Seattle Homeless: https://raw.githubusercontent.com/<YOUR_GITHUB_USERNAME>/<YOUR_REPO>/main/assets/seattle-homeless.csv
