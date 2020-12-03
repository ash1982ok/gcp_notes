# ***Sample case study: Mountkirk Games***

Mountkirk Games makes online, session-based, multiplayer games for mobile platforms. They build all of their games using some server-side integration. 
Historically, they have used cloud providers to lease physical servers.

Due to the unexpected popularity of some of their games, they have had problems scaling their global audience, application servers, MySQL databases, 
and analytics tools.

Their current model is to write game statistics to files and send them through an ETL tool that loads them into a centralized MySQL database for reporting.


### Points comes to mind when you read it

- Online session based
- Multiplayer games 
- for mobile platforms
- Server side integration
- have cloud to lease servers

- ***aced problem in scaling their***
  - global audience
  - application servers
  - MySQL db
  - Analytics tools
  
- they write game statistics to files 
- send them through an ETL tool
- that loads them into centralized mysql db for reporting


### Solution


- Compute engine with Tomcat as application server or whatever app server they use.
- To manage their multiplayer session pub/sub ??
- Firestore / cloud sql for mobile backend??
- Big Query for analytics
- Cloud ETL
