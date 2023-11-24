# class-8-reading

Class 8 

Css Flexbox<br>
A layout model designed for one dimension content.<br> 
Takes a bunch of items which have Dif sizes and returning best layout for items<br>
      
B.   Ideal layout of sidebar pattern<br>
	1. When there is not enough space the sidebar will break onto a new line.<br>
      
C.   What can you do w. Flex layout.<br>
	1. Display a row or a column<br>
	2. They respect the writing mode of the document<br>
	3. They re single line by default, can be asked to wrap onto multiple line<br> 
	4. Items in the layout can be visually reordered away from their order in the dom<br>
	5. Space can be dirt inside items, can become bigger & smaller according to the<br>
	     space avail in parent<br>
	6. Space can be dis around items and flex Ines in wrapped layout, using<br>
	    Box Alignment properties<br>
	7. The items themselves can be aligned on the cross axis<br> 

D. Main Axis & Cross Axis
	1. Main axis is set by is the one set by your flex-direction. 
		a. If is row your main axis is along the row<br>
		b. If is column main axis is column<br>
	2. Flex items move as group on main axis, remember we have things trying to get <br>
	    best layout for them as a group<br>
	3. Cross axis runs other direction.<br>
	4. Can do two things on the cross axis<br>
		a. Can move items individually or as group so they align against each other<br>
		    and flex container<br>

E. Creating a flex container<br>
	1. To use flexes yo need to declare you want to use flex formatting context not<br>
	     regular block and inline layout.<br>
	2. Do so changing the value of display property to flex<br>
		.containter {
		     display: flex;
		}
	3. This will give you a block level box w flex item children<br>
	4. Initial values mean that:<br>
	     1. Items display as row<br>
	     2. They do not wrap<br> 
	     3. They do not grow to fill container<br>
	     4. They line update the start of the container<br>

 D. Controlling the direction of items<br>
	1. Row items lay out as a row<br>
	2. Row-reverse items layout as row form the end of the flex container<br>
	3. Column the items layout as column<br>
	4. Column-reverse the items lay out as a column from the end of the flex container<br>

E. Reversing the flow of items and accessibility<br>
	1. Be cautious when using any props that reorder the vis display away from how<br>
	    things are ordered in the thumb doc, can have NEGATIVE on accessibility<br>
F. Writing modes and direction<br>
	1. Flex items behave/linked to writing mode of doc.<br>
	2. With main & cross & writing mode to consider we start to talk about start & end<br>
	     rather than top bottom left & right in flex box might be easier to understand<br>
	3. So our flex items line up form main start. The end of that axis is main-end. The <br>
	    end of the axis is main-end. The start of cross axis is cross-start and the end<br>
	    cross-end<br>
    
G. Wrapping flex items.<br>
	1. The initial val of flex-wrap prop is nowrap means not enough space in cont will<br>
	    overflow<br>
	2 When flex cont wraps it creates multi flex lines. 
		a. Each line acts like a new flex container. If wrapping rows it is not possible<br> 
		    to get something in row 2 to line up w. Something above in row 1. <br>

H. Flex flow shorthand. <br>
	1. Can set flex-direction, flex-wrap, using props using shorthand flex-flow<br>
	
I. Controlling space inside flex items<br>
	1. Assuming our container has more space than is needed to display items.<br>
	    they stop growing at the max content size. Due to initial val of flex prop<br>
		a. Flex-grow: 0 do not grow<br>
		b. Flex-shrink; 1 items can shrink smaller than their flex-basis<br>
		c. Flex-basis: auto items have a base size of auto<br>
	2. Can be repped by keyword val of flex:initial. Flex shorthand prop or longhand<br>
	    prop flex-grow, flex-shrink, flex-basis applied to children of flex container<br>  
	3.See following for flex grow, shrink and basis https://web.dev/learn/css/flexbox/<br>

     
J. Diff vales for flex. 
	1. Can do same thing from flex basis or auto need to spec 3 Vals<br>
		a. Flex grow<br>
		b. Flex shrink<br>
		c. Flex basis<br>

