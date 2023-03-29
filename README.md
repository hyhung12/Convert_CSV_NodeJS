# Mongoose_To_CSV
- Requirements:
```
npm i csv-writer
```
- Code:
```
const createCsvWriter = require('csv-writer').createObjectCsvWriter;
const mongoose = require('mongoose');

mongoose.connect('mongodb+srv://hyhung12:babykute@cluster0.ijfrnwn.mongodb.net/mongo_test', { useNewUrlParser: true });
```
