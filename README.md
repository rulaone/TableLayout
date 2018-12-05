# TableLayout 
# Introduction: 

Tablelayout is a layout were it can organized it's children into rows and columns, this layout container  does not need to have borders lines  for its columns, rows, or even cells. Also Tablelayout consiste of a number of tableRow objects, this table it can have many columns and rows, in each rows it can have zero or more cells and each cell have one view object for example ImageView, or TextView. Table it can leave cells empty, but a cell can not extend a column  


# History :


# The major methods/attributes:

In the XML attributes,id this attribute used to identify as a tablelayout, and by using SetColumnShrinkable(), it will shrink in the width of the column to get it fit with table into its parent object. Also using SetColumnStretchable(), which will stretch the width of column and it will fit any extra spaces, and setColumnCollapsed() which will hide the column. However, total width of a table is defined by its parent continer, the layout_width is always will be Match_parent, but the layout_hight it can be defined as a child and if it's a TablRow then it should be using Wrap_Content, the TableRow is for builing a row. 

# Example:

Having the first example which shows, using tablelayout and having shrinkColumn (*) that mean it will shrink all the cloumns, you can  change shrinkColumn from * to a specific column for example if it is the first column it should be (0) : 

```
<TableLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="fill_parent"
    android:layout_height="fill_parent"
    tools:context=".MainActivity"
    android:shrinkColumns="*"> <!-- have all columns shrink-->

    
    <!--having tableRow using a wrap_content -->
    <TableRow
        android:layout_width= "wrap_content"
        android:layout_height= "wrap_content"
        android:padding="5dip" >

        <Button
            android:text="Item 1"
            android:id="@+id/butitem1"
            />
        <TextView
            android:text="Text 1"
            android:id="@+id/butitem2"
            />
</TableRow>

```
In each Tablelayout it have a tableRow, inside the tablerow it can have a TextView,Button, or ImageView.In this example it show how uyou can use [TableLayout](https://github.com/rulaone/TableLayout/blob/master/Tablelayout.zip). Also by writing which 

# The reference
https://developer.android.com/reference/android/widget/TableLayout