K. Reordering Flex items<br>
	1. Items can be re-ordered by using order prop. Allows the ordering of ordinal
	    groups<br>   
	2. Items laid out in the direction dictated by flex direction lowest val 1st. 
	3. If more than one item has the same val it will be displayed w. Other items of that<br>
	    value<br>

L. Distributing space on the main axis<br>
	1. Justify-content prop to flex container tive it a val of flex end and the items line<br>
	    up<br> at the end of the container and the spare space is place at the star<br>

M. With flex-direction: column<br>
	1. If change flex direction to common with justify content will work on column<br> 
	    to have space needed need to give container height or block-size<br>

N. Distributing space between flex lines<br>
	1. Flex start by default the initial val of align-content is stretch. Add prop<br>
	    align-content to the flex container to change the default behavior<br>

P. Aligning items on the cross-axis<br>
	1. On cross axis you can align items within flex line using align-items and align self<br>
	2. Following values to align the items<br>
		a. Flex-start<br>
		b. Flex-end<br>
		c. Center<br>
		d. Stretch<br>
		e. Baseline<br>

Q. Why no justify-self in flex box. <br>
	1. Flex items act as a group on. Main axis so cannot split up.<br>
	2. In grid layout justify-self and justify-items properties work on the inline axis <br> 
	     to do alignment of items on that axis within their grid area<br>
	3. Flex box does work very nicely with auto margins.<br>

R. How to center an item vertically and horizontally<br>
	1. Alignment props can be use to cent item inside other box.<br>
	2. Justify content prop aligns the item on the main axis. The align-items prop on<br>
	    cross axis.<br>


II. FlexBox MDN<br>
A. Why Flexbox? Cannot do following with css position and floats<br>
		1. Vertically centering a block of content inside parent<br>
		2. Making all the children of a container take up an equal amount of avail<br>
		     width/height regardless of how much width/heigh is avail<br>
		3. Making all columns in a multiple column layout adopt the same height<br>
		    even if they contain a diff amount of content<br>

B. Specifying what element to lay out as flex boxes<br>
		1. Start need to select elements to be laid out as flexible boxes<br>
		2. Set val of display on parent element of the elements you want to affect<br>
		3. In this case we lay out the article  element so we set this on the section<br>
		4. This causes the section element to become a flexible container and it’s<br>
		    children flex items. 
	C. What’s happening here’s. 
		1. Element given display val of flex to is acting like block level element<br>
		2. It’s children are laid out as flex items. 

D. The Flex model<br>
		1. The main axis -> running the direction of the flex times are laid out in<br>
		2. The start and end of axis are call the main start and main end<br>
		3. Cost axis is the axis running perpendicular to the direction of flex items<br>
		4. Parent element that has display: flex set on it is called the flex container.<br>

E. Columns or rows. <br.
		1. FB provides a prop called flex-direction that specifies which direction the<br>
		    the main axis runs<br>
		2. By default thesis se to row, which means they are laid out in row<br>
		3. Flex-direction: column; puts things in a column<br>

F. Wrapping<br>
		1. Issue arises when yo have fixed width or height in your layout eventually<br>
		    your flex box children will overlook their container<br>
		2. Can be fixed with flex-wrap: wrap; and flex: 200px;<br>

G. Flex-flow shorthand<br>
		1. Flexflow shorthand for flex-direction, flex-wrap, flex-flow can replace<br>
			flex-direction: row;
			flex-wrap: wrap; 
			with 
			flex-flow: row wrap;


### Questions
1. Flexbox is designed for one-dimensional content. Explain what this means.
	a. It moves items left and right and up and down it does not move them forward or deeper in to the page. 

2. Explain the difference between the main axis and cross axis.
	a. The main axis is the axis you set items to display in a row which is horizontal and<br> 
column is vertical. The cross axis is perpendicular to the main axis. 

3. How can using certain properties of flexbox negatively impact accessibility?
	a. Using row-reverse and column-reverse can have a negative impact on accessibility<br>
	    by reordering the visual display away from how things are ordered in the html<br>

1. What are some advantages of using flexbox over float?<br>
	a. You have the ability to center things correctly off of their parent which is impossible<br>
	using float<br>
2. How does this topic connect with your long term goals?<br>
	a. It makes layouts tidier<br>

## Stuff I want to know more about
  EVERYTHING
	
	
