- LinkedBlockingQueue 用的是 Guared Suspension 模式。调用 take 函数的时候，如果队列为空，则会被阻塞。

- 等待端的示例
  ```java
  while (!ready) {
    wait();
  }
  ```
- 唤醒端的示例
  ```java
  ready = true;
  notifyAll();
  ```