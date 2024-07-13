# WPF Zoo Manager

Zoo Manager is a WPF application that allows users to manage zoos and their associated animals. It provides functionalities to add, update, and delete zoos and animals, as well as to associate animals with specific zoos. The application uses an MS SQL Server database to store and retrieve data.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Database Schema](#database-schema)
- [Code Overview](#code-overview)
- [Contributing](#contributing)
- [License](#license)

## Installation

1. Clone the repository:

    ```sh
    git clone https://github.com/yourusername/ZooManager.git
    ```

2. Open the solution in Visual Studio.

3. Update the connection string in `App.config` to match your database configuration:

    ```xml
    <connectionStrings>
        <add name="WPF_ZooManager.Properties.Settings.UdemyCourseConnectionString" connectionString="Your_Connection_String_Here" providerName="System.Data.SqlClient"/>
    </connectionStrings>
    ```

4. Build and run the application.

## Usage

1. **View Zoos**: The application displays a list of all zoos in the database.
2. **View Animals**: The application displays a list of all animals in the database.
3. **View Associated Animals**: When a zoo is selected, the application displays a list of animals associated with that zoo.
4. **Add Zoo**: Enter the location of a new zoo in the textbox and click "Add Zoo" to add a new zoo to the database.
5. **Update Zoo**: Select a zoo, modify its location in the textbox, and click "Update Zoo" to update the zoo information.
6. **Delete Zoo**: Select a zoo and click "Delete Zoo" to remove it from the database.
7. **Add Animal**: Enter the name of a new animal in the textbox and click "Add Animal" to add a new animal to the database.
8. **Update Animal**: Select an animal, modify its name in the textbox, and click "Update Animal" to update the animal information.
9. **Delete Animal**: Select an animal and click "Delete Animal" to remove it from the database.
10. **Add Animal to Zoo**: Select a zoo and an animal, then click "Add Animal to Zoo" to associate the animal with the selected zoo.
11. **Remove Animal**: Select an animal from the associated animals list and click "Remove Animal" to disassociate it from the selected zoo.

## Features

- View, add, update, and delete zoos
- View, add, update, and delete animals
- Associate and disassociate animals with/from zoos

## Database Schema

The application uses the following database schema:

- **Zoo Table**
    - Id (Primary Key)
    - Location

- **Animal Table**
    - Id (Primary Key)
    - Name

- **ZooAnimal Table**
    - ZooId (Foreign Key referencing Zoo.Id)
    - AnimalId (Foreign Key referencing Animal.Id)

## Code Overview

The main functionalities of the application are implemented in `MainWindow.xaml.cs`:

- **ShowZoos()**: Displays the list of zoos.
- **ShowAllAnimals()**: Displays the list of all animals.
- **ShowAssociatedAnimals()**: Displays the list of animals associated with the selected zoo.
- **AddZoo_Click()**: Adds a new zoo.
- **UpdateZoo_Click()**: Updates the selected zoo.
- **DeleteZoo_Click()**: Deletes the selected zoo.
- **AddAnimal_Click()**: Adds a new animal.
- **UpdateAnimal_Click()**: Updates the selected animal.
- **DeleteAnimal_Click()**: Deletes the selected animal.
- **AddAnimalToZoo_Click()**: Associates an animal with the selected zoo.
- **RemoveAnimal_Click()**: Disassociates an animal from the selected zoo.


## Screenshot of Zoo Manager
![Zoo Manager Screenshot](https://github.com/DimitarAtanassov/WPF-ZooManager/blob/master/ZooManagerSS.png)
