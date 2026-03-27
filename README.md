# Page Replacement Algorithm Visualizer

A modern, interactive web-based visualization of Operating Systems page replacement algorithms with step-by-step memory views, live statistics, and algorithm comparisons.

## Overview

This project provides an educational tool for understanding and comparing three fundamental page replacement algorithms:
- **FIFO** (First In First Out)
- **LRU** (Least Recently Used)
- **Optimal** (MIN Algorithm)

Built with Bootstrap 5 and Chart.js for a responsive, visually appealing interface.

## Features

### 1. **Frame-by-Frame Visualization**
- Watch how each page reference changes memory frames
- Page hits and faults are color-coded:
  - 🔴 Red: Page Faults
  - 🟢 Green: Page Hits
- Clear, table-based step-by-step view of algorithm execution

### 2. **Live Analytics Dashboard**
- Real-time calculation of page faults, hits, and fault rates
- Individual KPI cards for each algorithm
- Comparative bar chart showing performance across algorithms
- Summary insight highlighting the best algorithm for the given input

### 3. **Step Sync Slider**
- Single slider to highlight the same step across all three algorithms
- Enables easy side-by-side comparison of algorithm behavior
- Smooth scrolling to highlighted rows in tables

### 4. **Interactive Simulation**
- Configurable number of memory frames (1-20)
- Custom page reference strings (space-separated values)
- Run simulations instantly with one click
- Responsive design works on desktop and mobile

## Project Structure

```
.
├── index.html          # Home/landing page
├── visualizer.html     # Main interactive simulator
├── theory.html         # Educational theory content
├── index2.html         # Secondary page
├── index3.html         # Secondary page
├── index4.html         # Secondary page
├── index5.html         # Secondary page
├── main.html           # Alternative main entry point
└── README.md           # This file
```

## Pages

### `index.html` - Home Page
- Landing page with project overview
- Feature cards highlighting key capabilities
- Navigation links to visualizer and theory
- Built by Luvkesh & Abhijeet

### `visualizer.html` - Interactive Simulator
- Main simulation interface
- Input controls for frame count and page reference string
- Three tabbed sections for FIFO, LRU, and Optimal algorithms
- Live step-sync slider for comparison
- Summary card with best algorithm recommendation
- Comparative chart visualization

### `theory.html` - Educational Content
- Theoretical background on page replacement
- Algorithm explanations and use cases
- Performance comparisons

## Technologies Used

- **HTML5** - Semantic markup
- **CSS3** - Modern styling with glassmorphism design
- **Bootstrap 5.3.3** - Responsive UI framework
- **Chart.js 4.4.0** - Data visualization
- **Vanilla JavaScript** - Algorithm implementations and interactivity

## Design System

### Color Palette
- **Primary Background**: `#020617` (Dark slate)
- **Secondary Background**: `#0f172a` (Darker blue)
- **Accent Color**: `#facc15` (Warm yellow)
- **Text Primary**: `#e5e7eb` (Light gray)
- **Text Muted**: `#9ca3af` (Medium gray)
- **Danger**: `#dc2626` (Red for faults)
- **Success**: `#16a34a` (Green for hits)

### Visual Effects
- Glassmorphism cards with backdrop blur
- Gradient backgrounds (blue & green radial gradients)
- Smooth transitions and hover effects
- Professional typography with Inter font family

## How to Use

### Running the Simulator

1. Open `visualizer.html` in a web browser
2. Adjust the **Number of Frames** (1-20)
3. Enter a **Page Reference String** (space-separated numbers)
4. Click **Run Simulation**
5. Explore results:
   - View detailed step tables for each algorithm
   - Compare fault counts in the chart
   - Use the step slider to sync views across algorithms
   - Read the summary insight for recommendations

### Example Input
```
Number of Frames: 3
Page Reference String: 7 0 1 2 0 3 0 4 2 3 0 3 2
```

## Algorithm Explanations

### FIFO (First In First Out)
- Removes the page that entered memory first
- Simplest to implement
- Does not consider page usage patterns
- Can experience Bélády's anomaly

### LRU (Least Recently Used)
- Removes the page not used for the longest time
- Balances performance and implementation complexity
- More efficient than FIFO in most cases
- Requires tracking page access times

### Optimal (MIN)
- Removes the page whose next use is farthest in the future
- Theoretical lower bound for page faults
- Not practical in real systems (requires future knowledge)
- Serves as benchmark for other algorithms

## Algorithm Performance

Performance varies based on:
- **Number of frames** available
- **Page reference pattern**
- **Locality of reference** in the workload

The visualizer helps demonstrate how different algorithms perform under various conditions.

## Browser Compatibility

- Chrome/Chromium 90+
- Firefox 88+
- Safari 14+
- Edge 90+

## Development Notes

### Algorithm Implementations
All algorithms are implemented in vanilla JavaScript:
- `simulateFIFO()` - FIFO algorithm
- `simulateLRU()` - LRU algorithm with last-used tracking
- `simulateOptimal()` - Optimal algorithm with future scanning

### Table Rendering
- Dynamic table generation based on frame count
- Data attributes (`data-step`) for step identification
- CSS classes for fault highlighting

### Chart Management
- Chart.js instance management with proper cleanup
- Responsive configuration for different screen sizes
- Custom color schemes matching the design system

## Credits

**Created by:**
- Luvkesh Rawat
- Abhijeet

**For:** Operating Systems Lab - Semester Project

## Future Enhancements

Potential improvements:
- [ ] Additional algorithms (Clock, Second Chance)
- [ ] Algorithm complexity analysis
- [ ] Performance metrics table
- [ ] Downloadable results/reports
- [ ] Custom algorithm implementation interface
- [ ] Preset benchmark scenarios
- [ ] Multilingual supportw

## License

Educational project for OS Lab coursework.

---

**Last Updated:** December 2025
