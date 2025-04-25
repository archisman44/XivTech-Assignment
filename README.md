# XivTech-Assignment
 Assignment: Real-Time Crypto Price Tracker
# Real-Time Crypto Price Tracker

A responsive React + Redux Toolkit application that tracks real-time cryptocurrency prices with simulated WebSocket updates, featuring a professional trading-themed design.

## Setup Instructions

### Option 1: Run HTML File
1. Save `abc.html` from the provided code.
2. Save the background image as `background.jpg` in the same directory (or update the URL in the `<style>` block if hosted online).
3. Open the HTML file in a modern browser (Chrome, Firefox, etc.).
4. The app will load with a trading background (coins with line graphs), a dark table, and coin logos.

### Option 2: Node.js Setup
1. **Clone the Repository**:
   ```bash
   git clone <repository-url>
   cd crypto-price-tracker
   ```
2. **Install Dependencies**:
   ```bash
   npm install
   ```
3. **Run the Application**:
   ```bash
   npm start
   ```
   The app will be available at `http://localhost:3000`.

## Tech Stack & Architecture

- **React**: Component-based UI with Tailwind CSS for styling.
- **Redux Toolkit**: Centralized state management with `createSlice` and `configureStore`.
- **Mock WebSocket**: Simulates real-time price updates using `setInterval`.
- **Tailwind CSS**: Utility-first CSS for responsive design.
- **Babel**: Transpiles JSX for browser compatibility (HTML version).

### Architecture Overview
- **State Management**: All crypto data (price, % changes, volume) is stored in a Redux slice (`cryptoSlice`). Selectors optimize component re-renders.
- **Real-Time Updates**: A `MockWebSocket` class dispatches updates every 1.5 seconds, modifying price, % changes, and volume randomly.
- **UI**: A responsive table displays 10 assets with logos, name, symbol, price, % changes (color-coded), market cap, volume, supply, and a static 7D chart (SVG polyline). The app features a trading-themed background (coins with blue/orange line graphs and numbers) and a semi-transparent dark table.
- **Components**: `CryptoTable` renders the asset table, and `App` handles WebSocket initialization and dispatching updates.

## Demo
[(http://127.0.0.1:3002/abc.html)]

## Bonus Features (Not Implemented)
- Real WebSocket integration (e.g., Binance).
- Filters/sorting for top gainers.
- localStorage support.
- Unit tests for reducers/selectors.
- TypeScript.

## Notes
- The 7D chart is a static SVG polyline, colored based on 7D % change.
- The table is responsive with `overflow-x-auto` for mobile devices.
- All state is managed in Redux; no local component state is used.
- The app features a professional trading background (coins with blue/orange line graphs and numbers) and a semi-transparent dark table with coin logos.
