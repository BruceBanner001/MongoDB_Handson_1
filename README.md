<h3>Question1: Create a database , give it name like "Human_Resource".</h3>

use Human_Resource
switched to db Human_Resource

<h3>Question2: Create a collection inside this named "employee".</h3>

Human_Resource> db.createCollection("employee");
{ ok: 1 }

<h3>Question3:Query the collection "employee" and list all the documents.

Link:https://prepbytes-misc-images.s3.ap-south-1.amazonaws.com/assets/1640781204638-employee.json </h3>

Human_Resource> db.employee.insertMany([{
...   "firstName": "John",
...   "lastName": "Doe",
...   "salary": "25000",
...   "department": "HR",
...   "lastCompany": "X",
...   "lastSalary": "10000",
...   "overallExp": "2",
...   "contactInfo": "1234567890",
...   "yearGrad": "2016",
...   "gradStream": "CSE"
... },{
...   "firstName": "Rohan",
...   "lastName": "Jame",
...   "salary": "30000",
...   "department": "Technical",
...   "lastCompany": "Y",
...   "lastSalary": "15000",
...   "overallExp": "1",
...   "contactInfo": "1234567860",
...   "yearGrad": "2015",
...   "gradStream": "CSE"
... },{
...   "firstName": "Jame",
...   "lastName": "Doe",
...   "salary": "35000",
...   "department": "Accounts",
...   "lastCompany": "Z",
...   "lastSalary": "20000",
...   "overallExp": "1",
...   "contactInfo": "123567890",
...   "yearGrad": "2019",
...   "gradStream": "ECE"
... },{
...   "firstName": "Sao",
...   "lastName": "Avika",
...   "salary": "30000",
...   "department": "Sales",
...   "lastCompany": "Y",
...   "lastSalary": "15000",
...   "overallExp": "2",
...   "contactInfo": "1234567860",
...   "yearGrad": "2015",
...   "gradStream": "CSE"
... },{
...   "firstName": "Jame",
...   "lastName": "roh",
...   "salary": "35000",
...   "department": "Accounts",
...   "lastCompany": "Z",
...   "lastSalary": "15000",
...   "overallExp": "2",
...   "contactInfo": "123567890",
...   "yearGrad": "2019",
...   "gradStream": "EEE"
... },{
...   "firstName": "Rohan",
...   "lastName": "Jame",
...   "salary": "30000",
...   "department": "Technical",
...   "lastCompany": "Y",
...   "lastSalary": "15000",
...   "overallExp": "1",
...   "contactInfo": "1234567860",
...   "yearGrad": "2015",
...   "gradStream": "CSE"
... },{
...   "firstName": "Jame",
...   "lastName": "Doe",
...   "salary": "35000",
...   "department": "Accounts",
...   "lastCompany": "Z",
...   "lastSalary": "20000",
...   "overallExp": "1",
...   "contactInfo": "123567890",
...   "yearGrad": "2019",
...   "gradStream": "ECE"
... },{
...   "firstName": "Sao",
...   "lastName": "Avika",
...   "salary": "30000",
...   "department": "Sales",
...   "lastCompany": "Y",
...   "lastSalary": "15000",
...   "overallExp": "2",
...   "contactInfo": "1234567860",
...   "yearGrad": "2015",
...   "gradStream": "CSE"
... },{
...   "firstName": "Jame",
...   "lastName": "Doe",
...   "salary": "35000",
...   "department": "Accounts",
...   "lastCompany": "Z",
...   "lastSalary": "15000",
...   "overallExp": "2",
...   "contactInfo": "123567890",
...   "yearGrad": "2019",
...   "gradStream": "EEE"
... },{
...   "firstName": "Rohan",
...   "lastName": "Jame",
...   "salary": "30000",
...   "department": "Technical",
...   "lastCompany": "Y",
...   "lastSalary": "15000",
...   "overallExp": "1",
...   "contactInfo": "1234567860",
...   "yearGrad": "2015",
...   "gradStream": "CSE"
... },{
...   "firstName": "Jame",
...   "lastName": "Doe",
...   "salary": "35000",
...   "department": "Accounts",
...   "lastCompany": "Z",
...   "lastSalary": "20000",
...   "overallExp": "1",
...   "contactInfo": "123567890",
...   "yearGrad": "2019",
...   "gradStream": "ECE"
... },{
...   "firstName": "Sao",
...   "lastName": "Avika",
...   "salary": "30000",
...   "department": "Sales",
...   "lastCompany": "Y",
...   "lastSalary": "15000",
...   "overallExp": "2",
...   "contactInfo": "1234567860",
...   "yearGrad": "2015",
...   "gradStream": "CSE"
... },{
...   "firstName": "Jame",
...   "lastName": "Doe",
...   "salary": "35000",
...   "department": "Accounts",
...   "lastCompany": "Z",
...   "lastSalary": "15000",
...   "overallExp": "2",
...   "contactInfo": "123567890",
...   "yearGrad": "2019",
...   "gradStream": "EEE"
... }])
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId("638d97719b11474038deffb1"),
    '1': ObjectId("638d97719b11474038deffb2"),
    '2': ObjectId("638d97719b11474038deffb3"),
    '3': ObjectId("638d97719b11474038deffb4"),
    '4': ObjectId("638d97719b11474038deffb5"),
    '5': ObjectId("638d97719b11474038deffb6"),
    '6': ObjectId("638d97719b11474038deffb7"),
    '7': ObjectId("638d97719b11474038deffb8"),
    '8': ObjectId("638d97719b11474038deffb9"),
    '9': ObjectId("638d97719b11474038deffba"),
    '10': ObjectId("638d97719b11474038deffbb"),
    '11': ObjectId("638d97719b11474038deffbc"),
    '12': ObjectId("638d97719b11474038deffbd")
  }
}

