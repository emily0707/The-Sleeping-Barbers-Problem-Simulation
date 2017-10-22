# What does this Program do? 
This program simulates the sleeping barber problem with multiple barbers and customers threads. 

## The Sleeping-barber problem
A barbershop consists of a waiting room with n chairs and a barber room with m barber chairs. If there are no customers to be served, all the barbers go to sleep. If a customer enters the barbershop and all chairsare occupied, then the customer leaves the shop. If all the barbers are busy but chairs are available, then the customer sits in one of the free chairs. If the barbers are asleep, the customer wakes up one the barbers.                                                                                                                                                      
## Challenges  
Avoid deadlocks and yet serve as much customers as possible. 

## Solutions
1. Use two critical Sections, one for barbers, one for customers. 
2. Use pthread_cond_timedwait(). For example, A barber has to enter a critical section to wait for a customer. To avoid deadlocks, the barber thread waits for a customer to give him a service signal within a certian time period.  Then it goes back to check any customer sits on his chair. 

