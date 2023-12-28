## Time in a Distributed System?
In a distributed system time is used to identify the order of the event. A Centralized system runs in a single node; it 
has a global clock. We can identify the order of the events with the timestamp.

When it comes to the distributed system. We can have multiple small components which are running in multiple nodes. It 
is not possible to have a global clock for a distributed system. We can not fix the physical clock of each node and 
synchronize it. Why? Because there is always a skew between the clocks in multiple nodes.

### Logical Clocks ?
Since we can not sync the physical clock in distributed systems. We use a logical clock to determine the order of the 
event.

### What is a logical clock?
Logical clock is an alternative for a clock in a distributed system which is not dependent on the physical process. 
Instead, the logical clock uses message exchanges of the node to determine  the time and order.

### Event order with a logical clock?
Logical clock maintains a counter for each node and whenever it processes an event it will increase the counter. 
For example If a node receives events at 10:AM, 1:25 PM and 2:PM then the clock is assigned the timestamp of 1, 2, and 3 respectively. In this approaches we can determine the order of the events but we do not know the distance between the two events.
