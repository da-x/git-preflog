## git-preflog

This script tries to present ref changes of the recent 'git fetch' or
'git push' similarly to how they were represented by Git when they 
happened.

Example output:

```
Fetch from origin 15 hours ago:
 + 7fca9c06f826...04b8685acab7    jack/issue-1173 -> origin/jack/issue-1173  (forced update)
 + 665dd1dd1e1c...902fadf1d9be    jack/issue-1278 -> origin/jack/issue-1278  (forced update)
 + cf10c3202b7e...fbe66ae77ee4    jack/issue-1475 -> origin/jack/issue-1475  (forced update)

Push to origin 15 hours ago:
   dan/_patches/_issue-1248

Fetch from origin 1 hour ago:
   cb15d1cfff00..47978031233a     1.3.4 -> origin/1.3.4
   cb15d1cfff00..47978031233a     1.3.4-stable -> origin/1.3.4-stable
 + 964b95a0af48...1449cbe69d6f    da-x/_issue-1248 -> origin/da-x/_issue-1248  (forced update)
   cd2be5a60adc..d71d40a813da     master -> origin/master
 * [new branch]                   shawn/review/work -> origin/shawn/review/work
 + 1299a6453dda...51ce2cd9f67d    shawn/review/otherwork -> origin/shawn/review/otherwork  (forced update)
```

*limitation*: deleted refs are absent from the summaries, because
their corresponding reflogs were deleted.
