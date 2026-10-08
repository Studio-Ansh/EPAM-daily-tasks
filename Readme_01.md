# Hardware Concurrency and Memory Models

### 1. Instruction Reordering

Compilers and CPUs may change instruction execution order to improve
performance. Without proper synchronization, this can cause unexpected
results when multiple threads share data.

### 2. Memory Model

Defines the rules for how threads access shared memory, order
operations, and observe changes made by other threads.

### 3. Happens-Before

Guarantees that one operation is ordered before another. Proper
synchronization ensures earlier writes are visible to the receiving
thread.

### 4. Memory Visibility

Describes whether one thread can reliably observe another thread's
changes. Synchronization helps ensure correct visibility of shared data.

### 5. Memory Barriers/Fences

Restrict the reordering of memory operations to maintain the required
ordering between threads.

### 6. Acquire and Release

-   **Release:** Publishes previous memory operations so another thread
    can observe them.
-   **Acquire:** Ensures subsequent operations can safely observe data
    published by a corresponding release.

### 7. Sequential Consistency

Provides a single, consistent global order for sequentially consistent
atomic operations, making concurrent programs easier to understand.
