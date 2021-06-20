# Distinguish data, computed, method, watch
#### Data: Type is object or function (return an object)
- Properties is reative
#### Computed: Type: [key: String]: Function
- **Computed** contains properties like **data** do. However the properties inside **computed** can be caculate. And They are cached,
only re-evaluate when any its reactive dependencies changes (The properties(variable) you use inside **computed** are all its dependencies, but reactive dependency are those that are observable, like **data** properties)
- Usually, computed properties are caculated based on props or local data(of course props and data will be its reactive dependencies)
#### Method
**Method** can do everything that **computed** can. The diffrence is **computed** can cache data and it can't receive parameter.
#### Watch
if you want to do sth when a data changes, you can use **watch**
Note: Only watch reactive data (non-reactive will not watch)