Note: Below Data are present in JSON Format.

Human_Resource> db.employee.find().pretty()
[
  {
    _id: ObjectId("638d97719b11474038deffb1"),
    firstName: 'John',
    lastName: 'Doe',
    salary: '25000',
    department: 'HR',
    lastCompany: 'X',
    lastSalary: '10000',
    overallExp: '2',
    contactInfo: '1234567890',
    yearGrad: '2016',
    gradStream: 'CSE'
  },
  {
    _id: ObjectId("638d97719b11474038deffb2"),
    firstName: 'Rohan',
    lastName: 'Jame',
    salary: '30000',
    department: 'Technical',
    lastCompany: 'Y',
    lastSalary: '15000',
    overallExp: '1',
    contactInfo: '1234567860',
    yearGrad: '2015',
    gradStream: 'CSE'
  },
  {
    _id: ObjectId("638d97719b11474038deffb3"),
    firstName: 'Jame',
    lastName: 'Doe',
    salary: '35000',
    department: 'Accounts',
    lastCompany: 'Z',
    lastSalary: '20000',
    overallExp: '1',
    contactInfo: '123567890',
    yearGrad: '2019',
    gradStream: 'ECE'
  },
  {
    _id: ObjectId("638d97719b11474038deffb4"),
    firstName: 'Sao',
    lastName: 'Avika',
    salary: '30000',
    department: 'Sales',
    lastCompany: 'Y',
    lastSalary: '15000',
    overallExp: '2',
    contactInfo: '1234567860',
    yearGrad: '2015',
    gradStream: 'CSE'
  },
  {
    _id: ObjectId("638d97719b11474038deffb5"),
    firstName: 'Jame',
    lastName: 'roh',
    salary: '35000',
    department: 'Accounts',
    lastCompany: 'Z',
    lastSalary: '15000',
    overallExp: '2',
    contactInfo: '123567890',
    yearGrad: '2019',
    gradStream: 'EEE'
  },
  {
    _id: ObjectId("638d97719b11474038deffb6"),
    firstName: 'Rohan',
    lastName: 'Jame',
    salary: '30000',
    department: 'Technical',
    lastCompany: 'Y',
    lastSalary: '15000',
    overallExp: '1',
    contactInfo: '1234567860',
    yearGrad: '2015',
    gradStream: 'CSE'
  },
  {
    _id: ObjectId("638d97719b11474038deffb7"),
    firstName: 'Jame',
    lastName: 'Doe',
    salary: '35000',
    department: 'Accounts',
    lastCompany: 'Z',
    lastSalary: '20000',
    overallExp: '1',
    contactInfo: '123567890',
    yearGrad: '2019',
    gradStream: 'ECE'
  },
  {
    _id: ObjectId("638d97719b11474038deffb8"),
    firstName: 'Sao',
    lastName: 'Avika',
    salary: '30000',
    department: 'Sales',
    lastCompany: 'Y',
    lastSalary: '15000',
    overallExp: '2',
    contactInfo: '1234567860',
    yearGrad: '2015',
    gradStream: 'CSE'
  },
  {
    _id: ObjectId("638d97719b11474038deffb9"),
    firstName: 'Jame',
    lastName: 'Doe',
    salary: '35000',
    department: 'Accounts',
    lastCompany: 'Z',
    lastSalary: '15000',
    overallExp: '2',
    contactInfo: '123567890',
    yearGrad: '2019',
    gradStream: 'EEE'
  },
  {
    _id: ObjectId("638d97719b11474038deffba"),
    firstName: 'Rohan',
    lastName: 'Jame',
    salary: '30000',
    department: 'Technical',
    lastCompany: 'Y',
    lastSalary: '15000',
    overallExp: '1',
    contactInfo: '1234567860',
    yearGrad: '2015',
    gradStream: 'CSE'
  },
  {
    _id: ObjectId("638d97719b11474038deffbb"),
    firstName: 'Jame',
    lastName: 'Doe',
    salary: '35000',
    department: 'Accounts',
    lastCompany: 'Z',
    lastSalary: '20000',
    overallExp: '1',
    contactInfo: '123567890',
    yearGrad: '2019',
    gradStream: 'ECE'
  },
  {
    _id: ObjectId("638d97719b11474038deffbc"),
    firstName: 'Sao',
    lastName: 'Avika',
    salary: '30000',
    department: 'Sales',
    lastCompany: 'Y',
    lastSalary: '15000',
    overallExp: '2',
    contactInfo: '1234567860',
    yearGrad: '2015',
    gradStream: 'CSE'
  },
  {
    _id: ObjectId("638d97719b11474038deffbd"),
    firstName: 'Jame',
    lastName: 'Doe',
    salary: '35000',
    department: 'Accounts',
    lastCompany: 'Z',
    lastSalary: '15000',
    overallExp: '2',
    contactInfo: '123567890',
    yearGrad: '2019',
    gradStream: 'EEE'
  }
]

