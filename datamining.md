Dataminging

Map REDUCE model

Use typical usage pattern

Distribued File System
    Data kept in chunks - chunks server
    never same two chunks on the same server

    chunks server also serve as compute servers

Master node 
    store metadata
    know the location of chunks

Client library
    talks master
    Connecs directly to chunk server

Huge text document exemple -> task it's to analyse
    cs1 File to large
        solution: Hash tables -> index by word with a count

    cs2 word and count pairs don't fit in memory
        bash 
            ```
                words(doc.txt) | sort | uniq -c

            ```
            // Bash commands Yeeaah and parallelizable


concept map and reducer

#### Word counting
map first step 
group by key second step
reduce third step


Lecture séquentielle du disque 
randomize access are less ok

```
map(key,value)

for each word w in value:
    emit(w, 1)

```

Scheduling and data-flow 

partitionning function

Map reduce environnement

### Important!!

partionning
scheduling 
group by key
handling failures
communication

Immediate result -> stored local
Input and final output -> distribued

MASTER NODE 
= COORDINATION

Task status(idle, in progress, completed)
idle task get scheduled and workers available

Master pings worker periodically to determine the failures

Dealing with failiures
reset or reschuled

Master failure 
All is aborted / master failure is quite uncommon

### How many map and reduce jobs

Rule of thumb
M = map tasks
R= Reduce taks

    M much larger than the number of Node 

    One Distribued file system chunk per map is common
    Imporove and recover from failures

    Usually R is smaller than M 

Combiners
    Faire des préaggrégation 
    Principales songts
        Median
        Sum et 
        Average

    Exemple de mapReduce hADOOP et PIg

Analysis of large class

Challenges

    WHO TO TRUST ?
    What is the best answer ? 

Solution :
    Rank by link structure
    link analysis - pageRank



### PageRank

inlinks vs outlinks
origin of links 

See how the other page link to it

Simple recursive equation

Calcul de l'importance des noeuds

Flow model
FLow equations

Use Gaussian elimination to moderate

PageRank matrix formulation

Random Walk interpretation
It's used in order to have a moderation
Random walks = Markov PROCESSES
