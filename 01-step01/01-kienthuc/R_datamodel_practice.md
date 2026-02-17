## 2. Object relationship

Create relationships for the Offer object
The object you created for the previous challenge is pretty handy. Imagine how much more useful it would be if brokers could specify which client made an offer and which property the client wants to buy. Add two relationships to the Offer object so brokers can capture this data in Salesforce. Create a Master-Detail relationship with the Property object and a Lookup relationship with the Contact object.

Even if you're completing this module as part of the Admin Beginner trail, be sure you use the new Trailhead Playground you created in the previous unit.
Before You Start:
Create the Property object as described in the previous unit.

Challenge Requirements:
Create a custom Master-Detail field on the Offer object
Data Type: Master-Detail
Related To: Property
Field Label: Property
Field Name: PropertyCopy
Create a custom Lookup Relationship field on the Offer object
Data Type: Lookup Relationship
Related To: Contact
Field Label: Contact
Field Name: ContactCopy