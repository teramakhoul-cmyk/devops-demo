summary: during 9:05 and 9:32 after logging in the user received a message "service temporarily unavailable". which happened after a deployement at 8:45.
impact: login was stopped for 30min
timeline: 8:45 deployement
          9:05 sharp increase in login errors
          9:10 support started recieving user calls 
          9:18 devops found errors
          9:25 rolling back to old version
          9:32 login service recovered
likely root cause: the new version can not support huge traffic
action items with owners: use elastic resourses
                          testing huge traffic before deployement
                          lower the alert threshold son we can detect the problem earlier
1 lesson for the next sprint: test the authentication under realistic load before deployment
                            
