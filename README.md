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

** Types of validation rules

1) Standard validation rules : these are the rules that are applied by the system for data consistency
2) Custom validation rules : allows you to create the rules according to your business needs

** Validation Rules Fields : 

in order to create a validation rules some of the fields are needed to be defined

i) Rule name
ii) Active
iii) Description
iv) Error condition formula
v) Error message
vi) Error location

# List views

-> A list view is a filtered list of records where you can view records for one object at a time.
-> If u want to add a custom list, u can click on list view controls and select new.
-> you can add upto 15 fields in list view.

# Filed dependency

-> In salesforce if we select the controlling field , the other field(dependent field) should show the value those relate to the
controlling field.
-> For ex : if the controlling field is Technologies and the dependent field is Certifications then the Certifications should show the
value that relate to specific Technologies.

** Controlling Fields

-> The controlling field decides the behaviour of the dependent field. 
-> There are 3 controlling fields they are chekbox,standard picklist , custom picklist

** Dependent Fields

-> The dependent field shows only those values related to the controlling field, in the dependent field we can set which values
should be displayed according to the controlling field. 
-> There are 2 controlling fields i) custom picklist ii) multiselect picklist

** Uses of field dependency 

-> we can filter the dependent values based on the values we select in the controlling field using the field dependency.
-> It enhances the accuracy while creating the record because when we select the controlling field, then in the dependent field
it shows only the values that are realted to the controlling field.

** Considerations of field dependency

-> After converting the existing field to a controlling field (or) a dependent field , it does not affect your existing records
it will apply for new records.
-> If you change the existing controlling field value, then the dependency field value will be lost.

# Lightning App Builder 

-> Lightning app buider is a point and click tool that makes it easy to create custom pages for the salesforce mobile app and 
giving the users what they need all in one place.
-> You can update the app's branding , navigations and options and also the lightning pages associated with the app with the help of
lightning app builder.
-> Lightning app builder can be used to single page applications.
-> Lightning app builder can be used to create dashboard style applications (like shwoing most sales) etc.
-> They can be used to build point apps for ex : expense apps that allow users to enter the price and monitor expenses they submitted.
-> They can be used to create custom record pages for your objects.
->  They can be used to create custom home pages containing the components and features that users mostly use.

# Lightning components

-> A lightning component is a compact, configurable and reusable element that you can add to the lightning web page in a lightning app builder.
-> Lightning pages support these components standard components , custom components and third-party components on app exchange
-> Standard component : standard components are the components built by salesforce.
-> Custom components : Custom components are the components that are built by you or someone else for you, you can customize these 
to work in the lightning app builder.
-> Third-party components : The AppExchange provides a marketplace for these lightning components you can find the pacakages that are
already configured and ready for use.

# Building custom home page for lightning experience

-> You can build custom home pages for diff profiles.
-> Go to setup and find the lightning app builder .
-> Click on the new and select the home page.
-> Choose the template and place the components and click on save.
-> click on activate and choose apps and profile.

# Dynamic forms

-> Dynamic forms break the record detail fields into seperate individual fields and section components that you can put
anywhere on the page, including seperate tabs and and accordain sections.
-> You can use the visibility rules to show the end users only the fields they need to see, when they need to see.

# Uses of Dynamic forms

-> Dynamic forms give you an instant upgrade from the page layout , you can place the components where ever you wish.
-> Dynamic forms gives you visibility rules to show and hide fields and sections.

# Customizing the page

-> Even though you broke the record detail into individual components there me still some fields which may result in perfomance issues.
-> one way to resolve this issue is to move the low-priority fields to tabs and accordians whose content is not visible when the page loads.

> steps : 

1) start by optimizing the app by deleting the empty other information section.
2) click the details tab on the canvas
3) Hover over to the other information section and click on the delete icon.

# Security in salesforce

** Organizational level : Organizational level is the highest level of security in salesforce. It includes maintaining a list of 
authorized users , set password policies and limit login hours and locations.

** steps to achieve security in Organizational level : 
1) Ip restriction : allows only certain ip address.
2) Password policies : makes the password expirwe after certain amount of time and increase the complexity of the password creation
so that it is hard to hack.
3) Login access : specify the users about the timing when they are allowed for logging in.

** Object level : Object level is used to control the data access . Using object permissions you can prevent the user from seeing,
editing (or) deleting any instance of a pariticular object like lead (or) Opportuinity.
-> Object permissions can be set in the permissions and profiles.
1) Permission set : a permission set is a collection of settings and permissions that give user access to various tools and functions.
2) Profiles : a profile is a set of collection of settings and permissions that defines what a user can do in the application.

** Field level : field level security in salesforce is congigured for the users profile . Using field level administrator can control 
whether a user can create,see,update and delete a pariticular object field.

** Record level : Record level security allows pariticular users to view an object but restricts the individual object records they are allowedto see.
-> you can manage record level access in 4 ways.
1) organization - wide defaults
2) Role hierarchies
3) Sharing rules
4) Manual Sharing 

** organization - wide defaults : owners of the record have full access to the crud operations. so if a user wants he can make the 
object record private or public.

** Role hierarchies : The higher hierarchy have the access for the records of the below users.

# Password policies

** Setting up password policies

-> you can set password and login policies such as specifying the amount of time before all the user's password expire and the complexity
of the password.

** Expire passwords

-> Expire the password of all the users except for those with "Password never expire" permission.

** User password reset

-> Resert the password of the users.

# Control access to Objects

** Manage object permission 

-> The simpliest way to control the data access is to set the permission on a pariticular object.
-> You can control whether the user can create,read,edit or delete any records of that object.

** Permission sets : It is used to assign object,fields and user permission to the users.Users can be assigned multiple permission sets.

** Permission set groups : used to group multiple permission sets for easier management.

** Profiles : used to configure user's default settings such as assigned apps,record types and page layouts.

# Profiles 

-> A profile is a collection of settings and permissions that determine which data and features users can access on the platform.

# Permission set

-> A permission set is a collection or group of permissions that gives users access to various tools and functions like profiles.