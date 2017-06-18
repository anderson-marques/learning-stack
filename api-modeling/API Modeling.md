# learning Stack - API Modeling

## Definitions (Entities)

### 1. Learning Path - Sequence of subjects required to master some subject or target some goal.

### 2. Subject - Item of learning. Can have relationships with others subjects.

## Endpoints

### 1. Create a new learning path:

    POST /learning-paths

    {
        "name"  : "Java SE",
        "level" : "Beginner",
        "owner" : "example@mycompany.com"
        "description" : "Java Standard Edition",
        "tags" :[
            "java", "programming"
        ],
        "content": {
            { "order" : 1, "subjectId" : 1, "name" : "Programing Logic", "relevance" : 8, "path" : "/subjects/1" },
            { "order" : 1, "subjectId" : 2, "name" : "Java History", "relevance" : 3, "path" : "/subjects/2" }
        }
    }
    
    Return: learning path id (lpid)
    
### 2. Get learning paths    
  
   GET /learning-paths/1
   
### 2. List learning path content
  
   GET /learning-paths/1/content
   
   
### 3. List learning paths    
  
   GET /learning-paths