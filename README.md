# notes
## Never Failing Perforce Jenkins Trigger
```
commit_process change-commit //depot/... "bash -c %quote%curl --connect-timeout 2 http://project-jenkins/job/CommitProcess/buildWithParameters?p4_changelist=%changelist% > /dev/null 2>&1 & exit 0%quote%"
```
## Python
### Print a Pretty Stack Trace
```
import sys
import traceback

current_frame = sys._getframe()

# adjust which frames should be printed
relevant_frame = current_frame.f_back.f_back

formatted_stack_lines = traceback.format_stack(relevant_frame)
formatted_stack_str = '\n'.join(formatted_stack_lines)

print(formatted_stack_str)
```
