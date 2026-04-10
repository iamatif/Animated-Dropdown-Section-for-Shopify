This is a structured README description for your GitHub Pull Request, based on the code you provided for the **Animated Dropdown Section**.

---

# Animated Dropdown Section for Shopify

## 📝 Overview
This pull request introduces a custom, highly interactive **Animated Dropdown** section. It is designed to showcase features or FAQs with a synchronized progress bar animation and dynamic image swapping. It provides a premium, "SaaS-style" feel where the content cycles automatically but allows for manual user interaction.

---

## 🚀 Key Features

### 1. Auto-Cycling Progress Tabs
The section automatically rotates through different content blocks. Each block features a vertical progress bar that fills over a set duration (5 seconds), providing a visual cue for the next transition.

### 2. Dynamic Image Swapping
As the dropdown items change (either automatically or via click), the corresponding feature image on the right side updates with a smooth cross-fade transition effect, ensuring the visual matches the active text.

### 3. Smart Interaction (Pause on Hover)
The JavaScript logic includes `mouseenter` and `mouseleave` listeners. 
- **Hovering:** Pauses the timer and the progress bar animation at its current state.
- **Leaving:** Resumes the animation from the exact point it was paused.

### 4. Fully Responsive Design
The code utilizes a dual-layout approach:
- **Desktop:** A split-screen layout (60/40) with the FAQ list and the dynamic image.
- **Mobile:** A stacked layout utilizing a slider-ready structure (Splide.js compatible) to ensure readability on smaller screens.

---

## 🛠 Technical Details

### CSS Styling
- **Dark Theme UI:** Defaulted to a sleek `#00081E` background with `#1B72EC` accent colors.
- **Smooth Transitions:** Uses `max-height` transitions for the accordion effect and `opacity` for image fading.
- **Custom Typography:** Integrated styles for 'Inter' and 'Tw Cen MT' fonts with refined letter spacing for subtitles.

### JavaScript Logic
- **State Management:** Tracks the current active index and the remaining time for the progress bar.
- **Smooth Image Swap:** Implements a `fade-out` class to prevent harsh image flickering during source changes.
- **Vanilla JS:** Written in pure JavaScript to ensure compatibility and performance without heavy library dependencies.

---

## ⚙️ Section Settings (Schema)

The section is fully customizable via the Shopify Theme Editor:

### Header Settings
- **Feature Image:** The primary image used for the mobile view.
- **Section Title/Subtitle:** Customizable text for the heading area.
- **Additional Class:** Allows developers to inject custom CSS classes for specific styling overrides.

### Block Settings (Dropdown Item)
- **Feature Image:** Specific image tied to this content block (Desktop dynamic view).
- **Title:** The clickable question/heading.
- **Description:** The expandable content area.

---

## 📦 How to Use
1. Copy the code into a new section file (e.g., `animated-dropdown.liquid`).
2. Add the section to any page via the Theme Editor.
3. Add "Dropdown" blocks and upload unique images for each block to see the dynamic swapping in action.
4. (Optional) For mobile slider functionality, ensure `Splide.js` is linked in your theme.

---

**Note:** The progress bar duration is currently hardcoded at `5000ms` (5 seconds) within the script for optimal user reading time.
