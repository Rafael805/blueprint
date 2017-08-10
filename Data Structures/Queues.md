# Queue

**Queues** are the classis **"First In, First Out" (FIFO)** data structure.

They are very common, for example in event driven operating systems (OS). A queue is used to store the events occuring in the system. 

The OS msut respond to events in the order they occur. For instance, as you type every time you hit a key, the OS registers which key you hit in an event queue.  Useful for any type of system where we want to process things in the order they arrived. So a web server may queue requests and process them in the order they arrived which seems fair. Or a printer may print documents in the order they arrived. 
