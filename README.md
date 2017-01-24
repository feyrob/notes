# notes
## Never Failing Perforce Jenkins Trigger
```
commit_process change-commit //depot/... "bash -c %quote%curl --connect-timeout 2 http://project-jenkins/job/CommitProcess/buildWithParameters?p4_changelist=%changelist% > /dev/null 2>&1 & exit 0%quote%"
```
