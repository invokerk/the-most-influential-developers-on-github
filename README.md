The Most Influential Developers on Github -- Github Data Challenge 2014
=======================================================================

#Under Construction

#Warning
The result is based on limited data(2014/5/23 ~ 2014/8/23) and not on behalf of Github. The rank might be changed if the collected data increased.

#The Result
1. visionmedia
2. mattt
3. sindresorhus
4. lexrus
5. onevcat
6. 0xced
7. stormzhang
8. paulirish
9. daimajia
10. turingou
11. andrew
12. romaonthego
13. necolas
14. krzysztofzablocki
15. youxiachai
16. MatthewMueller
17. jeresig
18. neonichu
19. cheeaun
20. igrigorik
21. zenorocha
22. goshakkk
23. mreiferson
24. fengmk2
25. tommy351

#Abstract
There are many developers on github, following influential developers is highly beneficial since they spread useful repositories and others.
This survey employed the well-known PageRank algorithm, the data of watching events from the GitHub Archive and users' connections from Github API to mine the most influential developers on Github.

#Data Collection
The watching events data were collected and extracted the repository's name, actor's name and event issued time respectively. The users' connections were collected from the following relationship.
To collect the data, one can issue `python task_grab_watch_events`.

#Build Graphs
Issue `python task_gen_events_graphs`.
In this phrase, every repository's watching event is a 3-tuple(repo, actor, created_time) represented vertex of a directed graph, each vertex direct connects vertices which represent the following users of the vertex which watch the repository relatively early, in the other word, a graph represents the cascade of a repository's watching events. The whole Github's repositories' watching events can form many graphs. 

#Calculate the Influence
Issue `python task_cal_pagerank` then `python task_cal_influence`.

