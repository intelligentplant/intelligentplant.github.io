## The IP Data Query Tab

[This
video](https://www.youtube.com/watch?v=_Q_361HDaOE&list=PLsVwx5rtV9c0duV5jln2IX9BIMDCCEWrY&index=2)
shows how to use the "IP Data Query" tab.

### Get Current Value

Clicking "Get Current Value" allows you to configure a request to get
the current value for some tags.

  - Select the relevant data source 
  - Enter a filter to search for tags available from that data source
    and click "Search"
  - Select the tag(s) you would like to query
  - Select whether you would like a header row and time stamps
  - Click "Add"

This will insert the result of the query you entered at the currently
selected point in the spreadsheet.

If the data source you want to query isn't listed it may be because it's
not authorized, it doesn't support tag read operations or you aren't
authorized to read from the data source.

### Get Historical Values

Clicking "Get Historical Values" allows you to configure a request to
get the historical values for some tags.

  - Select the relevant data source 
  - Enter a query to search for tags available from that data source
  - Select the tag(s) you would like to query
  - Enter the start, end times, interval and data funciton for the query
  - Enter the number of points (e.g. a 10 day query with interval 1h is
    240 points)
  - Select whether you would like a header row and time stamps
  - Click "Add"

This will insert the result of the query you entered at the currently
selected point in the spreadsheet.

If the data source you want to query isn't listed it may be because it's
not authorized, it doesn't support tag read operations or you aren't
authorized to read from the data source.

### Write Data

Clicking "Write Data" allows you to write a value to a tag in a data
source.

  - Select a data source from the drop down 
  - Search for the tag(s) you would like to write to
  - Enter the time stamp you would like to associate with the value. You
    can enter the time as a date, an excel formula or a relative time
    (e.g. "\*" for now or "\*-10d" for 10 days ago)
  - Enter the value you want to write to the tag, this can be any excel
    formula that produces a number
  - Click "Write"

If you don't see the data source you want to write to listed it may be
because it's not authorized, it doesn't support write operations or you
don't have permission to write to that data source.

### Write All

The write all button allows you to write multiple values to multiple
tags instantly.

In order for this to work you must setup the workbook to have certain
defined names. To setup a defined name:

1.  Open the workbook
2.  Click the "Formulas" tab
3.  Click "Define Name" in the "Defined Names" section
4.  Enter the name of the defined name
5.  Enter the value of the defined name in the "Refers to" input box
6.  Click "OK"

You can edit these names later by clicking "Name Manager" then selecting
a name and clicking "Edit"

To configure the "Write All" action created the following defined names:

  - **DataSource** - The fully qualified name of the data source that
    should be written to
  - **Tags** - The range of cells that contains the tag names you want
    to update
  - **Values** - The range of cells that contains the new values of the
    tags
  - **CurrentValues** - \[Optional\] The range of cells that contains
    queries to the effected tags (so that they can be reloaded
    autmatically)

Each value in the Values range will be written to the corresponding tag
in the Tags range. Tags whose corresponding Values cell is empty will be
ignored.

### Refresh Data

This button will reload all data query formulas in the currently opened
sheet.

### Refresh Selection

This button will reload all data query formulas in the currently
selected range.

### Wiki

This button will open the add-in wiki.

## Advanced

All text boxes can will be evaluated as a formula if they begin with "="

You can use the "Custom Tag" box to add tags that aren't listed, this is
primarily useful if you want to query Alarm Analysis Meta tags.

Deselect "Enter As Formula" if you would like the result of the query to
be added directly to the sheet. Leaving it selected generates a formula
as described in the "Using Data Query Formulas" section
