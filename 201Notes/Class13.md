# Readings

## Local storage and how to use it on websites:

Why: Persistence

How: Cookies (but they typically allow only 4kb of storage, considered spyware to some) OR **LOCAL STORAGE!!!!**

Using JavaScript:

``` localStorage.setItem('favoriteflavor','vanilla'); 

var taste = localStorage.getItem('favoriteflavor');
// -> "vanilla"

localStorage.removeItem('favoriteflavor');
var taste = localStorage.getItem('favoriteflavor');
// -> null
```

An issue local storage has is, it can only use Strings. We bypass this using JSON.stringify() and JSON.parse():

``` var car = {};
car.wheels = 4;
car.doors = 2;
car.sound = 'vroom';
car.name = 'Lightning McQueen';
console.log( car );
localStorage.setItem( 'car', JSON.stringify(car) );
console.log( JSON.parse( localStorage.getItem( 'car' ) ) );
```

It's uses are to ensure caching, e.g. second and further loadings of a page is much more instant. 
However it is possible for hackers or ill intended uses of local storage.

### Questions:

Why would a developer use local storage for a web application?
- Allows for faster loadings, persistence and for data to be stored further than a single session. 
What information should not be stored in local storage?
- Sensitive data such as personal passwords, credit card details and anything you wouldn't give a stranger in the street.
Local storage can store what type of data? How would you convert it to that type before storing?
- Any type of data, however we are required to use JSON.stringify() to convert the data into a JSON string before storing it in
  local storage. JSON.parse() does the reverse. 
