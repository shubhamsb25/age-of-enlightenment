## running long running tasks in vm but session times out? No problem

use nohup -> no hangup and moving process to background and write logs to some file via redirectin

override log file
nohup ./runner1.sh > output1.log 2>&1 & 
append to log file
nohup ./runner1.sh >> output1.log 2>&1 &

### running python scripts and log not visible?

could be due to python buffering when writign to files instead of stdout
use
nohup python3 -u script.py >> output.log 2>&1 &

### find process running in background
ps aux | grep runner1.sh

### see logs of process
tail -f output1.log

### kill background process
kill -9 <pid>
