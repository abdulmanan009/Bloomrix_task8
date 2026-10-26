# DevTools Responsive Testing Note

I tested the layout using browser DevTools Device Toolbar at the following widths:

1. **Mobile (320px & 375px):** 
   - Verified header stacks vertically (Flexbox).
   - Navigation links now wrap using `flex-wrap: wrap` preventing horizontal scrolling.
   - Course cards form a single column.
   - Footer columns stack vertically.
   
2. **Tablet (768px):**
   - Verified header switches to a horizontal row.
   - Hero switches to a 2-column flex layout.
   - Lesson area becomes a 2-column layout (main + sidebar).
   - Pricing cards switch to 2 columns.

3. **Desktop (1440px):**
   - Verified the `.container` max-width correctly caps content at 1200px.
   - Confirmed that background colors (white on courses, dark on footer) stretch the full width of the screen, while the text remains centered. 
   - Course grid uses `repeat(auto-fit, minmax(280px, 1fr))` to fit 3 cards across.

**Interactive Element Testing (3 Transforms):**
- Confirmed `.course-card` lifts up on hover (`translateY`).
- Confirmed `.btn` lifts on hover (`translateY`).
- Confirmed `.lesson-sidebar a` shifts right on hover (`translateX`).
- Tabbed through the page using the keyboard to confirm `:focus-visible` outlines appear.