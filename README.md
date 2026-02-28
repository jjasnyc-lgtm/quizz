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
