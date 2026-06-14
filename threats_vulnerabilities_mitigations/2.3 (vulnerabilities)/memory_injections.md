# Memory Injections

Software on a computer runs inside of memory. Nothing executes from hardware unless loaded from a disk itself AND processed by memory & cpu.

By this application, malware also runs in memory. Memory forensics can find malicious code. Memory contains running processes that malware can inject itself into. DLLs (Dynamic Link Libraries), threads, buffers, etc.

Malware is very hidden. It runs in its own process and usually injects itself somewhere into a legitimate process.

Let's say malicious code is injected into running memory. Because that memory holds one set of rights and permissions, it will run whatever (granted it has permission) that script 

## DLL Injection

Dynamic Linked Lists are functions or libraries that Windows that contains code or data. Many applications can use this library (this saves alot of time and memory as opposed to implementing the function for each individual application.) These can not be edited but they can be added even if they're malicious. To get a system to see it, attackers will inject a path in memory to that malicious DLL. 

This is one of the most popular memory injection methods as it is relatively simple to implement while as being very effective.