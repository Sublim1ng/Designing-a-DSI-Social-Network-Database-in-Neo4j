# DSI Social Network Database in Neo4j

## 1. Database Design and Setup
### 4 Types of Nodes
**User:** <br>
*properties:* <br>
name: The name of the user. <br>
position: The job title or current position of the user. <br>
interests: A list of user interests in the data science field. <br>
*Rationale:*  <br>
Users are the most important part of a social network, my User node captures the basic personal information of users. <br>
<br>
**Post:** <br>
*properties:* <br>
post_id: The unique identifier of a post. <br>
topic: The topic of the post. <br>
content: The content of the post. <br>
author: The person who published the post. <br>
timestamp: The time when the post was published. <br>
likes: The number of likes the post received. <br>
*Rationale:* <br>
Users can share their opinions and thoughts by publishing posts. Those posts can be used for future communication. <br>
<br>
**Reply:** <br>
*properties:* <br>
content: The content of the reply. <br>
author: The person who published the reply. <br>
timestamp: The time when the reply was published. <br>
likes: The number of likes the reply received. <br>
*Rationale:* <br>
Each user can reply to a specific post as comments, increasing interaction between users. <br>
<br>
**Event:** <br>
*properties:* <br>
event_id: The unique identifier of an event. <br>
name: The name of the event. <br>
date: The date the event is scheduled. <br>
location: The location where the event is going to take place. <br>
description: The description of the event. <br>
attendees: The maximum capacity of the event. <br>
*Rationale:* <br>
This node gives information on future events in the data science field, which are suitable for users to participate. <br>

### 5 Types of Edges
**FRIENDS_WITH:** <BR>
Source and destination: From User to User. <br>
Rationale: This edge represents the friendship between 2 users. <br>
<br>
**PUBLISHED:** <br>
Source and destination: From User to Post. <br>
Rationale: This edge represents the relationship that a user published a post. <br> 
<br>
**WROTE** <br>
Source and destination: From User to Reply. <br>
Rationale: This edge represents the relationship that a user wrote a reply. <br>
<br>
**IN_RESPONSE_TO** <br>
Source and destination: From Reply to Post. <br>
Rationale: This edge represents the relationship that a reply is in response to a post. <br>
<br>
**WANTS_TO_ATTEND** <br>
Source and destination: From User to Event. <br>
Rationale: This edge represents the relationship that a user wants or plans to attend an event. <br>
<br>

## 2. The Potential Benefits and Challenges of the Platform











