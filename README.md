# DevTools Responsive Testing Note

I tested the layout using browser DevTools Device Toolbar at the following widths:

1. **Mobile (375px):** 
   - Verified header stacks vertically (Flexbox).
   - Hero section stacks vertically.
   - Course cards form a single column using `grid-template-columns: 1fr`.
   - Footer columns stack vertically.
   
2. **Tablet (768px):**
   - Verified header switches to a horizontal row.
   - Hero switches to a 2-column flex layout.
   - Pricing cards switch to 2 columns.
   - Footer columns align horizontally.

3. **Desktop (1440px):**
   - Verified the main container maxes out at 1200px and centers on the screen.
   - Course grid uses `repeat(auto-fit, minmax(280px, 1fr))` to automatically fit 3 cards across the screen without media queries.
   - Images properly maintain a 16:9 aspect ratio using `aspect-ratio` and `object-fit: cover`.

**Interactive Element Testing:**
- Confirmed `.course-card` lifts up on hover using `transform: translateY(-5px)`.
- Confirmed `.btn` has a transform lift and background transition on hover.
- Tabbed through the page using the keyboard to confirm `:focus-visible` outlines appear on all links and buttons.