<h3>Question4:Query the collection "employee" and list the employees who are having salary more than 30000.</h3>

Human_Resource> db.employee.find({salary:{$gt: "30000"}})
[
  {
    _id: ObjectId("638d97719b11474038deffb3"),
    firstName: 'Jame',
    lastName: 'Doe',
    salary: '35000',
    department: 'Accounts',
    lastCompany: 'Z',
    lastSalary: '20000',
    overallExp: '1',
    contactInfo: '123567890',
    yearGrad: '2019',
    gradStream: 'ECE'
  },
  {
    _id: ObjectId("638d97719b11474038deffb5"),
    firstName: 'Jame',
    lastName: 'roh',
    salary: '35000',
    department: 'Accounts',
    lastCompany: 'Z',
    lastSalary: '15000',
    overallExp: '2',
    contactInfo: '123567890',
    yearGrad: '2019',
    gradStream: 'EEE'
  },
  {
    _id: ObjectId("638d97719b11474038deffb7"),
    firstName: 'Jame',
    lastName: 'Doe',
    salary: '35000',
    department: 'Accounts',
    lastCompany: 'Z',
    lastSalary: '20000',
    overallExp: '1',
    contactInfo: '123567890',
    yearGrad: '2019',
    gradStream: 'ECE'
  },
  {
    _id: ObjectId("638d97719b11474038deffb9"),
    firstName: 'Jame',
    lastName: 'Doe',
    salary: '35000',
    department: 'Accounts',
    lastCompany: 'Z',
    lastSalary: '15000',
    overallExp: '2',
    contactInfo: '123567890',
    yearGrad: '2019',
    gradStream: 'EEE'
  },
  {
    _id: ObjectId("638d97719b11474038deffbb"),
    firstName: 'Jame',
    lastName: 'Doe',
    salary: '35000',
    department: 'Accounts',
    lastCompany: 'Z',
    lastSalary: '20000',
    overallExp: '1',
    contactInfo: '123567890',
    yearGrad: '2019',
    gradStream: 'ECE'
  },
  {
    _id: ObjectId("638d97719b11474038deffbd"),
    firstName: 'Jame',
    lastName: 'Doe',
    salary: '35000',
    department: 'Accounts',
    lastCompany: 'Z',
    lastSalary: '15000',
    overallExp: '2',
    contactInfo: '123567890',
    yearGrad: '2019',
    gradStream: 'EEE'
  }
]

