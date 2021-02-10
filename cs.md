## Computer Science


### CS Trade-offs
- **Look** vs **Leap** - optimal stopping problem / secretary problem
- **Explore** vs **Exploit** - multi-armed bandit problem
- **Sort** vs **Search**
- **Size** vs **Speed** - small and fast or big and slow
- **Speed** vs **Accuracy** - slow and accurate/robust or fast and error prone/fragile
- **Responsiveness** vs **Throughput** - cost is delay
- **Time** and **Space** vs **Certainty**

### CAP Theorem
It is impossible for a distributed data store to simultaneously provide more than two out of the following three guarantees:  
- **Consistency**: Every read receives the most recent write or an error  
- **Availability**: Every request receives a (non-error) response, without the guarantee that it contains the most recent write  
- **Partition tolerance**: The system continues to operate despite an arbitrary number of messages being dropped (or delayed) by the network between nodes  

No distributed system is safe from network failures, thus network partitioning generally has to be tolerated. In the presence of a partition, one is then left with two options: consistency or availability. When choosing consistency over availability, the system will return an error or a time out if particular information cannot be guaranteed to be up to date due to network partitioning. When choosing availability over consistency, the system will always process the query and try to return the most recent available version of the information, even if it cannot guarantee it is up to date due to network partitioning.
