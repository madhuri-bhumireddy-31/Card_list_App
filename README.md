# Card List App

A React application that demonstrates:
- Virtualized list rendering using **react-window**  
- A **Scroll to Top** button with smooth scrolling  
- Component-level testing using **Jest** and **React Testing Library**

---

## Setup Instructions

1. Clone the repository:
   ```bash
   git clone MY-APP
   cd my-app
2. Install dependencies:
   ```bash
   npm install
3. Start the development server:
   ```bash
   npm start
4. Run the test suite:
   ```bash
   npm test

# Summary of Approach
The application is split into three main components:

**Card.jsx** → Renders individual card UI.

**CardList.jsx** → Uses react-window’s FixedSizeList for efficient rendering of thousands of cards (virtual scrolling).

**ScrollToTopButton.jsx** → A floating button that becomes visible when the user scrolls past 300px and scrolls smoothly back to the top.

Styling is handled in a central style.css file for responsive layout across all devices.

## Virtual Scrolling Implementation
Implemented using react-window’s FixedSizeList.
Instead of rendering all 1000+ cards in the DOM, only the visible items + a small buffer are rendered at a time.
This ensures smooth performance and avoids unnecessary re-rendering.

## Testing
Testing is done using Jest + React Testing Library.
CSS imports are mocked using identity-obj-proxy in jest.config.js.

## Tests included:
**Card Rendering**
Ensures title & description are displayed correctly.

**ScrollToTop Buttn**
Ensures button only appears after 300px scroll.
Ensures click scrolls list back to top.

**Virtualized List Rendering**
Ensures that the first few visible cards (e.g., Card 1, Card 5) are rendered into the DOM.

Run tests:
```bush
npm test
