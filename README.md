# Inheritance and Delegation

This repository is set up for discussion on relative strengths and weaknesses of 
`inheritance` and `delegation`.

Lab05 Handout can be found at: [https://github.com/CMU-17-214/s2024/blob/main/labs/lab05.md](https://github.com/CMU-17-214/s2024/blob/main/labs/lab05.md)

# Responses

##### Which is more dependent on the implementation details of the SortedIntList, composition or inheritance?
Inheritance. I had to make sure to check the implementation of addAll to ensure that it called add().

##### If the add method in SortedIntList is significantly modified or its behavior changes, which implementation is more likely to break?
In this case, both are equally likely, since I either called super.add() or the delegation.add(). 
But in general, the inheritance method couples both classes more closely, and is more likely to break.

##### What issues does using composition solve that might have been problematic with inheritance?
If SortedIntList changes the underlying implementation of addAll() to add numbers directly instead of 
calling add(), then our inheritance solution will break.

##### Based on the provided implementations, when would it be more appropriate to use inheritance and when to use composition?
Use inheritance when strong coupling is reasonable and implementations are known to be stable. 
Use composition when we need more re-usability, testability and extensibility.