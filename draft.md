<h1>DESIGN DOCUMENT!

<h2>Overview


This Document outlines the construction of the "ADIN INSPECTOR" per the specifications of the requirements document.
The system is split into two distinct packages ??, the Back-end and the Front-end.
The Backend comprises of the Kafka messaging system, a mongoDB database and a mediator.
When the software starts it initlializes an instance of Zookepeer and the Kafka Server, next a consumer is started for all topics provided by Kafka.
When the consumer recieves a message from a specific topic it checks the databse to see if the entry already exists, if not then it is added to the databse.

FRONT END STUFF
<h2>Classes
<h3>Back-end

STUFF!
Things!
excitement!
<h2>Class Diagrams
<h2>Sequence Diagrams (zb. test cases from pflichtenheft )
<h2>Packages
<h2>Testing flow proposal
