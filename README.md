




# Mongoose_To_CSV
- **Requirements:**
```
npm i csv-writer
```
- Code:
+ **Step 1: Import the function createObjectCsvWriter**
```
const createCsvWriter = require('csv-writer').createObjectCsvWriter;
const mongoose = require('mongoose');
```
+ **Step 2: Connect to MongoDB Atlas Server**
```
mongoose.connect('mongodb+srv://hyhung12:babykute@cluster0.ijfrnwn.mongodb.net/mongo_test', { useNewUrlParser: true });
```
+ **Step 3: Define Schema (Optional)**
```
const userSchema = new mongoose.Schema({
  name: String,
  age: String,
  level: String
});
```
+ **Step 4: Define model**
```
const User = mongoose.model('<atlas_collection>', {})
```
+ **Step 5: Function exportToCsv**
  - Data : lean<br><br>

  ```
  const data = await User.find().lean();
  ```
  - Create a **CsvWriter** object by using function **createObjectCsvWriter**<br><br>
  ```
  const csvWriter = createCsvWriter({
    path: 'users.csv',
    header: [
      { id: 'Name', title: 'Name' },
      { id: 'Age', title: 'Age'},
      { id: 'Level', title: 'Level' }
    ]   
  });
  ```
  + Write data to CSV file
 
  ```
  csvWriter.writeRecords(data);
  ```

- **Complete code**
```

```

