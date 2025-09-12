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


# Junction Objects

-> Junction objects are used to create many-to-many relation.
-> They are created using a custom object to relate two other objects via two master-Detail RelationShips.
-> Only two master detail relations are allowed in an object
-> The first master detail relation u create in the Junction object becomes your primary relationship.
-> The look an feel will be the same as your primary master master object.
-> The junction object record inherits the value of the owner field from the primary master object.
-> Since the owner filed is not visible in the details side of the relationship , this inherited value is relevant if both
the master detail relationships on junction object are deleted.
-> In case if u delete the primary master detail relationship or convert it into lookup relationship
then the secondary master object becomes the primary master object.
-> We dont use lookup relation in junction object because there is no cascade option in lookup.

# Roll-up summary 

-> Roll-up summary can only be done in the master-detail relationship.
-> Roll-up summary is only allowed on the parent object.
-> we perform count,sum,minimum value,maximum value of a field in the details record.

# Page Layout

-> Page layout controls the presentation of fields,related lists and custom links on object record pages.
-> They also help determine which fields are to be visisble,read-only and required.
-> Page layout in salesforce is created with the object naeme by default.
-> There will be one minimum page layout for every object by default.
-> Multiple page layouts can be created to an object.

# Features of Page Layout

** Fields 

-> You can add , remove (or) re-arrange them on a page layout.
-> You have the option to modify field properties within the page layout. 

** Buttons 
 
-> You have the ability to manage which standard and custom buttons are shown.
-> You can also configure the sequence in which custom buttons are presented.

** Custom links

-> generates a personalized link for the object by utilizing the button,link and action functionality.
-> you cam add these custom links to the details page of the record page layout.

# Record Types

-> Record type is a feature in salesforce that is used to define different picklist values,
or different page layouts for the records in the same object.

-> If you want to map the record types to the page layout we use page layout assignment.

# Validation rules

-> validation rules in salesforce verify that the details entered by the user meet certainc criteria before the record is
inserted or updated.