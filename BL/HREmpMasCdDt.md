# Excel Data Uploading Confing

### object types
1. Excel File
2. Excel Sheet
3. Excel Column

### Define Excel

1. Create Excel with excel type **ExcelFile**
2. **OurCode** is used to identify exact excel sheet in sp.

### Define Sheets
1. **Object Caption** should be excel's sheet name
2. **Default Path** should be table's name

### columns Defining 

#### Update one table from one sheet

1. **Default Path** Should be table's column
2. **Object Caption** should be excel's column
3. if we going to insert column that not taken from user but should be there then **is visible** should be off and default value should be provided

#### Update multiple tables from one sheet

1. Basic configuations are same way.
2. But here you have to define **MapName** as table name
3. **Map Id** should be anything but it uses for group items for same table
4. when you enable isMust for some columns then it's insert to other tables without considering anything. 
5. **Tip :** when you enable isMust with MapId by selecting from map Id's then it become available for all MapId enabled tables but it's not enabled for default table