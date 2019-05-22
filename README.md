# designpatternjs

var task = {
    title: 'My Tiltle',
    description: 'My Description'
}

Object.defineProperty(task, 'toString', {
    value: function(){
        return this.title + ' ' + this.description;
    },
    writable: true, // change function to string
    enumerable: true, // Object.keys(task) // show 'toString' in the array 
    configurable: true // ability to redefine the whole of property
})

var urgentTask = Object.create(task, {
    name: { value: 'Saikat' },
    greet: {
        value: function(){
            return 'Hello';
        }
    }
});

//equivalent
//var foo = {}
//var bar = Object.create(Object.prototype);

