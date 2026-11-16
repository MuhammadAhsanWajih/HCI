# Usability Evaluation: HEC Pakistan Website

Heuristic evaluation of the Higher Education Commission (HEC) Pakistan website (hec.gov.pk) using Nielsen's ten usability heuristics.

| Item | Details |
|---|---|
| Course | Human-Computer Interaction, Week 1 |
| Evaluator | Muhammad Ahsan Wajih, BS Computer Science, University of Agriculture Faisalabad |
| Date | 16 November 2026 |
| Screens reviewed | Home page; R&D Research Grant Programs; HEC Announcements; Attestation of Degrees/Diplomas/Certificates |

## 1. Method

One evaluator inspected screenshots of four screens taken in desktop Chrome and judged each against Nielsen's ten heuristics. Each problem received a severity rating from 0 to 4. For colour contrast, ratios were calculated from pixel colours sampled in the screenshots using the WCAG relative-luminance formula and compared with the WCAG 2.2 minimum of 4.5:1 for normal-size text.

Scenarios used to choose the screens:

- **A:** a student wants to attest a degree (home page, then attestation page).
- **B:** a researcher wants to find a research grant (R&D page).
- **C:** a student wants the latest HEC announcements (announcements page).

| Rating | Meaning |
|:-:|---|
| 0 | Not a usability problem |
| 1 | Cosmetic problem; fix if time allows |
| 2 | Minor problem; low priority |
| 3 | Major problem; high priority to fix |
| 4 | Usability catastrophe; must fix before release |

## 2. What works well

| # | Observation | Heuristic |
|---|---|---|
| S1 | The home search box has a helpful placeholder with examples: "Search a keyword, service, scholarships etc". | H6 Recognition, H10 Help |
| S2 | Inner pages show a breadcrumb trail (R&D, Announcements, Attestation). | H1 System status |
| S3 | Listing pages offer filters with Reset Filter, a list/grid toggle, a result count ("Showing 8 out of 24 results") and pagination. | H3 Control, H7 Efficiency |
| S4 | Announcements default to "Current Announcements", with "Past Announcements" one click away. | H7 Efficiency |
| S5 | The home carousel and announcement ticker have previous/next arrows. | H3 User control |
| S6 | The attestation page has a side menu of related topics and a user manual link. | H10 Help, H6 Recognition |

## 3. Findings and fixes by screen

### Home page

![Figure 1: HEC home page, captured 16 November 2026.](../assets/screenshots/01-home.jpg)

*Figure 1: HEC home page, captured 16 November 2026.*

| # | Problem | Evidence and detail | Heuristic | Severity | Recommended fix |
|---|---|---|---|:-:|---|
| F1 | Low-contrast text on service cards | White text on the four coloured service cards has low contrast. Measured from the screenshot: 1.9:1 on yellow, 2.1:1 on lime, 2.7:1 on orange and 3.4:1 on teal. WCAG asks for 4.5:1 for normal-size text, and the small description lines are normal-size. The grey Quick Links and footer links sit directly on a photograph and also look faint (not measured, because the background varies). | H8 Aesthetic and minimalist design (legibility) | 3 - Major | Use dark text on the yellow and lime cards, or darken the card colours, so every text reaches 4.5:1. Place Quick Links on a solid dark panel instead of over the photo. |
| F2 | Unexplained acronyms in Quick Links | Quick Links use acronyms: NAHE, M&E, QAA, ACAD, HRD and ETC. A first-time visitor cannot tell what is behind them. NAHE is repeated in the main menu on inner pages. | H2 Match between system and real world | 3 - Major | Use full names or plain-language labels, with the acronym in brackets only if needed, and add a tooltip. |
| F3 | Hidden navigation on the home page | On the home page the main navigation is collapsed behind a hamburger icon at the top left, but inner pages show a full menu bar (Home, Services & Facilities, Scholarships & Funds and so on). Visitors meet two different navigation models. | H4 Consistency and standards | 2 - Minor | Show the same visible menu on the home page, or add a clearly labelled Menu button. |
| F4 | Crowded first screen | The first screen holds search, a five-card carousel with side arrows, an announcement ticker, a news banner, Quick Links, a footer-link row and a floating EDU TV button at the screen edge. "HEC Leadership Message" takes the first card, ahead of task-focused services such as Degree Attestation and Scholarships. | H8 Aesthetic and minimalist design | 2 - Minor | Lead with common student tasks (attest a degree, scholarships, equivalence), move the leadership message lower and merge the two banners. |

