# Problems & solutions
Problems faced &amp; Solutions Found (my experience)

1. Using SQLCMD to deploy SQL files in Linux written in Windows truncated in lot of places due

    The problem was due to CRLF in Windows and LF in Linux. 
    We solved it by setting the default line ending to CRLF in GIT as mentioned here: https://help.github.com/articles/dealing-with-line-endings/

2. Jenkins terminated the Node projects once the build was complete

    It seems there is a built in functionality in Jenkins to kill Child processes once the build is complete. 
    The solution was to set the BUILD_ID as mentioned here: https://stackoverflow.com/questions/25402350/jenkins-kill-all-child-processes

3. SVMPerf took too long to train for some records in the dataset

    Since I was not sure why, I wanted to set a timeout to training interval for every record. 
    So, I prefixed the svm training command with a timeout duration eg: `timeout 120s svm_perf_learn`
