## disk usage and mounts
df -h

## cpu count 
lscpu | grep "^CPU(s):" | awk '{print $2}'
