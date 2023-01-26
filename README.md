# For-in-loop

var object = {"a":"foo", "b":"bar", "c":"baz"};
// `a` is inaccessible
Object.defineProperty(object , 'a', {
 enumerable: false,
});
for (var key in object) {
 if (object.hasOwnProperty(key)) {
 console.log('object.' + key + ', ' + object[key]);
 }
}
