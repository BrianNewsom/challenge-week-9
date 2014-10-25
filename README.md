# Name

write-your-name

# How many points have you earned?

0/100

(Make your own calculation and replace the number 0 with the points you think you've earned.)

# How many hours have you spent on this?

fill-in-your-answer

# When did you first start working on this week's learning challenges?

fill-in-your-answer

# What is the most difficult part about this week's challenge?

fill-in-your-answer

# Show and tell (8 points)

## Link (2 points)

[title-of-the-article](http://link-to-an-article-about-machine-learning-use-for-big-data)

## Discuss how you may apply the machine learning technique mentioned in this article to another interesting problem (6 points).

fill-in-your-answer

# D3 IV

## Checkpoints (3 points x 4 = 12 points)

# 1. (3 points)

![image](img/cp1.png?raw=true)

[checkpoint](d3/cp1.html)

# 2. (3 points)

![image](img/cp2.png?raw=true)

[checkpoint](d3/cp2.html)

# 3. (3 points)

![image](img/cp3.png?raw=true)

[checkpoint](d3/cp3.html)

# 4. (3 points)

![image](img/cp4.png?raw=true)

[checkpoint](d3/cp4.html)

## Challenges (4 points x 3 = 12 points)

# 1. (4 points)

![image](img/ch1.png?raw=true)

# 2. (4 points)

![image](img/ch2.png?raw=true)

# 3. (4 points)

![image](img/ch3.png?raw=true)

[challenge3](d3/ch3.html)



# MongoDB II

## Checkpoints (6 points x 2 = 12 points)

### 1 (6 points)

[mongodb js code collecting github events about our course](mongodb/cp1.js)

### 2 (6 points)

![terminal output of mongodb query](img/mcp2.png?raw=true)

## Challenge 1 (4 points x 10 = 40 points)

### 1 (4 points)

> db.course_events.findOne({ "actor.login" : "doubleshow" })

![screenshot](img/mch1.png?raw=true)

### 2 (4 points)

> db.course_events.findOne({"actor.login" : "doubleshow" }, {"actor": 1})

![screenshot](img/mch2.png?raw=true)

### 3 (4 points)

> db.course_events.find({ "actor.login" : {$in : ["doubleshow", "chrisbopp"]}}, {"actor.login":1, "created_at":1})

![screenshot](img/mch3.png?raw=true)

### 4 (4 points)

> db.course_events.db.course_events.findOne({'type':'PushEvent'})

![screenshot](img/mch4.png?raw=true)

### 5 (4 points)

> db.course_events.find({'type':'PushEvent'},{'payload.commits.author.name':1})

![screenshot](img/mch5.png?raw=true)

### 6 (4 points)

> db.course_events.findOne({'type' : { $in : ["IssuesEvent"]}})

![screenshot](img/mch6.png?raw=true)

### 7 (4 points)

> db.course_events.find({'type' : { $in : ["IssuesEvent"]}}, {"payload.issue.user.login" : 1})

![screenshot](img/mch7.png?raw=true)

### 8 (4 points)

> db.course_events.find({'type' : { $in : ["IssuesEvent"]}, "payload.issue.state" : "closed"}, {"payload.issue.user.login" : 1 , "payload.issue.state" : 1})

![screenshot](img/mch8.png?raw=true)

### 9 (4 points)

> db.course_events.find({'type' : { $in : ["IssuesEvent"]}, "payload.issue.state" : "open"}, {"payload.issue.user.login" : 1 , "payload.issue.state" : 1})

![screenshot](img/mch9.png?raw=true)

### 10 (4 points)

> db.course_events.find({'type' : { $in : ["IssuesEvent"]}, "payload.issue.comments" : {$gt : 0}}, {"payload.issue.user.login" : 1 , "payload.issue.comments" : 1})

![screenshot](img/mch10.png?raw=true)


## Challenge 2 (8 points x 2 = 16 points)

### 1 (8 points)

What time do individuals (no names attached) submit pull requests?

> db.course_events.find({'type' : { $in : ["PullRequestEvent"]}}, {"payload.pull_request.created_at" : 1})

![screenshot](img/mch21.png?raw=true)

### 2 (8 points)

How many events have I contributed total to the organization (of the last 300)?

> db.course_events.find( {"actor.login" : "BrianNewsom"}).count()

![screenshot](img/mch22.png?raw=true)
