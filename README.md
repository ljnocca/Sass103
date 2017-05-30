# Sass103

## Main Lessons

## Color Functions
* The function fade-out makes a color more transparent by taking a number between 0 and 1 and decreasing opacity, or the alpha channel, by that amount:
   ```
   $color: rgba(39, 39, 39, 0.5);
   $amount: 0.1;
   $color2: fade-out($color, $amount);//rgba(39, 39, 39, 0.4)
   ```

	* The fade-in color function changes a color by increasing its opacity:
	```
	$color: rgba(55,7,56, 0.5);
	$amount: 0.1;
	$color2: fade-in($color, $amount); //rgba(55,7,56, 0.6)
	```
	* The function adjust-hue($color, $degrees) changes the hue of a color by taking color and a number of degrees (usually between -360 degrees and 360 degrees), and rotate the color wheel by that amount.
* Here is how Sass computes colors:
1. The operation is performed on the red, green, and blue components.
2. It computes the answer by operating on every two digits.
`$color: #010203 + #040506;`

* EACH LOOPS in Sass iterate on each of the values on a list. The syntax is as follows:
	```
	@each $item in $list {
	  //some rules and or conditions
	}
	```
* The value of $item is dynamically assigned to the value of the object in the list according to its position and the iteration of the loop.

* FOR LOOPS in Sass can be used to style numerous elements or assigning properties all at once. They work like any for-loop you've seen before.

	* Sass's for loop syntax is as follows:
	```
	@for $i from $begin through $end {
	   //some rules and or conditions
	}
	```
1. $i is just a variable for the index, or position of the element in the list
2. $begin and $end are placeholders for the start and end points of the loop.
3. The keywords through and to are interchangeable in Sass

* In Sass, if() is a function that can only branch one of two ways based on a condition. You can use it inline, to assign the value of a property:

`width: if( $condition, $value-if-true, $value-if-false);`
*	For cases with more than two outcomes, the @if, @else-if, and @else directives allow for more flexibility.
	```
	@mixin deck($suit) {
	 @if($suit == hearts || $suit == spades){
	   color: blue;
	 }
	 @else-if($suit == clovers || $suit == diamonds){
	   color: red;
	 }
	 @else{
	   //some rule
	 }
	}
	```
	



