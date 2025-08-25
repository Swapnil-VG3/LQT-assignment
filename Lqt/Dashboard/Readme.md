# Sustainability Dashboard for Textile Manufacturing

An AI-powered sustainability monitoring dashboard designed specifically for the Head of Sustainability at textile manufacturing companies to track energy, water, waste, and emissions metrics in real-time



##  Overview

This dashboard provides a platform for monitoring key sustainability KPIs, identifying operational hotspots, ensuring regulatory compliance, and making data-driven decisions to optimize resource utilization while reducing environmental impact

### Target User
**Head of Sustainability** - Responsible for overseeing and optimizing the company's resource usage and ensuring that the sustainability goals are met, regulatory compliance is maintained, and delivering clear performance reports to stakeholders

##  Features

### Must-Have Features 

#### 1. **Smart Filters & Defaults**
- Time range filtering (Today, Week, Month, Quarter, Year)
- Unit, department, machine, and shift filters
- Persistent filter state across sessions


#### 2. **Interactive KPI Tiles**
- **Energy Consumption** monitoring with real-time values
- **Water Usage** tracking with target comparisons
- **Waste Generation** metrics with trend analysis
- **CO2 Emissions** monitoring with compliance indicators
- **Overall Performance** radar chart with comprehensive metrics

#### 3. **Click-to-Explore Navigation**
- Click any KPI tile for detailed insights
- Dedicated insights pages for each metric
- Overall performance drill-down capabilities


#### 4. **Critical Alerts System**
- Real-time alert notifications with bell icon
- Color-coded alerts by severity (Critical, Warning, Info)
- Automatic alert count badges


#### 5. **Dynamic Visualizations**
- Line graphs for trend analysis
- Bar charts for department comparisons
- Radar charts for overall performance
- Progress bars for goal tracking
- Heatmaps for hotspot identification

#### 6. **Goal Progress Tracker**
- Real-time progress monitoring
- Target vs. actual comparisons
- Status indicators (On Track, Over Target, Behind Schedule)
- Visual progress bars with color coding

#### 7. **Export & Reporting**
- **PDF Export**: Presentation-ready reports
- **CSV Export**: Raw data for analysis
- **Excel Export**: Structured data with formatting
- Customizable date ranges and branding options
  

### Good-to-Have Features 

#### 1. **Sticky Notes & Comments**
- Add contextual notes to specific metrics
- Timestamped comments for historical context
- Team collaboration through shared notes


#### 2. **Event Overlay on Graphs**
- Operational events marked on trend charts
- Cause-and-effect relationship visualization
- Historical event tracking

#### 3. **Advanced Comparison Views**
- Side-by-side department comparisons
- Time period comparative analysis
- Multi-dimensional data visualization


## 🛠 Technology Stack

### Frontend
- **React 18+** - Modern component-based architecture
- **Tailwind CSS** - Utility-first styling framework
- **Recharts** - Responsive chart library
- **Lucide React** - Modern icon system

### Data Visualization
- **Line Charts** - Trend analysis over time
- **Bar Charts** - Department and unit comparisons
- **Radar Charts** - Overall performance metrics
- **Progress Bars** - Goal tracking and KPI progress
- **Responsive Design** - Works on desktop and mobile

### Key Libraries
```json
{
  "react": "^18.0.0",
  "recharts": "^2.8.0",
  "lucide-react": "^0.263.1",
  "tailwindcss": "^3.3.0"
}
```

##  Installation & Setup

### Prerequisites
- Node.js 16+ installed
- npm or yarn package manager
- Modern web browser

### Quick Start

1. **Clone or Download the Project**
   ```bash
   mkdir sustainability-dashboard
   cd sustainability-dashboard
   ```

2. **Initialize React Project**
   ```bash
   npx create-react-app .
   ```

3. **Install Dependencies**
   ```bash
   npm install recharts lucide-react
   ```

4. **Replace App.js**
   - Copy the dashboard code into `src/App.js`
   - Update export: `export default SustainabilityDashboard;`

5. **Add Tailwind CSS**
   Add to `public/index.html` in `<head>`:
   ```html
   <script src="https://cdn.tailwindcss.com"></script>
   ```

6. **Start Development Server**
   ```bash
   npm start
   ```

7. **Access Dashboard**
   Open `http://localhost:3000` in your browser

### Alternative Setup with Vite (Faster)

```bash
npm create vite@latest sustainability-dashboard -- --template react
cd sustainability-dashboard
npm install recharts lucide-react
npm run dev
```

## 📊 Sample Data

The dashboard comes with realistic mock data including:

### KPI Metrics
- **Energy**: 1,500 kWh (Target: 2,000 kWh)
- **Water**: 10,500 L (Target: 11,000 L) 
- **Waste**: 25 kg (Target: 50 kg)
- **Emissions**: 190 kg CO2 (Target: 200 kg CO2)

### Department Data
- Spinning, Weaving, Dyeing, Finishing departments
- Historical trend data for 5-day period
- Comparative metrics across all departments

### Alert Examples
- Critical: Water usage exceeded 120% in Unit A
- Warning: Energy consumption 15% above average
- Info: Weekly waste reduction goal achieved


## 📈 Success Metrics

The dashboard tracks these key performance indicators:

### Operational Efficiency
- **Reporting Time Reduction**: 60% faster report generation
- **Alert Response Time**: <2 hours (down from 1 day)
- **Resource Efficiency**: 15%+ reduction in waste

### Compliance & Governance
- **Audit Readiness**: 100% compliance tracking
- **Data Accuracy**: Single source of truth
- **Stakeholder Transparency**: Real-time visibility

### User Experience
- **Data Accessibility**: Centralized, user-friendly interface
- **Manual Effort Reduction**: Automated data collection
- **Goal Achievement**: Higher target completion rates


##  Troubleshooting

### Common Issues

1. **Charts Not Displaying**
   ```bash
   npm install recharts --save
   npm start
   ```

2. **Styling Issues**
   - Ensure Tailwind CDN is loaded in `index.html`
   - Check browser console for CSS errors

3. **Performance Issues**
   - Reduce chart data points for large datasets
   - Implement data pagination for historical data

4. **Mobile Responsiveness**
   - Dashboard is mobile-optimized
   - Use horizontal scrolling for wide charts

### Error Solutions

**Module Not Found:**
```bash
rm -rf node_modules package-lock.json
npm install
```

**Port Already in Use:**
```bash
npm start -- --port 3001
```

**Build Errors:**
```bash
npm run build
# Check console output for specific errors
```

##  Browser Support

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+
- Mobile browsers (iOS Safari, Chrome Mobile)


