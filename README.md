# Car Dealership Application

# Description
The application should display cars to the user in a list. The user can view the cars' details where there should be some contact information if the buyer is interested.
The user should have a search option and some filtering options to make the browsing easier. There should be an admin dashboard for the dealership's employees where they can
add, update or delete cars in/from the inventory. Normal users should not be able to access the admin features.

# Domain Details
Each car that is added should have the following fields: make, model, year, horsepower, transmission type (automatic/manual), type (Sedan, Coupe, SUV, Truck, Cabrio etc.), color.

# CRUD
To create a car the admin should press a button "Add New" or something similar. This will get the user to a new page or pop-up and present the empty fields with placeholder text in them
to guide the user. There should be the following fields to fill. Make, Model, Year, Horsepower, Transmission, Type, Color. All fields should be mandatory to fill out in order to create a new car.

Reading cars will happen when the admin goes to the inventory section where they can see all the cars and edit/delete them, or when the user will browse the collection of cars. There should be filters for reading cars and a search bar for both the inventory in the admin dashboard and the actual inventory presented to the user.

To update a car the admin should press a button "Update" near the car that they want to update and a new pop-up or window will show presenting the updateable fields. The fields should be the same
as in the Add section but they will be precompleted with the current information of the car which the admin will be able to edit and then hit some button like "Save" at the end of the fields to make the changes persist.

To delete a car the admin should press a button "Delete" near the car that they want to delete and a confirmation pop-up should show making sure the admin did not accidentally click the "Delete" button. If the admin confirms the delete, then it will persist and the car will be removed from the database.

# Persistence Details
Create, Update and Delete operations should persist on the server and the local database alike.

# Offline Service
When the server goes offline the changes should persist on the local database and placed in a queue so when the server comes back up, the changes can be applied on the server side database as well.
When the server goes offline a bar on the top side of the screen should notify the user that the server is down and the application is using the local database.
Add operations by the admin should persist on the local database when offline. When back online the server side database will be updated and the new entities will be added.
Update operations by the admin should persist on the local database when offline. When back online the server side database will be updated with the new information.
Delete operations by the admni should persist on the local database when offline. When back online the server will get updated and all deleted entities in the local database should be removed on the server as well.
Read operations should work normally except that the local database will be used to fetch the entities, which might result in some entities missing, depending on the scenario.
