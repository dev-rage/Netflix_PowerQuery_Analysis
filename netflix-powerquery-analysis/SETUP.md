# Setup Guide

This guide will help you set up and explore the Netflix Data Analysis project.

## Prerequisites

- Microsoft Excel (2016 or later) with Power Query
- Power BI Desktop (for viewing .pbix files)
- Basic understanding of data analysis concepts

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/netflix-powerquery-analysis.git
cd netflix-powerquery-analysis
```

### 2. Explore the Data

The raw dataset is located in `data/netflix_titles.csv`. You can:
- Open it in Excel to view the raw data
- Import it into Power Query to replicate the cleaning process
- Use it as a practice dataset for your own analysis

### 3. View the Cleaned Data

Open `outputs/netflix_cleaned_and_aggregates.xlsx` to see:
- **Transformed Data** sheet: The fully cleaned dataset
- **Summary** sheet: Aggregated insights and statistics

### 4. Explore the Power BI Dashboard

1. Open `outputs/netflix_analysis.pbix` in Power BI Desktop
2. Interact with the visualizations
3. Explore different filters and slicers
4. Review the data model and relationships

### 5. Review the Documentation

- **Project Report**: `docs/project_report.docx` - Detailed documentation of the process
- **Presentation**: `presentations/project_presentation.pptx` - Visual overview of findings

## Replicating the Analysis

### Step 1: Import Data
1. Open Microsoft Excel
2. Go to Data > Get Data > From File > From Text/CSV
3. Select `data/netflix_titles.csv`
4. Click "Transform Data" to open Power Query Editor

### Step 2: Apply Transformations
Follow the steps outlined in the README.md or project_report.docx:
1. Remove empty rows
2. Change data types
3. Handle missing values
4. Split and parse columns
5. Clean text data
6. Filter and create new columns
7. Create aggregations

### Step 3: Load and Save
1. Click "Close & Load" in Power Query Editor
2. Save your Excel workbook

### Step 4: Create Visualizations (Optional)
1. Export cleaned data to Power BI
2. Create visualizations based on your insights

## Power Query Tips

- Use **Applied Steps** pane to track your transformations
- Right-click column headers for quick transformations
- Use **Group By** for aggregations
- Leverage M language for advanced transformations
- Always keep a copy of raw data

## Common Issues

### Issue: Excel doesn't have Power Query
**Solution:** Power Query is built into Excel 2016 and later. For Excel 2010/2013, install the Power Query add-in.

### Issue: Can't open .pbix file
**Solution:** Download Power BI Desktop (free) from Microsoft's website.

### Issue: Date parsing errors
**Solution:** Ensure date formats match your regional settings in Power Query.

## Contributing

If you'd like to suggest improvements or report issues:
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## Support

For questions or issues, please open an issue in the GitHub repository.

## Additional Resources

- [Power Query Documentation](https://docs.microsoft.com/en-us/power-query/)
- [Power BI Documentation](https://docs.microsoft.com/en-us/power-bi/)
- [M Language Reference](https://docs.microsoft.com/en-us/powerquery-m/)
