# unix-bash-etc

# find

size at least 500k: find . -name '*.log' -size +500k

# exec
Gets executed for every result of parent command
find . -name '*.log' -size +500k -exec echo {} \;
* \; terminates the command
* {} placeholder of parent command result

find . -name '*.log' -size +500k -exec du -h {} \;
* du: disk utility
* -h: human readable form

# locate
locate works on a db. If new files are created run updatedb to see the results.
locate <some-file>

# history
previous 2008 commands in history
!! - executes previous command
!<history-no> - executes that command from history

# diff
diff <f1> <f2> --side-by-side --color

# ssh
copy public key to remote to login without password in future: ssh-copy-id <user>@remote
## ssh tunneling
ssh <remote> -L<my-port>:localhost:<remote-port>
* connects <my-port> to <remote-port> on <remote>
#grep
grep -v <search>
* show results without <search> in them
# cal
displays calendar

# head
get first line: head -n 1 <file>
# tail
last line: tail -n 1 <file>
tail -f <file>