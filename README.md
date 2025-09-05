# CRM
This is my learnings in salesforce.

-> Salesforce is a  Crm . Not only a crm but also a cloud company. Everything offered is resided in the trusted and multitenant cloud.

# RelationShips 

-> LookUp relation : LookUp relation is loosely coupled.
-> One object can be connected to other in one-to-may relation.
-> If the parent record is deleted the child record is also deleted.

# Master-Detail RelationShips 

-> Master-Detail RelationShips is strongly coupled.
-> If the parent record is deletd the child record is also deleted.


# LookUp vs Master-Detail Relation

1) LookUp 

-> Loosely coupled.
-> Roll-up summary fied is not availble.
-> Parent record is not req when creating a child record.
-> LookUp fields are not req on the page layout.
-> Child record is not controlled by parents.
-> You can have a child record without a parent record.

2) Master Relation 

-> strongly coupled.
-> Roll-up summary fied is availble.
-> Parent record is req when creating a child record.
-> Master relation is req on the page layout.
-> Child record is controlled by parents.
-> You can not have a child record without a parent record.