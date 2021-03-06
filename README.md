# TableLayout 
# Introduction: 

Tablelayout is a layout where it can organized it's children into rows and columns, this layout container  does not need to have borders lines  for its columns, rows, or even cells. Also Tablelayout consiste of a number of tableRow objects, this table it can have many columns and rows, in each rows it can have zero or more cells and each cell have one view object for example ImageView, or TextView. Table it can leave cells empty, but a cell can not extend a column  


# History :
This component was introduced into the Android system with a level of 1, and until now it is using the level 1. The packege of this library is by implementing the from the class object then it was exteneded by a class view. The view class is responsible for the drawing and event handeling, also it have a subclasses which is a viewGroup that will from it a other views which can be called a children and it runs a base class for other layouts, for example Linearlayout, and RelativeLayout. Moreover, a linearlayout which can display in a horizontal for a column or vertically for a single row. Then tablelayout which arrenge the childrens into a row and columns.  
# The major methods/attributes:

In the XML attributes,id this attribute used to identify as a tablelayout, and by using SetColumnShrinkable(), it will shrink in the width of the column to get it fit with table into its parent object. Also using SetColumnStretchable(), which will stretch the width of column and it will fit any extra spaces, and setColumnCollapsed() which will hide the column. However, total width of a table is defined by its parent continer, the layout_width is always will be Match_parent, but the layout_hight it can be defined as a child and if it's a TablRow then it should be using Wrap_Content, the TableRow is for builing a row. 

# Example:
In each Tablelayout it wil have a tableRow, inside the tablerow it can have a TextView,Button, or ImageView.In this example it show how you can use [TableLayout](https://github.com/rulaone/table2). Having the first example which shows, using tablelayout and having shrinkColumn (*) that mean it will shrink all the cloumns in there. Also, you can  change shrinkColumn from * to a specific column for example if it is the first column it should be (0)  which shows in the [example2](https://raw.githubusercontent.com/rulaone/TableLayout/master/eample2.PNG), or you can change it to "1"such as in [example3](https://raw.githubusercontent.com/rulaone/TableLayout/master/eample3.PNG) which will stretch the second column. An you can change it from stretch to shirnk in the size:  
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
Also you can use both of them the shrink and stretch them like in [example4](https://raw.githubusercontent.com/rulaone/TableLayout/master/eample4.PNG) :

```
<TableLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="fill_parent"
    android:layout_height="fill_parent"
    tools:context=".MainActivity"
    android:stretchColumns="1"
    android:shrinkColumns="0">
    <!-- this can stretch the second  colum which is (n-1)and shrink the third column -->

    <!--having tableRow using a wrap_content-->
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
```
By using the collapscolumn which will hide the columns like in [example5](https://github.com/rulaone/TableLayout/blob/master/eample5.PNG):
```
<TableLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="fill_parent"
    android:layout_height="fill_parent"
    tools:context=".MainActivity"
    android:stretchColumns="1"
    android:shrinkColumns="0"
    android:collapseColumns="1,2">
    <!--collapse will hide column  one and two->
```



# The reference
https://developer.android.com/reference/android/widget/TableLayout










