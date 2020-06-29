# GraphQL  

## Phyrosophy  
GraphQl is new way of integration  
(now, the most prevalent way is REST)  
Both of them integrate application and web  

### query  
Query is describing the data wanted(with HTTP POST request) ---(send)---> API  
Unlike REST, all GraphQL queries are sent to the same address, and their type is POST.  

```
query FetchBlogsQuery {
  user(username: "mluukkai") {
    followedUsers {
      blogs {
        comments {
          user {
            blogs {
              title
            }
          }
        }
      }
    }
  }
}
```  
The servers response would be about the following JSON-object  
```
{
  "data": {
    "followedUsers": [
      {
        "blogs": [
          {
            "comments": [
              {
                "user": {
                  "blogs": [
                    {
                      "title": "Goto considered harmful"
                    },
                    {
                      "title": "End to End Testing with Cypress is most enjoyable"
                    },
                    {
                      "title": "Navigating your transition to GraphQL"
                    },
                    {
                      "title": "From REST to GraphQL"
                    }
                  ]
                }
              }
            ]
          }
        ]
      }
    ]
  }
}

```
### schema<heart of GraphQL>  
Describing the data sent between the client and the server.  
  ```
  type Person {
  name: String!
  phone: String
  street: String!
  city: String!
  id: ID! 
}

type Query {
  personCount: Int!
  allPersons: [Person!]!
  findPerson(name: String!): Person
}
```  
As you see, Person have five fields.  
Four of them have String(one of scalar types of GraphQL)  
*(!)must be given the value/Non-null  


