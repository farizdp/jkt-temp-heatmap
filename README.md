# Jakarta Weather Visualization - Complete Guide

## 📊 Generated Files

### 1. Visualizations
- **jakarta_weather_calendar_heatmap.png** - Calendar heatmap using Fahrenheit (matching reference style)
- **jakarta_weather_celsius.png** - Calendar heatmap optimized for Celsius tropical climate
- **temperature_classification_comparison.png** - Visual comparison of different temperature classification schemes

### 2. Interactive & Code
- **jakarta_weather_interactive.html** - Interactive HTML version with controls
- **create_weather_viz.py** - Python script for Fahrenheit visualization
- **create_weather_viz_celsius.py** - Python script for Celsius visualization (tropical-optimized)
- **jakarta_weather_notebook.ipynb** - Jupyter notebook with analysis

### 3. Documentation
- **temperature_classification_reference.md** - Comprehensive temperature classification guide
- **README.md** (this file)

---

## 🌡️ Temperature Classification Standards for Celsius

### Quick Reference

#### For General/Temperate Climates:
```
Below 0°C     : Freezing
0-10°C        : Cold
10-15°C       : Cool
15-20°C       : Mild/Comfortable
20-25°C       : Warm/Comfortable ⭐ (Thermal Neutral Zone)
25-30°C       : Warm
30-35°C       : Hot
Above 35°C    : Very Hot/Extreme
```

#### For Tropical Climates (like Jakarta):
```
Below 24°C    : Cool (rare)
24-26°C       : Comfortably Cool
26-28°C       : Comfortable ⭐
28-30°C       : Comfortably Warm
30-32°C       : Hot
32-35°C       : Very Hot
Above 35°C    : Extreme (rare)
```

---

## 📚 Key Research References

### 1. **World Health Organization (WHO)**
- Comfortable indoor temperature: **18-24°C** for healthy adults
- Minimum recommended: **20°C** for infants, elderly, and vulnerable individuals
- Below 16°C with high humidity: respiratory hazards

### 2. **Thermal Neutral Zone**
- Range: **20-25°C (68-77°F)**
- Definition: Temperature range where the resting human body can maintain core temperature with minimal effort
- Conditions: Little wind, moderate relative humidity

### 3. **Tropical Climate Studies**
Research from Indonesia (Jakarta context):
- **24-26°C**: Comfortably Cool
- **26-28°C**: Comfortable (preferred by locals)
- **28-30°C**: Comfortably Warm
- Studies from Indonesia show comfortable range: **24-29°C** for local residents

Similar tropical studies:
- Nigeria: 26-28°C comfortable
- India (Hyderabad): 26-32.5°C comfort band
- India (Jaipur): Neutral at 30.15°C

### 4. **Köppen Climate Classification**
- Tropical climate (A): Average temperature ≥18°C every month
- Jakarta is classified as **Af** (Tropical Rainforest)

---

## 🎨 Color Schemes for Visualization

### Recommended for Jakarta Data (Celsius):

```python
# Temperature bins optimized for tropical climate (24-35°C range)
temp_bins = [0, 24, 26, 28, 30, 32, 35, 50]

# Colors: Cool blue → Warm orange → Hot red
colors = ['#3182bd', '#6baed6', '#9ecae1', '#c6dbef', 
          '#fee0d2', '#fc9272', '#de2d26', '#a50f15']

# Labels
labels = [
    'Below 24°C (Cool)',
    '24-26°C (Comfortably Cool)', 
    '26-28°C (Comfortable)', 
    '28-30°C (Warm)', 
    '30-32°C (Hot)', 
    '32-35°C (Very Hot)', 
    'Above 35°C (Extreme)'
]
```

### Why These Ranges?
1. **Data-driven**: Jakarta's actual temperatures fall in 24-32°C range
2. **Culturally appropriate**: Matches local perception of temperature
3. **Research-based**: Aligned with Indonesian thermal comfort studies
4. **Visually effective**: Shows meaningful variations in the data

---

## 📊 Your Jakarta Data Summary

```
Data Period:     2015-01-01 to 2025-10-23
Temperature Range: 24.0°C to 31.8°C
Average Temp:    28.6°C
Climate Type:    Tropical Rainforest (Af)
```

