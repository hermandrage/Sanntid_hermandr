# Reasons for concurrency and parallelism


To complete this exercise you will have to use git. Create one or several commits that adds answers to the following questions and push it to your groups repository to complete the task.

When answering the questions, remember to use all the resources at your disposal. Asking the internet isn't a form of "cheating", it's a way of learning.

 ### What is concurrency? What is parallelism? What's the difference?
 > *parallelism: Gjøre flere ting samtidig*
 > *Concurrency: Switche fort mellom å gjøre forskjellige ting, sånn at de tilsynelatende gjøres samtidig.*

 ### Why have machines become increasingly multicore in the past decade?
 > *Fordi multicore gir deg bedre utelse, og det har i større og større grad blitt mulig det siste tiåret siden de har blitt mindre.*

 ### What kinds of problems motivates the need for concurrent execution?
 (Or phrased differently: What problems do concurrency help in solving?)
 > *Utnytter ventetiden mens man venter på inn/uotputs.*

 ### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
 (Come back to this after you have worked on part 4 of this exercise)
 > *Begge deler muliggjør ting du ikke kunne gjort uten concurrency, men mer styr.*

 ### What are the differences between processes, threads, green threads, and coroutines?
 > *Coroutines er at ting gjennomføres sekvensielt (prosedyre), mens med tråder kan man consepuelt gjøre flere ting samtidig. Greenthreads er styrt av et runtime libary eller en virutal machine i stedenfor et naivt OS. Processes kjører på en separat memoryspace, mens tråder gjører på en som er delt.*

 ### Which one of these do `pthread_create()` (C/POSIX), `threading.Thread()` (Python), `go` (Go) create?
 > *pthread_create() lager en ny tråd, threading.Thread() lager en greenthread og go er en coroutine.*

 ### How does pythons Global Interpreter Lock (GIL) influence the way a python Thread behaves?
 > *Gjør at bare en tråd kan være i execution mode om gangen*

 ### With this in mind: What is the workaround for the GIL (Hint: it's another module)?
 > *Use the multiprocess module*

 ### What does `func GOMAXPROCS(n int) int` change?
 > *GOMAXPROCS sets the maximum number of CPUs that can be executing simultaneously and returns the previous setting. If n < 1, it does not change the current setting. The number of logical CPUs on the local machine can be queried with NumCPU. This call will go away when the scheduler improves.*
