Must Have 
Display devices
Show a table or list with device details.
Filter devices
Allow users to show all devices or only those needing patches.
Search
Search devices by name.


Ambiguous requirments: 
Sample data does not contain the timestamp
How will we seach will we use browser or 
Create an endpoint that returns device data.
Assumptions: 
Read only for patch status
Empty should not be an error
Offline devices will still be appearing 

Error handling

Handle failed requests and empty results gracefully.

Unit tests

Test filtering logic and at least one API or UI behavior.

Sample Data: 
```
[
  {
    "id": "dev-001",
    "name": "Finance-Laptop-01",
    "os": "Windows 11",
    "isOnline": true,
    "needsPatch": true
  },
  {
    "id": "dev-002",
    "name": "Web-Server-02",
    "os": "Ubuntu 24.04",
    "isOnline": true,
    "needsPatch": false
  },
  {
    "id": "dev-003",
    "name": "HR-Laptop-03",
    "os": "Windows 11",
    "isOnline": false,
    "needsPatch": true
  },
  {
    "id": "dev-004",
    "name": "Build-Server-04",
    "os": "Ubuntu 22.04",
    "isOnline": true,
    "needsPatch": true
  }
]
```

API CALL: 
get/api/devices 

Takes in: 
List 
id, name, os, isOnline, needsPatch 
Returns : 
Device : {
    id, 
    name,
    os,
    isOnline,
    needsPatch
}
Lets make the last-checked-timestamp to be optional. 