<h3>Question5:Query the collection "employee" and list the employees who are having experience more than 1 year.</h3>

Human_Resource> db.employee.find({overallExp:{$gt:"1"}})
[
  {
    _id: ObjectId("638d97719b11474038deffb1"),
    firstName: 'John',
    lastName: 'Doe',
    salary: '25000',
    department: 'HR',
    lastCompany: 'X',
    lastSalary: '10000',
    overallExp: '2',
    contactInfo: '1234567890',
    yearGrad: '2016',
    gradStream: 'CSE'
  },
  {
    _id: ObjectId("638d97719b11474038deffb4"),
    firstName: 'Sao',
    lastName: 'Avika',
    salary: '30000',
    department: 'Sales',
    lastCompany: 'Y',
    lastSalary: '15000',
    overallExp: '2',
    contactInfo: '1234567860',
    yearGrad: '2015',
    gradStream: 'CSE'
  },
  {
    _id: ObjectId("638d97719b11474038deffb5"),
    firstName: 'Jame',
    lastName: 'roh',
    salary: '35000',
    department: 'Accounts',
    lastCompany: 'Z',
    lastSalary: '15000',
    overallExp: '2',
    contactInfo: '123567890',
    yearGrad: '2019',
    gradStream: 'EEE'
  },
  {
    _id: ObjectId("638d97719b11474038deffb8"),
    firstName: 'Sao',
    lastName: 'Avika',
    salary: '30000',
    department: 'Sales',
    lastCompany: 'Y',
    lastSalary: '15000',
    overallExp: '2',
    contactInfo: '1234567860',
    yearGrad: '2015',
    gradStream: 'CSE'
  },
  {
    _id: ObjectId("638d97719b11474038deffb9"),
    firstName: 'Jame',
    lastName: 'Doe',
    salary: '35000',
    department: 'Accounts',
    lastCompany: 'Z',
    lastSalary: '15000',
    overallExp: '2',
    contactInfo: '123567890',
    yearGrad: '2019',
    gradStream: 'EEE'
  },
  {
    _id: ObjectId("638d97719b11474038deffbc"),
    firstName: 'Sao',
    lastName: 'Avika',
    salary: '30000',
    department: 'Sales',
    lastCompany: 'Y',
    lastSalary: '15000',
    overallExp: '2',
    contactInfo: '1234567860',
    yearGrad: '2015',
    gradStream: 'CSE'
  },
  {
    _id: ObjectId("638d97719b11474038deffbd"),
    firstName: 'Jame',
    lastName: 'Doe',
    salary: '35000',
    department: 'Accounts',
    lastCompany: 'Z',
    lastSalary: '15000',
    overallExp: '2',
    contactInfo: '123567890',
    yearGrad: '2019',
    gradStream: 'EEE'
  }
]

<h3>Question7:Query the collection "employee" and update the salary of the employee whose salary is greater than 70000 to 65000.</h3>

Human_Resource> db.employee.updateMany({salary:{$gt:"70000"}},{$set:{salary: '65000'}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 0,
  modifiedCount: 0,
  upsertedCount: 0
}

<h3>Question8:Delete all the documents from "employee" where last company is Y.</h3>

Human_Resource> db.employee.deleteMany({lastCompany: "Y"})
{ acknowledged: true, deletedCount: 6 }
