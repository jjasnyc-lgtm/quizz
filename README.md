# quizz
Accepted from Plan:

Mobile-First Layout: I agreed with starting the layout for mobile screens (600px or less) and using a stacked approach for both the navigation and hero section. This ensures a smooth transition to larger screens and is consistent with modern responsive design best practices.

Breakpoints at 600px, 900px, and 1200px: I liked the proposed breakpoints because they cover the most common screen sizes, ensuring that the design works well across phones, tablets, and desktops.

Rejected from Plan:

Hero Card Aligning on Desktop: The plan mentioned aligning the hero card to the right on larger screens. I rejected this idea because the card, with its large text and KPI data, would look better centered rather than pushed to the right. This also maintains a cleaner, more balanced look across all screen sizes.

Prompt 2: Debug Prompt

Bug Description:

I encountered an issue where the hero section wasn't stacking vertically on mobile (600px or less). The hero text and card were supposed to stack, but they remained side by side. This made the mobile layout look broken and uncomfortable to view.

Exact CSS Snippet I Asked About:

@media (max-width: 600px) {
  .hero {
    flex-direction: column;
    text-align: center;
  }

  .hero-text {
    max-width: 100%;
    margin-bottom: 20px;
  }

  .hero-card {
    margin-top: 20px;
  }
}

AI Response:

The AI explained that the issue was likely caused by flex-direction not being correctly applied to the .hero class. The solution was to ensure that the container (.hero) was set to display: flex with the flex-direction: column in the mobile media query. It also suggested checking that no conflicting styles were overriding these properties.

What I Changed:

After reviewing the AI's response, I realized that I missed setting the .hero container to display: flex in the mobile media query. The CSS code below fixed the issue:

@media (max-width: 600px) {
  .hero {
    display: flex; /* Added this line */
    flex-direction: column;
    text-align: center;
  }

  .hero-text {
    max-width: 100%;
    margin-bottom: 20px;
  }

  .hero-card {
    margin-top: 20px;
  }
}

This change successfully stacked the hero text and card on mobile.

Verification List

Viewport Sizes Tested:

375px (mobile phone)

600px (small mobile device)

768px (tablet)

900px (tablet landscape)

1200px (large desktop)

What I Checked Visually:

Mobile (375px): Verified that the hero section stacked vertically, and the navigation was centered. The text was centered, and the card aligned below it.

Tablet (768px): Checked that the grid switched to 2 columns and the hero section displayed correctly with the text on the left and card on the right.

Desktop (1200px): Confirmed the grid displayed 4 columns and the hero section remained properly aligned with the text on the left and card on the right.

Social Media Icons: Checked that social media icons in the footer were correctly aligned and functional across different screen sizes.

Name:Jumaane Saunders

Your Name

Tools used:

ChatGPT, Colab, Browser

Q1:

Key finding (2-4 sentences):
The plot shows a clear positive relationship between the X and Y values. As X increases, Y tends to increase in a linear fashion. This suggests that the data can be modeled using a linear regression model.

Outlier:
No outliers were identified in the plot. The data points follow a relatively smooth increasing trend without significant deviations.

Q2:

What was broken:
The hero section wasn't stacking vertically on mobile. The text and card remained side-by-side instead of stacking.

What I changed:
I added display: flex to the .hero class within the mobile media query to ensure the hero content stacks properly. Also, I ensured the flex-direction: column rule applied.

Q3:

Prompt 1 (plan, no code):
[Implement all of the following: 1. Header layout • Desktop: Logo on the left and navigation on the right. • Mobile (max-width: 600px): Navigation becomes stacked and centered. 2. Container • Max width 1000px, centered. • Add horizontal padding so content does not touch screen edges. 3. Hero section • Desktop: Two columns. • Mobile: Stacks vertically. • Hero card aligns to the right on desktop. 4. Grid section breakpoints • Desktop: 4 columns. • Tablet (601px to 900px): 2 columns. • Mobile (0px to 600px): 1 column. 5. Hover styles • Add basic hover styles for .btn and .card.]

Response snippet:
Header Layout:

[On desktop (above 600px), the header uses flex with space between the logo and navigation.

On mobile (max-width: 600px), the logo and navigation stack vertically, and the navigation links are centered.

Container:

The container has a max-width of 1000px to ensure the content doesn't stretch too wide on large screens.

Horizontal padding is added to give the content space from the edges.

Hero Section:

On desktop, the .hero section is set to use flex with the text on the left and the KPI card on the right.

On mobile, the hero text and the KPI card stack vertically, with the text centered.

Grid Section:

On desktop, the grid is set to have 4 columns using grid-template-columns: repeat(4, 1fr).

On tablet (601px to 900px), it switches to 2 columns.

On mobile (0px to 600px), it switches to 1 column.

Hover Styles:

Added hover effects to the .btn (changes background color to #ff9900) and .card (slightly raises the card with a shadow effect).]

Accepted:

Mobile-first design with stacked layout.

Breakpoints at 600px, 900px, and 1200px.

Rejected:

Aligning the hero card to the right on desktop. I rejected this because I preferred to keep the card centered for better balance and design.

Prompt 2 (debug):
[1. Prompt 1: Planning prompt (must include no code) • Ask ChatGPT for a plan to implement responsive breakpoints and hero behavior. • Then write: – Two things you accepted from the plan – One thing you rejected (and why) 2. Prompt 2: Debug prompt (must include a problem statement) • Describe one bug you hit (for example: hero not stacking, grid overflow, nav alignment). • Include the exact CSS snippet you asked about. • Paste the most important part of the AI response. • Describe what you changed afterward. 3. Verification list • List the viewport sizes you tested (for example: 375px, 768px, 1200px). • State what you checked visually]

Response snippet:
[Mobile First Approach: Start by designing the layout for mobile screens first (width of 600px or less). Use flexbox or grid to stack the navigation links vertically and ensure the hero section (text and card) are stacked.

Desktop Layout: For larger screens (above 600px), re-align the navigation links horizontally. Additionally, the hero section should use a flexbox layout with the text on the left and the KPI card on the right.

Breakpoints: Introduce breakpoints at 600px, 900px, and 1200px for tablet and desktop views.

600px: Stacked layout (both navigation and hero section).

900px: Two columns in the grid layout for tablet screens.

1200px: Four columns in the grid layout for desktop screens.

Behavior of Hero Section: Ensure the hero text is left-aligned on desktop and centered on mobile, with the KPI card aligning to the right on desktop and stacking below the text on mobile.

Testing: Test on various screen sizes using Chrome DevTools or similar tools to simulate real devices.]

What I verified:

Viewport sizes tested:
375px, 600px, 768px, 900px, 1200px.

What I checked visually:

Ensured the hero section stacked correctly on mobile (375px).

Checked the grid layout for 2 columns on tablet (768px) and 4 columns on desktop (1200px).

Verified that the social media icons and footer looked good across different screen sizes.

Q4:

Chart caption:
This chart shows the relationship between the X and Y values, where the Y values increase as X increases.

Decision based on chart:
Based on this chart, one might decide to use a linear model to predict future values of Y from X.