### Key Observations:
✓ Consistently warm year-round (tropical climate)
✓ Most temperatures fall in 26-30°C range
✓ Cooler months (Jan-Feb): More blue in visualization
✓ Warmer months (Apr-Nov): More orange/red in visualization
✓ No extreme cold (<20°C) or extreme heat (>35°C) recorded

---

## 💡 Factors Affecting Temperature Comfort

Beyond air temperature, comfort is influenced by:

1. **Humidity** - Jakarta has high humidity (affects "feels like" temperature)
2. **Wind Speed** - Coastal breezes can make it feel cooler
3. **Solar Radiation** - Direct sun increases perceived temperature
4. **Acclimatization** - Locals are adapted to tropical heat
5. **Activity Level** - Physical activity generates body heat
6. **Clothing** - Insulation affects comfort

---

## 🎯 Best Practices for Temperature Visualization

### 1. **Choose Appropriate Scale**
- For global data: Use general climate scale (0-40°C)
- For tropical data: Use tropical scale (20-38°C)
- For comfort analysis: Use thermal neutral zone (15-30°C)

### 2. **Consider Your Audience**
- Local residents: Use acclimatized scale
- International viewers: Include context about local climate
- Scientific audience: Reference standards (WHO, Köppen, etc.)

### 3. **Color Selection**
- Blue shades: Cool temperatures
- Yellow/Orange: Warm temperatures
- Red shades: Hot temperatures
- Ensure colorblind-friendly palette

### 4. **Context Matters**
Always provide:
- Temperature units (°C or °F)
- Geographic location
- Climate type
- Data source
- Time period

---

## 🔧 How to Customize Your Visualization

### Change Temperature Scale:
```python
# Edit these lines in the Python script:
TEMP_BINS_C = [0, 24, 26, 28, 30, 32, 35, 50]  # Your custom ranges
LEGEND_LABELS_C = ['Your', 'Custom', 'Labels']  # Match number of bins
```

### Change Color Scheme:
```python
# Edit this line:
COLORS = ['#color1', '#color2', '#color3', ...]  # Your hex colors
```

### Change Years:
```python
START_YEAR = 2015  # Your start year
END_YEAR = 2025    # Your end year
```

### Change Temperature Type:
```python
TEMP_COLUMN = 'tavg'  # Options: 'tavg', 'tmin', 'tmax'
```

---

## 📖 Additional Resources

### Online Tools:
- Color Brewer: https://colorbrewer2.org/ (colorblind-safe palettes)
- Climate Data: https://www.meteostat.net/
- Köppen Classification: https://en.wikipedia.org/wiki/Köppen_climate_classification

### Research Papers:
- WHO Housing and Health Guidelines (1987)
- Indonesian Thermal Comfort Studies
- Köppen Climate Classification System
- Human Thermal Environment Studies

---

## ❓ Frequently Asked Questions

**Q: Why are the temperature ranges different from the reference image?**
A: The reference image uses Fahrenheit (°F). This guide provides Celsius (°C) classifications based on scientific research and tropical climate standards.

**Q: Why focus on 24-35°C for Jakarta?**
A: Jakarta's actual temperatures fall in this range. Using a wider scale (0-40°C) would compress all data into a narrow color band, losing visual detail.

**Q: What's the "Thermal Neutral Zone"?**
A: It's 20-25°C (68-77°F), where the resting human body maintains core temperature without extra effort (no shivering or sweating).

**Q: How do I know which temperature scale to use?**
A: Consider:
- Your geographic location
- Your audience's expectations
- The actual data distribution
- The purpose of visualization

**Q: Are these classifications universal?**
A: No. Temperature perception varies by:
- Climate acclimatization
- Cultural norms
- Individual physiology
- Humidity and other factors

---

## 📝 Summary

**Key Takeaways:**
1. ✓ Temperature classification is context-dependent
2. ✓ Tropical climates need different scales than temperate climates
3. ✓ Jakarta's 24-32°C range is "comfortable to warm" for tropical residents
4. ✓ WHO recommends 20-25°C as comfortable for general populations
5. ✓ Always consider humidity, wind, and acclimatization factors

**For Your Jakarta Visualization:**
Use the tropical climate scale (24-35°C) for best results, as it:
- Matches the actual data distribution
- Reflects local comfort perceptions
- Shows meaningful temperature variations
- Aligns with Indonesian research

---

Created: 2025
Data Source: Jakarta Weather Data (2015-2025)
Temperature Classifications: Based on WHO, Köppen, and tropical climate research
