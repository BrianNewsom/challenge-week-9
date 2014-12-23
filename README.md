# Name
Dawson Botsford

# How many points have you earned?
100/100

(Make your own calculation and replace the number 0 with the points you think you've earned.)

# How many hours have you spent on this?
7

# When did you first start working on this week's learning challenges?
Saturday morning

# What is the most difficult part about this week's challenge?
Having to copy d3 code in order to get it working. There was not start instructioning for the scatter plot, we were just supposed to copy something and then add a few aspects to it.


# Show and tell (8 points)

## Link (2 points)

[Argyle Data Combating the Billion Dollar Fraud Industry With Machine Learning and Real-Time Analytics](http://www.marketwired.com/press-release/argyle-data-combating-billion-dollar-fraud-industry-with-machine-learning-real-time-1960507.htm)

## Discuss how you may apply the machine learning technique mentioned in this article to another interesting problem (6 points).
From the article: "53% of financial services organizations take up to 8 hours to detect fraud". Argyle data claims they have solved at least part of this problem by using machine learning. In just seconds they can detect and mitigate fraud. They use the Hadoop Stack.

# D3 IV

## Checkpoints (3 points x 4 = 12 points)

# 1. (3 points)

![image](http://i.imgur.com/xFWaxVX.png)

[checkpoint](checkpoint1.html)

# 2. (3 points)

![image](http://i.imgur.com/VPlfKfp.png)

[checkpoint](checkpoint2.html)

# 3. (3 points)

![image](http://i.imgur.com/Pd2vs0w.png)

[checkpoint](checkpoint3.html)

# 4. (3 points)

![image](http://i.imgur.com/dMbIopO.png)

[checkpoint](checkpoint4.html)

## Challenges (4 points x 3 = 12 points)

# 1. (4 points)

![image](http://i.imgur.com/jna8k2x.png)

# 2. (4 points)

![image](http://i.imgur.com/EKXEuy5.png)

# 3. (4 points)

![image](http://i.imgur.com/jFvuNme.png)

[challenge3](challenge3.html)



# MongoDB II

## Checkpoints (6 points x 2 = 12 points)

### 1 (6 points)

[MongoDB js code collecting Github events about our course](MongoDB-Github.js)

### 2 (6 points)

![terminal output of MongoDB query](http://i.imgur.com/Za2StDV.png)

## Challenge 1 (4 points x 10 = 40 points)

### 1 (4 points)
> db.test_insert_Github.findOne({'actor.login' : 'wannabeCitizen'},{});

![screenshot](http://i.imgur.com/pTvoEya.png)

### 2 (4 points)
> db.test_insert_Github.findOne({'actor.login' : 'wannabeCitizen'},{'actor':1}); 

![screenshot](http://i.imgur.com/QAWNErE.png)

### 3 (4 points)
>  db.test_insert_Github.find({'actor.login' : { $in : ['wannabeCitizen', 'chrisbopp']}},{'actor.login':1,'created_at':1});

![screenshot](http://i.imgur.com/H2eALuS.png)

### 4 (4 points)
> db.test_insert_Github.findOne({'type':'PushEvent'});   

![screenshot](http://i.imgur.com/k0cdlaK.png)

### 5 (4 points)
> db.test_insert_Github.find({'type':'PushEvent'}, {'payload.commits.author.name':'1'}); 

![screenshot](http://i.imgur.com/AL2blME.png)

### 6 (4 points)
> db.test_insert_Github.findOne({'type':'IssuesEvent'}, {'payload':'1'});

![screenshot](http://i.imgur.com/Mf8tl7g.png)

### 7 (4 points)
> db.test_insert_Github.find({'type':'IssuesEvent'}, {'payload.issue.user.login':'1'});

![screenshot](http://i.imgur.com/AzXXnxr.png)

### 8 (4 points)
> db.test_insert_Github.find({'type':'IssuesEvent', 'payload.action': 'closed'}, {'payload.issue.user.login':'1'});

![screenshot](http://i.imgur.com/TX9UIdZ.png)

### 9 (4 points)
> db.test_insert_Github.find({'type':'IssuesEvent', 'payload.action': 'opened'}, {'payload.issue.user.login':'1'});

![screenshot](http://i.imgur.com/OyDI4rG.png)

### 10 (4 points)
> db.test_insert_Github.find({'type':'IssuesEvent', 'payload.issue.comments':{$gt:0}}, {'payload.issue.user.login':'1', 'payload.issue.comments':1});

![screenshot](http://i.imgur.com/w4xpOhw.png)


## Challenge 2 (8 points x 2 = 16 points) 

### 1 (8 points)
Who's issue gets the most attention? (Who's issue had the most comments?)
> db.test_insert_Github.find({'type':'IssuesEvent'}, {'payload.issue.user.login':'1', 'payload.issue.comments':1}).sort({'payload.issue.comments':-1}).limit(1);

![screenshot](http://i.imgur.com/G3ddBaC.png)

### 2 (8 points)

Who forked this assignment first?
> db.test_insert_Github.find({'type':'ForkEvent','repo.name':'CSCI-4830-002-2014/challenge-week-9'},{'actor.login':1, 'created_at':1, 'repo.name':'CSCI-4830-002-2014/challenge-week-9'}).sort({'created_at':1}).limit(1).pretty;

![screenshot](http://i.imgur.com/WCcgF8u.png)
