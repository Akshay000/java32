// These two have the same value I took 
new String("same").equals("same") // --> true 

// ... but they are not the same object
new String("s1") == "s1" // --> false 

// ... neither are these
new String("s2") == new String("s2") // --> false 

// ... but these are because literals are interned by 
// the compiler and thus refer to the same object
"test" == "test" // --> true 

// ... but you should really just call Objects.equals()
Objects.equals("s1", new String("s2")) // --> true
Objects.equals(null, "same") // --> false
