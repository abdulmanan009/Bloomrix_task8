# DevTools Responsive Testing Note

I tested the layout using browser DevTools Device Toolbar at three specific widths:

1. **Mobile (375px):** 
   - Verified header stacks vertically.
   - Navigation links wrap using `flex-wrap: wrap` preventing horizontal scrolling.
   - Course cards form a single column.
   - Footer columns stack vertically.
   
2. **Tablet (768px):**
   - Header switches to a horizontal row.
   - Hero switches to a 2-column flex layout.
   - Lesson area becomes a 2-column layout with the sidebar side-by-side.
   - Pricing cards switch to 2 columns.
   - Footer columns align horizontally.

3. **Desktop (1440px):**
   - The `.container` max-width correctly caps content at 1200px, but backgrounds span full width.
   - I added a specific `@media (min-width: 1024px)` breakpoint for desktop. Here, the pricing grid changes to 3 columns and the hero section gains extra vertical padding to utilize the larger screen space.

**Interactive Element Testing (Transforms & Accessibility):**
- Confirmed `.course-card` lifts up on hover (`translateY`).
- Confirmed `.btn` links lift on hover (`translateY`).
- Confirmed `.lesson-sidebar a` shifts right on hover (`translateX`).
- Verified `:focus-within` on the card triggers the lift when navigating with the keyboard.
- Verified `prefers-reduced-motion` disables the transforms for users sensitive to motion.
- Tested the Skip Link: pressing Tab immediately shows the "Skip to main content" button.