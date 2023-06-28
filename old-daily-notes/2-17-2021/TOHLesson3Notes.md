#   reporting activity will be reported on thursday or friday - talk with your teammates!

#   TOH App Architecture Breakdown
-   We have a UI layer, a business logic layer, and a data layer. We also have a model layer for these layers to manipulate as needed
    -   Our UI is referencing our business logic layer, and models.
        -   The UI layer references the business logic layer and models, but NOT the data layer. You don't want front end users to be able to interact directly with your data!!!
    -   The BL layer is where you are processing input from the UI. It also has access to the Model class to manipulate model logic
        -   examples: validation, formatting, processing, backend interaction etc.
    -   The DL is just pushing and pulling data from the data source

#   TOH App Design Notes
-   Overriding the ToString method is as simple as providing the override keyword in the signature when declaring the ToString() method.
-   If you don't override the ToString method, it's default return is just the type of the object
-   Only methods that are virtual can be overridden.
    -   The virtual keyword is used to modify a method, property, indexer, or event declaration and allow for it to be overridden in a derived class.



# our store app will just be a console app :)
-   One of our requirements for the project is for our data to be persistent!


