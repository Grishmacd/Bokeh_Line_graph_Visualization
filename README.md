# Bokeh_Line_graph_Visualization

This code creates an interactive **Bokeh** chart that shows a line trend with highlighted data points, plus an annotated reference level using a horizontal guide line and label. It demonstrates how to build a clean plot with legends and basic annotations.

---

## What the visualization shows
- A **trend line** connecting the values (line chart)
- **Data points** marked on the same graph (circle markers)
- A horizontal **reference line** at `y = 6` (dashed) to represent an average/benchmark level
- A text **label** near the reference line to explain the meaning

---

## Data Used
- X values: `[1, 2, 3, 4, 5]`
- Y values: `[4, 9, 6, 5, 10]`

---

## Plot Components (Key Points)

### 1) Figure setup
- `figure(...)` creates the plot canvas with:
  - title
  - x/y axis labels
  - width and height

### 2) Line + Points
- `p.line(...)` draws the line and adds a legend entry: **Trend Line**
- `p.circle(...)` adds point markers and adds a legend entry: **Data Points**

### 3) Annotation (Reference line)
- `Span(location=6, dimension='width', ...)` draws a **horizontal line** across the plot at `y=6`
- Added using `p.add_layout(hline)`

### 4) Label
- `Label(x=3, y=6.5, text="Average Level", ...)` places an explanatory label near the reference line
- Added using `p.add_layout(label)`

### 5) Legend placement
- `p.legend.location = "top_left"` positions the legend neatly

---

## Libraries Used
- `bokeh.plotting` → create and display the figure (`figure`, `show`)
- `bokeh.models` → add annotations (`Span`, `Label`)
- `bokeh.io.output_notebook` → display Bokeh output inside a notebook

---

## Output
- An interactive Bokeh plot with:
  - a blue line for the trend
  - red circle markers for data points
  - a dashed green reference line at `y=6`
  - a label reading **"Average Level"**
  - a legend on the top-left

## Developer
Grishma C.D
