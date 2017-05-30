Simple router middleware for deployd

## Installation

`npm install dpd-router-event dpd-router-middleware --save`

## Usage

app.js:

      require('dpd-router-middleware')( require('deployd/lib/router'), 'middleware')  // <----- add this
      try{
        var deployd = require('deployd')
        var dpd = deployd({port:3000});
        dpd.listen();
      }catch(e){
        console.error(err.toString()) // becomes exception in analytics 
      }

**NOTE:** *middleware* as used above can be anything but must be the name of the router event resource;

Now, open dashboard and create a `Router Event` with the name given above (*middleware* or whatever you put there)