### R&D: Research Grant Programs

![Figure 2: HEC R&D page listing research grants. URL in screenshot: hec.gov.pk/english/services/RnD/Pages/default.aspx](../assets/screenshots/02-rnd-grants.jpg)

*Figure 2: HEC R&D page listing research grants. URL in screenshot: hec.gov.pk/english/services/RnD/Pages/default.aspx*

| # | Problem | Evidence and detail | Heuristic | Severity | Recommended fix |
|---|---|---|---|:-:|---|
| F5 | Repeated, faint grant tag | All eight visible grant cards carry the same small grey tag, "Competitive Research Grants:", which measures about 3.6:1 contrast. The filter labels also end with stray colons. The repeated tag does not help users tell the cards apart. | H8 Aesthetic and minimalist design | 1 - Cosmetic | Show a tag only when it differs, or show a deadline or status instead. Remove the trailing colons and darken tag text to at least 4.5:1. |
| F6 | Grant cards lack useful details | Each card shows only a title, the tag and an arrow. There is no summary, eligibility, deadline or open/closed status, so users must open every grant to compare them (24 results over 3 pages). | H6 Recognition rather than recall | 2 - Minor | Add a one-line summary, deadline and status to each card, and allow sorting by deadline. |
| F7 | Inconsistent section naming | The same area is named in several ways: browser tab "R & D Home", breadcrumb "R & D", heading "RESEARCH GRANT PROGRAMS", sub-heading "RESEARCH & INNOVATION WING" and main-menu entry "Initiatives & Research". A green "See Grants & Funds" button sits above a list that already shows grants, so it is unclear where it leads. | H4 Consistency and standards | 2 - Minor | Pick one name for the section and use it in the tab, breadcrumb and heading. Label the button by its destination or remove it. |
| F8 | Career Development panel mismatch | The "HEC CAREER DEVELOPMENT" panel says "Get enrolled today", but its button reads "Contact Us". The message is unrelated to research grants and the panel is dominated by decorative artwork. | H2 Match between system and real world | 2 - Minor | Make the message match the action, or replace the panel with grant help such as eligibility and deadlines. |

### HEC Announcements

![Figure 3: HEC Announcements page with banner, filter and two search boxes.](../assets/screenshots/03-announcements.jpg)

*Figure 3: HEC Announcements page with banner, filter and two search boxes.*

| # | Problem | Evidence and detail | Heuristic | Severity | Recommended fix |
|---|---|---|---|:-:|---|
| F9 | Three search tools on one page | Three separate search tools appear on one screen: the Search item in the main menu, "Search by name or tag" (filters announcements) and "Search from Google.com" with a Go button. Nothing explains how they differ, so users may search in the wrong place. | H4 Consistency and standards | 3 - Major | Keep one search with a scope selector (this page or whole site) and remove or relabel the Google box. |
| F10 | Oversized decorative banner | A large decorative banner (an illustration plus a giant faded "Announcement" watermark partly hidden behind the picture) fills roughly the top quarter of the page. Only the first two rows of cards are visible without scrolling in this screenshot. | H8 Aesthetic and minimalist design | 2 - Minor | Reduce the banner to a slim header and bring the filter and list up the page. |
| F11 | No dates on announcements | None of the four visible cards shows a publication date, and every card repeats the tag "Current Announcements", which duplicates the checked filter. Users cannot tell how recent an item is without opening it. | H1 Visibility of system status | 2 - Minor | Show the date on each card and drop the repeated tag. |

### Attestation of Degrees/Diplomas/Certificates

![Figure 4: HEC degree attestation information page.](../assets/screenshots/04-attestation.jpg)

*Figure 4: HEC degree attestation information page.*

