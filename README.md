DataWeave Code Challenge
======


This repository will contain the solutions to the test problems, and there will be 
a launch script that should be used to launch these solutions.


Notes
======

* This code is going to be developed for Python 2.7.
* Assumption: I am assuming the solution should be Linux/Windows compatible.
* Criteria: No third-party modules.


Task 1: Key-Value Server
======

Need to develop a key-value server that can be used to store a unique key-value mapping.
Any machine on the network needs to able to access this server's information.

Required features:
----

    * User should be able to specify the number of versions that the server can keep for any mapping.
    * Each time that the value is modified, the previous value should be recorded, so long as the min
    min. history value is greater than or equal to 1.
    * The history beyond the required min. historical data should be discarded.
    * Allowed operations:
        - ADD(key, value)
        - GET(key, version=None), return the latest if the version requested is not specified.
        - DELETE(key)

Restrictions:
----

    * Do not use dictionaries or any readily available hashmaps.


Thoughts:
----

    * Need to figure out how to write a TCP server that listens for requests and returns the value.
    * Need to figure out how to store this hashable data without relying on dictionaries.
    * How do I optimize this for speed? If a million values need to be stored on something like this, 
    how will the code handle it.


