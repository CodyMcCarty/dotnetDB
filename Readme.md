# Persist and retrieve relational data with Entity Framework Core  
Part of the MS learn path  
https://docs.microsoft.com/en-us/learn/modules/persist-data-ef-core/3-migrations

* Uses SQLite
* The entity models, Pizza.cs, Topping.cs, and Sauce.cs, have the following relationships:  
** A pizza may have one or more toppings.  
** A topping may be used on one or many pizzas.  
** A pizza may have one sauce, but a sauce may be used on many pizzas.  
* You may experiment with the app as you wish. Whenever you'd like to start with a fresh database, stop the app and delete the ContosoPizza.db, .db-shm, and .db-wal files, and then run the app again.
* 

## HttpRepl
1. dotnet tool install -g Microsoft.dotnet-httprepl
1. dotnet run --urls=https://localhost:5101
1. httprepl https://localhost:5101
* get, get 2, delete 4
* post  
(If no default editor:  
`pref set editor.command.default "<EXECUTABLE>"`  i.e.  
`pref set editor.command.default "C:\Program Files (x86)\Notepad++\notepad++.exe"`)  
```
{
  "name": "BBQ Beef",
  "sauce": {
    "name": "BBQ",
    "isVegan": false
  },
  "toppings": [
    {
      "name": "Smoked Beef Brisket",
      "calories": 250
    }
  ]
}
```
* Run the following command to add another topping to the new BBQ Beef pizza. `put 4/addtopping?toppingId=5 --no-body`
* Run the following command to change the sauce on the BBQ Beef pizza. `put 4/updatesauce?sauceId=2 --no-body`

// TODO: start reverse engineering https://docs.microsoft.com/en-us/learn/modules/persist-data-ef-core/5-test-db-operations