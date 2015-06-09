# `sshb` - an ssh batch command

i use this far too often not to have it saved here.  

pop hosts into a file called `hostfile` or similar.

set up ssh-agent (presuming your ssh keys are already set up)

    eval $(ssh-agent)
    ssh-add

    for i in $(cat hostlist) ; do
      ./sshb $i 'echo "hello world!"'

remember escapes, quoting, variable interpolation, et al.
