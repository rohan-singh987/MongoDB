# DataBase Commands
1. View all databases  
`show dbs`

1. Create a new dtabase or switch to an old databases   
`use name_of_database`

1. View current Database  
`db`

1. Delete current Database   
`db.dropDatabase()`


# Collection Commands
1. Show Collections  
`show collections`

1. Creating a collection named 'content'   
`db.createCollection('content')`

1. Drop a collection named 'content'  
`db.content.drop()`


# Row Commands
1. Insert in a Row (**one row**)  
` db.content.insert({'Key': 'object'}) `

eg:  db.content.insert({  
    'name': 'Singh',   
    'title':'js made easy'  
    'language':'javaScript',   
})  

1. Insert in a Row (**Many row**)  
` db.content.insert([ {'Key': 'object'}, {'Key': 'object'} ]) `  

eg: db.content.insertMany([  
    {  
        'name': 'Rohan',   
        'title': 'C++ made easy',  
        'language': 'C++'  
    },  
    {  
        'name': 'Sunny',   
        'language':'Python',   
        'title':'python made easy'  
    }  
])  

3. Show all Rows in a collection  
` db.content.find() `

4. Show all Rows (**pretty**)  
` db.content.find().pretty() `


# More command operation
1. Search in database    
` db.content.find({title:'python made easy'}) `  

2. Limit number of Rows while showing output   
` db.content.find().pretty().limit(n) `  
> Here in limit(n) n can be any integer