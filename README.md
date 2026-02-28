# quiz
Name: [Jumaane Saunders]
Tools used: ChatGPT, Colab, Browser, VS Code

Q1:
- Key finding (2-4 sentences): Study hours appears more predictive of exam score than sleep hours. The scatter plot shows a strong positive correlation between study hours and exam scores, with scores consistently increasing as study time increases. In contrast, sleep hours show no clear pattern - some students with low sleep (3-4 hours) still achieved high scores (83-88) if they studied more. This suggests that study time is the dominant factor in exam performance.

- Outlier: Student L appears as an outlier - despite studying 7 hours (medium-high), they achieved 80 points while sleeping 8 hours, performing slightly below expected given their study time compared to peers with similar study hours. Most students with 7 study hours scored 78-85, making Student L's score of 80 slightly lower than the trendline prediction.

Q2:
- What was broken: The original CSS had several issues: no responsive breakpoints for mobile, navigation not stacking on mobile, hero section not stacking vertically on mobile, grid columns not changing at different breakpoints, container lacked horizontal padding, and hover effects were missing.

- What I changed: Added complete responsive breakpoints (mobile: 0-600px, tablet: 601-900px, desktop: 900px+). Fixed header to stack navigation on mobile. Made hero section stack vertically on mobile. Implemented grid with 4/2/1 columns across breakpoints. Added container padding. Added hover effects for cards and buttons with transitions. Improved overall styling and spacing.

Q3:
Prompt 1 (plan, no code):
[PASTE]
"I need to create a responsive website with specific requirements. The header needs logo left and navigation right on desktop, but stacked and centered on mobile. The hero section needs two columns on desktop (text left, card right) but stack on mobile. The grid needs 4 columns on desktop, 2 on tablet (601-900px), and 1 on mobile (0-600px). I also need hover effects for buttons and cards. Can you provide a plan for implementing this with CSS only, no frameworks?"
Response snippet:
[PASTE]
"Here's a strategic plan:
1. Use CSS media queries with breakpoints at 600px and 900px
2. For header: use flexbox with justify-content: space-between on desktop, change to flex-direction: column on mobile
3. For hero: use flexbox with row direction on desktop, column on mobile
4. For grid: use CSS Grid with grid-template-columns changing at each breakpoint
5. Add transition effects for hover states on .btn and .card
6. Set container max-width: 1000px with margin: 0 auto and padding: 0 20px"

Accepted:
- Using three breakpoints (600px and 900px thresholds)
- CSS Grid approach for responsive columns
- Flexbox for header and hero sections

Rejected:
- The suggestion to use CSS variables (kept it simple for this quiz)
- Complex animations (stuck with simple transitions to meet requirements)

Prompt 2 (debug):
[PASTE]
"My hero section is not stacking properly on mobile. Here's my CSS:
.hero {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 40px 0;
}

On mobile, I want it to stack vertically with the card below the text, but it's staying side by side. What's wrong?"
Response snippet:
[PASTE]
"The issue is that you need to add a media query to change the flex-direction. On mobile, you need:
@media (max-width: 600px) {
    .hero {
        flex-direction: column;
        text-align: center;
    }
}
This will change the direction from row (default) to column, making elements stack vertically."

What I verified:
- viewport sizes tested: 375px (iPhone SE), 600px (mobile breakpoint), 768px (iPad), 900px (tablet breakpoint), 1200px (desktop)
- what I checked visually: header alignment (logo left/nav right on desktop, stacked on mobile), hero section layout (two columns on desktop, stacked on mobile), grid columns (4 on desktop, 2 on tablet, 1 on mobile), hover effects working, no horizontal scroll, container centered with proper padding

Q4:
- Chart caption: This scatter plot shows the strong positive correlation between study hours and exam scores, with a trendline slope of 4.33 indicating that each additional hour of study is associated with approximately 4.33 more points on the exam.

- Decision based on chart: Based on this visualization, I would recommend students focus on increasing study hours to at least 7-8 hours for scores above 80, as the data shows consistent improvement with more study time, while sleep hours beyond 6-7 hours don't show the same correlation with higher scores.
