# node-tookit
chart and table in nodejs 

## Table Generation

The Node.js toolkit uses node canvas to generate tables on the server. The tables support custom configuration of header styles, cell styles, multi-level header grouping, cell merging, borders, background colors, alignment methods, and other functions.

### Usage

To generate a table, use the `generateTable` function. Here is an example:

```javascript
import { generateTable } from 'node-tookit';

const data = [
  ['Header 1', 'Header 2', 'Header 3'],
  ['Row 1 Col 1', 'Row 1 Col 2', 'Row 1 Col 3'],
  ['Row 2 Col 1', 'Row 2 Col 2', 'Row 2 Col 3'],
];

const config = {
  headerStyles: { font: 'bold 14px Arial', color: 'blue' },
  cellStyles: { font: '12px Arial', color: 'black' },
  multiLevelHeader: true,
  cellMerge: { rows: [1, 2], cols: [1, 2] },
  borders: { color: 'black', width: 1 },
  backgroundColors: { header: 'lightgray', cells: 'white' },
  alignment: { header: 'center', cells: 'left' },
};

const tableImage = generateTable(data, config);
```

### Configuration Options

- `headerStyles`: Object to configure the header styles (e.g., font, color).
- `cellStyles`: Object to configure the cell styles (e.g., font, color).
- `multiLevelHeader`: Boolean to enable multi-level header grouping.
- `cellMerge`: Object to configure cell merging (e.g., rows, cols).
- `borders`: Object to configure the table borders (e.g., color, width).
- `backgroundColors`: Object to configure the background colors (e.g., header, cells).
- `alignment`: Object to configure the alignment methods (e.g., header, cells).