| # | Problem | Evidence and detail | Heuristic | Severity | Recommended fix |
|---|---|---|---|:-:|---|
| F12 | Justified body text | Body text is fully justified in a narrow column, which produces uneven gaps between words (for example in "Introducing a Fully Online & Paperless Degree Attestation System" and the paragraph beginning "Applicants are advised to carefully read"). | H8 Aesthetic and minimalist design | 2 - Minor | Left-align text and limit line length. |
| F13 | Important Note hard to read and away from the form | The Important Note tells applicants to enter names, father's name, date of birth, degree titles, registration number and CGPA exactly as on their documents. It is a long red block with an underlined heading and "->>" markers. Pure red on white measures 4.0:1, below the 4.5:1 minimum for body text, and a paragraph of red text is hard to scan. On this page the warning is separate from the application form (not reviewed). | H5 Error prevention | 3 - Major | Repeat the key rules beside the relevant form fields with inline checks. On this page use a calm callout box with short bullets in dark text. |
| F14 | Breadcrumb hidden behind the header | In the captured screen the breadcrumb "Home - Services - Students - Degree Attestation" is cut off behind the fixed header, so users cannot read where they are in the site. This may depend on scroll position. | H1 Visibility of system status | 2 - Minor | Offset content for the sticky header so the breadcrumb is always visible. |
| F15 | Apply link not prominent | The most important step, applying online at www.eservices.hec.gov.pk, appears inside a paragraph and is not styled as a link. The most visible links on the page are the announcement "Introducing a Fully Online & Paperless Degree Attestation System" and the user manual. | H7 Flexibility and efficiency of use | 3 - Major | Add a prominent "Apply for attestation" button at the top of the page that opens the portal. |
| F16 | Small presentation inconsistencies | The "four steps" of the process are bulleted, not numbered; the side-menu item "AdditionalRequirement for MS/M.Phil. & PhD Degree" is missing a space; the active item "General Information" is white on grey and measures 1.8:1. | H4 Consistency and standards | 1 - Cosmetic | Use a numbered list for steps, fix the label and darken the active state so its text reaches 4.5:1. |

### Site-wide header

*Seen on Figures 2 to 4.*

| # | Problem | Evidence and detail | Heuristic | Severity | Recommended fix |
|---|---|---|---|:-:|---|
| F17 | Header labels wrap; capitalisation differs | The two-row header uses very small type. Labels wrap onto two or three lines (for example "Higher Education Statistics"), and the utility link "About Hec" is capitalised differently from "HEC" everywhere else. | H4 Consistency and standards | 1 - Cosmetic | Use consistent capitalisation and shorten or widen long labels (for example, Statistics). |

## 4. Summary

| Severity | Count | Findings |
|---|---|---|
| 3 - Major | 5 | F1, F2, F9, F13, F15 |
| 2 - Minor | 9 | F3, F4, F6, F7, F8, F10, F11, F12, F14 |
| 1 - Cosmetic | 3 | F5, F16, F17 |
| Total | 17 | |

- **Most affected heuristics:** H4 Consistency and standards and H8 Aesthetic and minimalist design (five findings each).
- **H9** (error messages) could not be assessed because no error states were captured.

### Top three priorities

1. **Make the main student tasks obvious and readable on the home page.** Fix card contrast (F1), spell out acronyms (F2) and lead with task cards (F4).
2. **Make the attestation page action-led.** Add a prominent Apply button (F15) and turn the Important Note into a clear callout with checks at the form (F13).
3. **Give listing pages one search and useful cards.** Merge the search tools (F9) and show date and deadline on cards (F6, F11).

### Effort plan

| Effort | Findings |
|---|---|
| Quick win | F1, F5, F7, F12, F14, F16, F17 |
| Medium | F2, F3, F6, F8, F10, F11, F15 |
| Larger change | F4, F9, F13 |

## 5. Limitations

- A single evaluator reviewed the site. A single evaluator finds only some of the problems; three to five evaluators is the usual recommendation.
- The review used static screenshots from one desktop browser. Hover and focus states, error messages, page speed and mobile layout were not seen.
- Contrast ratios come from sampled pixels and may vary slightly with image scaling. Text over the home-page photo was not measured.
- No users were tested. Severity ratings are the evaluator's judgement.
- The application form and the e-services portal behind the attestation page were not reviewed.
- The website may have changed since the screenshots were taken on 16 November 2026.

## 6. References

- Nielsen, J. [10 Usability Heuristics for User Interface Design](https://www.nngroup.com/articles/ten-usability-heuristics/). Nielsen Norman Group.
- Nielsen, J. [Severity Ratings for Usability Problems](https://www.nngroup.com/articles/how-to-rate-the-severity-of-usability-problems/). Nielsen Norman Group.
- W3C. [WCAG 2.2, Success Criterion 1.4.3 Contrast (Minimum)](https://www.w3.org/TR/WCAG22/#contrast-minimum).
- Higher Education Commission, Pakistan: https://hec.gov.pk/
