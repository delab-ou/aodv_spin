# aodv_spin

Development Environment<br>
MacOS Mojave 10.14.4<br>
SPIN 6.4.9<br>
Python 3.7.3<br>
gcc 4.2.1<br>

Execution<br>
0:<br>
put all files in the same directory<br>
aodv.py uses \*\_src files to generate C files.

1:<br>
Run Script<br>
python3 aodv.py<br>

2:<br>
6 files are generated by aodv.py<br>
aodv_gen.pml<br>
pan_symm.c<br>
replace.h<br>
replace.c<br>
print_state.h<br>
print_state.c<br>

3:<br>
SPIN also generates 6 files <br>
pan.b pan.c pan.h pan.m pan.p pan.t<br>

4:<br>
Compile<br>
gcc -DNOREDUCE pan_symm.c replace.c state_print.c<br>

5:<br>
Run<br>
./a.out -E<br>

In aodv.py, there is a function genPromelaCsource(nodes=4,around=1,rtlen=2,retry=1)<br>
Args:<br>
nodes: is the number of nodes in a network<br>
around: is the number of neighbor nodes at most when a node broadcasts a packet.<br>
rtlen: is the number of entries in a routing table.<br>
retry: is how many time a source node tries to send a route request.<br>

Parameters when we conduct experiments are<br>
nodes=N, around=1, rtlen=2, retry=1.<br>
N is the number of nodes from 4 to 10.

