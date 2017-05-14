# UTS namespace
    1 uts.c: demonstrate the use of UTS namespaces
    2 ns_exec.c: join a namespace using setns() and execute a command
    3 unshare.c: unshare namespaces and execute a command; similar in concept
to unshare(1)
# PID namespaces
    1 pidns_init_sleep.c: demonstrate PID namespaces
    2 multi_pidns.c: create a series of child processes in nested PID
    namespaces
# more on PID namespaces
    1 ns_child_exec.c: create a child process that executes a shell
    command in new namespace(s)
    2 simple_init.c: a simple init(1)-style program to be used as the init
    program in a PID namespace
    3 orphan.c: demonstrate that a child becomes orphaned and is adopted
    by the init process when its parent exits
    4 ns_run.c: join one or more namespaces using setns() and execute a
    command in those namespaces, possibly inside a child process;
    similar in concept to nsenter(1)
# user namespaces
    1 demo_userns.c: simple program to create a user namespace and display
    process credentials and capabilities
    2 userns_child_exec.c: create a child process that executes a shell
    command in new namespace(s); similar to ns_child_exec.c, but with
    additional options for use with user namespaces
    3 userns_setns_test.c: test the operation of setns() from two
    different user namespaces.
# network namespaces
# Mount namespaces and shared subtrees

# how to run    
./uts test
./ns_exec /proc/2937/ns/uts hostname
