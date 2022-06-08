---
name: Data table
category: Lists and tables
keywords:
  - DataTable
  - data
  - table
  - tabular
  - index
examples:
  - fileName: default-data-table.tsx
    title: Default data table
    description: Use to present small amounts of data for merchants to view statically.
  - fileName: sortable-data-table.tsx
    title: Sortable data table
    description: >-
      Use when clarity of the table’s content is needed. For example, to note
      the number of rows currently shown in a data table with pagination.
  - fileName: data-table-with-footer.tsx
    title: Data table with footer
    description: >-
      Use when clarity of the table’s content is needed. For example, to note
      the number of rows currently shown in a data table with pagination.
  - fileName: data-table-with-custom-totals-heading.tsx
    title: Data table with custom totals heading
    description: Use to provide a custom heading for the totals row.
  - fileName: data-table-with-totals-in-footer.tsx
    title: Data table with totals in footer
    description: >-
      Use to reposition the totals row in a more appropriate location based on
      the data stored in the

      table for merchants to better understand its meaning.
  - fileName: data-table-with-row-heading-links.tsx
    title: Data table with row heading links
    description: Use to help merchants find relevant, finer grained data sets.
  - fileName: data-table-with-all-of-its-elements.tsx
    title: Data table with all of its elements
    description: Use as a broad example that includes most props available to data table.
  - fileName: data-table-with-increased-density-and-zebra-striping.tsx
    title: Data table with increased density and zebra striping
    description: Use as a broad example that includes most props available to data table.
  - fileName: data-table-with-sticky-header-enabled.tsx
    title: Data table with sticky header enabled
    description: Use as a broad example that includes most props available to data table.
---

# Data table

Data tables are used to organize and display all information from a data set. While a data visualization represents part of data set, a data table lets merchants view details from the entire set. This helps merchants compare and analyze the data.

---

## Best practices

Data tables should:

- Show values across multiple categories and measures.
- Allow for filtering and ordering when comparison is not a priority.
- Help merchants visualize and scan many values from an entire data set.
- Help merchants find other values in the data hierarchy through use of links.
- Minimize clutter by only including values that supports the data’s purpose.
- Include a summary row to surface the column totals.
- Not include calculations within the summary row.
- Wrap instead of truncate content. This is because if row titles start with the same word, they’ll all appear the same when truncated.
- Not to be used for an actionable list of items that link to details pages. For this functionality, use the [resource list] component.

### Alignment

Column content types are built into the component props so the following alignment rules are followed:

- Numerical = Right aligned
- Textual data = Left aligned
- Align headers with their related data
- Don’t center align

---

## Content guidelines

Headers should:

- Be informative and descriptive
- Concise and scannable
- Include units of measurement symbols so they aren’t repeated throughout the columns
- Use sentence case (first word capitalized, rest lowercase)

<!-- usagelist -->

#### Do

Temperature °C

#### Don’t

Temperature

<!-- end -->

Column content should:

- Be concise and scannable
- Not include units of measurement symbols (put those symbols in the headers)
- Use sentence case (first word capitalized, rest lowercase)

### Decimals

Keep decimals consistent. For example, don’t use 3 decimals in one row and 2 in others.

---

## Related components

- To create an actionable list of related items that link to details pages, such as a list of customers, use the [resource list component](https://polaris.shopify.com/components/lists-and-tables/resource-list).

---

## Accessibility

<!-- content-for: android -->

See Material Design and development documentation about accessibility for Android:

- [Accessible design on Android](https://material.io/design/usability/accessibility.html)
- [Accessible development on Android](https://developer.android.com/guide/topics/ui/accessibility/)

<!-- /content-for -->

<!-- content-for: ios -->

See Apple’s Human Interface Guidelines and API documentation about accessibility for iOS:

- [Accessible design on iOS](https://developer.apple.com/design/human-interface-guidelines/ios/app-architecture/accessibility/)
- [Accessible development on iOS](https://developer.apple.com/accessibility/ios/)

<!-- /content-for -->

<!-- content-for: web -->

### Structure

Native HTML tables provide a large amount of structural information to screen reader users. Merchants who rely on screen readers can navigate tables and identify relationships between data cells (`<td>`) and headers (`<th>`) using keys specific to their screen reader.

Sortable tables use the `aria-sort` attribute to convey which columns are sortable (and in what direction). They also use `aria-label` on sorting buttons to convey what activating the button will do.

<!-- usageblock -->

#### Do

Use tables for tabular data.

#### Don’t

Use tables for layout. For a table-like layout that doesn’t use table HTML elements, use the [resource list component](https://polaris.shopify.com/components/lists-and-tables/resource-list).

<!-- end -->

### Keyboard support

Sorting controls for the data table component are implemented with native HTML buttons.

- Give buttons keyboard focus with the <kbd>tab</kbd> key (or <kbd>shift</kbd> + <kbd>tab</kbd> when tabbing backwards)
- Activate buttons with the <kbd>enter</kbd>/<kbd>return</kbd> and <kbd>space</kbd> keys

<!-- /content-for -->