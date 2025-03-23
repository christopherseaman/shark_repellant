# VizTools

A collection of visualization tools for data analysis and presentation.

## Installation

```bash
pip install viztools
```

## Features

### Diverging Bar Chart

The `diverging_bar_chart` module provides functionality to create diverging bar charts, which are particularly useful for visualizing Likert scale responses or other ordinal data with a natural center point.

```python
from viztools.charts import create_diverging_bar_chart

# Example data
data = {
    "Group A": [20, 30, 10, 25, 15],  # Values for each category
    "Group B": [15, 25, 20, 20, 20]
}

# Labels from most negative to most positive
labels = ["Strongly Disagree", "Disagree", "Neutral", "Agree", "Strongly Agree"]

# Create the chart
create_diverging_bar_chart(
    data=data,
    labels=labels,
    output_path="survey_results.png",
    title="Survey Responses by Group"
)
```

#### Features:
- Supports multiple groups of data
- Automatically handles odd and even numbers of categories
- Customizable colors using any matplotlib colormap
- Proper alignment of bars around the center line
- Automatic legend generation
- Flexible output path handling

#### Parameters:
- `data`: Dictionary mapping group names to their counts/percentages
- `labels`: List of labels for each bar segment (from most negative to most positive)
- `output_path`: Where to save the output file (with or without .png extension)
- `title`: Optional title for the plot
- `x_label`: Label for the x-axis (default: "Percentage (%)")
- `y_label`: Optional label for the y-axis
- `width`: Width of the plot in inches
- `height`: Height of the plot in inches
- `zoom_factor`: Factor to scale the figure dimensions
- `color_map`: Name of the matplotlib colormap to use
- `color_range`: Tuple of (start, end) values for the colormap range

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details. 