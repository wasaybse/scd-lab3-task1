Implement the following program on eclipse IDE and answer the following questions:
How many threads are running?
Ans: There are 3 threads running (t1, t2, t3).
How many tasks are running?
Ans: There are 3 tasks running — each thread executes the run() method once.
If more tasks are added than what will be the impact on number of threads?
Ans: If you add more tasks (for example, t4, t5, etc.),then more threads will be created and started.
Each task (thread object) runs independently and concurrently, so CPU scheduling will handle more threads simultaneously.
Explain the flow of program:
Ans: The class Main extends Thread, so it can run as a separate thread.
Three objects (t1, t2, t3) are created.
Each .start() call starts a new thread and invokes run() method.
JVM handles thread scheduling — the output order may vary (since threads run concurrently).
Each thread prints "task one" — possibly in random order.
#Code:

    class Wasay extends Thread {
    public void run() {
        System.out.println("task one");
    }

    public static void main(String args[]) {
        Wasay t1 = new Wasay();
        Wasay t2 = new Wasay();
        Wasay t3 = new Wasay();

        t1.start();
        t2.start();
        t3.start();
    }
}
