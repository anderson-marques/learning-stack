## learning Stack - API Modeling

### Entities:

#### 1. Learning Path

Sequence of subjects required to master some subject or target some goal owned by some entity.

#### 2. Subject

Item of learning. Can have relationships with others subjects.

### Endpoints

#### 1. Learning Path

##### 1.1 Create a new learning path:

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
    
##### 1.2. Get learning paths    
  
    GET /learning-paths/{lpid}
    
##### 1.3. Search learning paths    
  
    GET /learning-paths?[criterias]
   
##### 1.4. List learning path content
  
    GET /learning-paths/{lpid}/content
   
##### 1.5. List learning paths    
  
    GET /learning-paths
   
##### 1.6. Update learning path    
 
    PUT /learning-paths/{lpid}   
    
##### 1.7. Update learning path    
  
    PATH /learning-paths/{lpid}
    
##### 1.8. Delete a learning path   
  
    PATH /learning-paths/{lpid}
    
    
#### 2. Subject

The subjects are uniques and have no owners?


    