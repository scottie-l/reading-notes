# Notes - Day 14

_<a href = "https://learn.shayhowe.com/advanced-html-css/css-transforms/">"Transforms"</a>_

Transform property comes in 2 different settings: 2d & 3d. Each with own properties and values.

Syntax is easy. transform followed by value amount inside the parenthesis.

Elements may be distorted, or transformed, on both 2d plane or 3d plane. 2d transforms work on the x, y axis, known as horizontal and vertical axis. 3d transforms work on both the x and y axis, as well as z axis. These 3d transforms help define not only length and width of element, but also depth.

The transform property accepts handful of different values. Rotate value provides ability to rotate element from 0 to 360 degrees. Using positive value will rotate element clockwise, and using negative value will rotate element counterclockwise. Default point of rotation is center of element, 50% 50%, both horizontally and vertically.

Using scale value within transform property allows you to change the appearance size of element. Default scale value is 1, so any value between .99 and .01 makes element appear smaller while  value greater than or equal to 1.01 makes element appear larger.

Possible to scale only height or width of element using scaleX and scaleY values. ScaleX value will scale width of element while the scaleY value will scale height of element. To scale both height and width of element but at different sizes, x and y axis values may be set simultaneously. To do, use scale transform declaring x axis value first, followed by comma, then y axis value.

Translate value works like that of relative positioning, pushing and pulling element in different directions without interrupting normal flow of document. Using translateX value will change  position of element on horizontal axis while using the translateY value will change position of element on vertical axis.

Like scale value, to set both x and y axis values at once, use translate value and declare x axis value first, followed by comma, then y axis value.

Distance values used within translate value may be general length measurement, usually pixels or percentages. Positive values will push element down and to right of its default position while negative values will pull element up and to left of its default position.

Last transform value in group, skew, used to distort elements on horizontal axis, vertical axis, or both. Syntax is similar to the scale and translate values. Using skewX value distorts element on horizontal axis while skewY value distorts element on vertical axis. To distort element on both axis the skew value is used, declaring x axis value first, followed by comma, and then the y axis value.

The distance calculation of skew value is measured in units of degrees. Length measurements, such as pixels or percentages, do not apply here.

Common for multiple transforms to be used at once, rotating and scaling size of element at same time. In this event multiple transforms can be combined together. To combine transforms, list  transform values within transform property one after other without use of commas.

Using multiple transform declarations will not work, as each declaration will overwrite the one above it. Behavior in that case would be same as if you were to set height of element numerous times.

Behind every transform there is matrix explicitly defining behavior of transform. Using rotate, scale, transition, and skew values provide easy way to establish matrix.

Default transform origin is dead center of element, both 50% horizontally and 50% vertically. To change this default origin position transform-origin property may be used.

Transform-origin property can accept one or two values. When only one value specified, value used for both horizontal and vertical axis. If two values specified, first used for horizontal axis and second used for vertical axis.

Individually values treated like background image position, using either length or keyword value. 0, 0 is same value as top left, and 100%, 100% is same value as bottom right. More specific values can be set, for ex. 20px 50px would set origin to 20 pixels across and 50 pixels down element.

Tansform-origin property does run into issues when also using translate transform value. Since both of are attempting to position element, values can collide. Use two of these with caution, always checking to ensure desired outcome is achieved.

In order for three-dimensional transforms to work elements need perspective from which to transform. Perspective for each element can be thought as vanishing point.

The perspective of element can be set in two ways. 1) Using perspective value within transform property on individual elements, while other includes using perspective property on parent element residing over child elements being transformed.

Using perspective value within transform property works great for transforming one element from a single, unique perspective. If you want to transform group of elements, all with same perspective, or vanishing point, apply perspective property to parent element.

Perspective value can be set as none or length measurement. None value turns off any perspective, while length value will set depth of perspective. Higher the value, further away perspective appears, thus creating fairly low intensity perspective and small three-dimensional change. Lower the value the closer perspective appears, thus creating high intensity perspective and large three-dimensional change.

Transform-origin can also set perspective-origin. Same values used for transform-origin property also used with perspective-origin property, and maintain same relationship to element. The large difference between the two falls where the origin of transform determines coordinates used to calculate change of transform, while origin of perspective identifies coordinates of vanishing point of transform.

Three-dimensional transforms can rotate element around any axis. Use three new transform values: rotateX, rotateY, and rotateZ.

Using rotateX value allows to rotate element around x axis. RotateY value allows to rotate element around y axis. Using rotateZ value allows element to be rotated around z axis.

Positive values will rotate the element around its dedicated axis clockwise, negative values will rotate element counterclockwise.

By using scaleZ three-dimensional transform elements may be scaled on the z axis.

Elements can also be translated on z axis using translateZ value. Negative value here will push element further away on z axis, resulting in smaller element. Using positive value will pull element closer on z axis, resulting in larger element.

Transform is taking place on z axis, not x or y axis. When working with 3d transforms, being able to move element on z axis has benefits.

Skew is the one two-dimensional transform that cannot be transformed on three-dimensional scale. Elements may be skewed on x and y axis, then transformed three-dimensionally, but cannot be skewed on z axis.

Shorthand properties include rotate3d, scale3d, transition3d, and matrix3d. Properties do require more math.

On occasion three-dimensional transforms will be applied on element that is nested within parent element which is also being transformed. In this event, nested, transformed elements will not appear in their own three-dimensional space. To allow nested elements to transform in their own three-dimensional plane, use transform-style property with preserve-3d value.

The transform-style property needs to be placed on parent element, above any nested transforms. The preserve-3d value allows transformed children elements to appear in their own three-dimensional plane while flat value forces transformed children elements to lie flat on two-dimensional plane.

When working with three-dimensional transforms, elements will occasionally be transformed in way that causes them to face away from screen. May be caused by setting rotateY(180deg) value for example. By default elements are shown from back. So if you prefer not to see these elements at all, set the backface-visibility property to hidden, and will hide element whenever it is facing away from screen.

Other value to backface-visibility is visible which is default value, & always displaying element.

_<a href = "https://learn.shayhowe.com/advanced-html-css/transitions-animations/">"Transitions & Animations"</a>_

One evolution with CSS3 was ability to write behaviors for transitions and animations. Front end developers have been asking for ability to design these interactions within HTML and CSS, without use of JavaScript or Flash.

With CSS3 transitions you have potential to alter appearance and behavior of element whenever state change occurs.

Animations within CSS3 allow appearance and behavior of element to be altered in multiple keyframes. Transitions provide change from one state to another, while animations can set multiple points of transition upon different keyframes.

For a transition to take place, element must have change in state, and different styles must be identified for each state. Easiest way to determining style for different states is by using the :hover, :focus, :active, and :target pseudo-classes.

There are four transition related properties total: transition-property, transition-duration, transition-timing-function, and transition-delay.

Transition-property property determines exactly what properties will be altered in conjunction with other transitional properties. Default, all properties within element’s different states will be altered upon change. Only properties identified within transition-property value will be affected by any transitions.

If multiple properties need to be transitioned there may be comma separated within the transition-property value. Additionally, the keyword value all may be used to transition all properties of element.

Not all properties may be transitioned, only properties that have an identifiable halfway point. Colors, font sizes, and the like may be transitioned from one value to another as they have recognizable values in-between one another. The display property, for example, may not be transitioned as it does not have any midpoint. 

Popular transitional properties include the following:
background-colorbackground-positionborder-colorborder-widthborder-spacingbottomclipcolorcropfont-sizefont-weightheightleftletter-spacingline-heightmarginmax-heightmax-widthmin-heightmin-widthopacityoutline-coloroutline-offsetoutline-widthpaddingrighttext-indenttext-shadowtopvertical-alignvisibilitywidthword-spacingz-index

The duration in which a transition takes place is set using the transition-duration property. The value of this property can be set using general timing values, including seconds (s) and milliseconds (ms). These timing values may also come in fractional measurements, .2s for example.

When transitioning multiple properties can set multiple durations, one for each property. Multiple durations can be declared using comma separated values. Order of these values when identifying individual properties and durations does matter. Ex. first property identified within transition-property property will match up with first time identified within the transition-duration property.

If multiple properties being transitioned with only one duration value declared, that one value will be duration of all transitioned properties.

The transition-timing-function property is used to set speed in which transition will move. Knowing the duration from transition-duration property a transition can have multiple speeds within single duration. Popular keyword values for transition-timing-function property include linear, ease-in, ease-out, and ease-in-out.

Linear keyword value identifies transition moving in constant speed from one state to another. The ease-in value identifies transition that starts slowly and speeds up throughout transition, while ease-out value identifies transition that starts quickly and slows down throughout transition. The ease-in-out value identifies transition that starts slowly, speeds up in middle, then slows down before ending.

Each timing function has a cubic-bezier curve behind it, which can be specifically set using the cubic-bezier(x1, y1, x2, y2) value. Additional values include step-start, step-stop, and a uniquely identified steps(number_of_steps, direction) value.

When transitioning multiple properties, can identify multiple timing functions. These timing function values, may be declared as comma separated values.

On top of declaring transition property, duration, and timing function, can also set delay with transition-delay property. Delay sets time value, seconds or milliseconds, that determines how long transition should be stalled before executing. To delay numerous transitions, each delay can be declared as comma separated values.

Declaring every transition property individually can become quite intensive. There is shorthand property, transition, capable of supporting all different properties and values. Using the transition value alone, can set every transition value in order of transition-property, transition-duration, transition-timing-function, and transition-delay. Do not use commas with these values unless you are identifying numerous transitions.

To set numerous transitions at once, set each individual group of transition values, then use a comma to separate each additional group of transition values.

To set multiple points at which element should undergo transition, use @keyframes rule. The @keyframes rule includes animation name, any animation breakpoints, and properties intended to be animated.

The different keyframe breakpoints set using percentages, starting at 0% and working to 100% with intermediate breakpoint at 50%. The keywords from and to could be used in place of 0% and 100%. Additional breakpoints, besides 50%, may be stated. The element properties to be animated are listed inside each of the breakpoints, left and top in the example above.

Only individual properties may be animated. Trying to animate from top: 0; to bottom: 0; will not work, because animations can only apply a transition within single property, not from one property to another. In this case, element will need to be animated from top: 0; to top: 100%;.

Once the keyframes for an animation have been declared they need to be assigned to element. To do so, animation-name property is used with animation name, identified from the @keyframes rule, as property value. The animation-name declaration is applied to element in which the animation is to be applied to.

You also need to declare an animation-duration property and value so that browser knows how long animation should take to complete.

Once you declared the animation-name property on element, animations behave similarly to transitions. They include duration, timing function, and delay. To start, animations need a duration declared using the animation-duration property. The duration may be set in seconds or milliseconds.

Timing function and delay can be declared using animation-timing-function and animation-delay properties respectively. Values for these properties mimic and behave like transitions.

Animations also provide ability to further customize element’s behavior, including ability to declare number of times animation runs, as well as direction in which animation completes.

Default, animations run their cycle once from beginning to end and then stop. To have animation repeat itself numerous times, animation-iteration-count property may be used. Values for animation-iteration-count property include either integer or infinite keyword. Using integer will repeat animation as many times as specified, while infinite keyword will repeat animation indefinitely in never ending fashion.

While being able to set the number of times animation repeats, may also declare direction animation completes using animation-direction property. Values for animation-direction property include normal, reverse, alternate, and alternate-reverse.

The normal value plays animation as intended from beginning to end. The reverse value will play the animation exactly opposite as identified within the @keyframes rule.

Alternate value will play animation forwards then backwards. Within the keyframes that includes running forward from 0% to 100% and then backwards from 100% to 0%. Using the animation-iteration-count property may limit the number of times animation runs both forwards and backwards. The count starts at 1 running animation forwards from 0% to 100%, then adds 1 running animation backwards from 100% to 0%. Combining for total of 2 iterations. The alternate value also inverses any timing functions when playing in reverse. If animation uses the ease-in value going from 0% to 100%, it then uses the ease-out value going from 100% to 0%.

Alternate-reverse value combines both alternate and reverse values, running animation backwards then forwards. Alternate-reverse value starts at 100% running to 0% and then back to 100% again.

Animation-play-state property allows animation to be played or paused using running and paused keyword values respectively. When you play paused animation, will resume running from its current state rather than starting from beginning again.

Animation-fill-mode property identifies how element should be styled either before, after, or before and after animation is run. The animation-fill-mode property accepts four keyword values, including none, forwards, backwards, and both.

None value will not apply any styles to element before or after animation has been run.

Forwards value will keep styles declared within the last specified keyframe. These styles may, however, be affected by animation-direction and animation-iteration-count property values, changing exactly where an animation ends.

Backwards value will apply styles within first specified keyframe as soon as being identified, before the animation has been run. This does include applying those styles during any time that may be set within animation delay. The backwards value may also be affected by the animation-direction property value.

Both value will apply the behaviors from both the forwards and backwards values.

Animations can be written out in shorthand format. Accomplished with one animation property, rather than multiple declarations. The order of values within animation property should be animation-name, animation-duration, animation-timing-function, animation-delay, animation-iteration-count, animation-direction, animation-fill-mode, and lastly animation-play-state.

_<a href = "https://www.webdesignerdepot.com/2014/05/8-simple-css3-transitions-that-will-wow-your-usersa ">"8 Simple CSS3 Transitions that will wow your Users"</a>_

Here are 8 really simple effects that to add to your UI.

All of these effects, except 1, are controlled with the transition property.

Transition property has three values: properties to transition, speed of the transition, & third value which lets you change how acceleration and deceleration is calculated.

Fade in: Fade in effects are coded in two steps: 1) set initial state; 2) set the change, for example on hover:

Change Color: Set the div’s class to “color” and specify the color we want in our CSS.

Grow & shrink: Set your div’s class to “grow”, then add this code to your style block:

.grow:hover

{

        -webkit-transform: scale(1.3);

        -ms-transform: scale(1.3);

        transform: scale(1.3);

}

Shrinking an element: To enlarge element we specify value greater than 1, to shrink, we specify a value less than 1.

Rotate Elements: Give your div the class “rotate” and add the following to your CSS:

.rotate:hover

{

        -webkit-transform: rotateZ(-30deg);

        -ms-transform: rotateZ(-30deg);

        transform: rotateZ(-30deg);

}

Square to Circle: Transition the border-radius property. Give your div the class “circle” and add this CSS to your styles:

.circle:hover

{

        border-radius:50%;

}

3D Shadow: Effect is achieved by adding box shadow, then moving element on x axis using transform and translate properties so it appears to grow out of screen. Give your div the class “threed” and then add the following code to your CSS:

.threed:hover

{

        box-shadow:

                1px 1px #53a7ea,

                2px 2px #53a7ea,

                3px 3px #53a7ea;

        -webkit-transform: translateX(-3px);

        transform: translateX(-3px);

}

Swing: can create animations using @keyframes, animation and animation-iteration. First define CSS animation in styles. Animation moves the element left and right.

Inset Border: Ghost button; button with no background and heavy border. Can add border to element, but will change element’s position. Could fix that using box sizing, but a simpler solution is transition in border using an inset box shadow. Give div class “border” and add following CSS to your styles:

.border:hover

{

        box-shadow: inset 0 0 0 25px #53a7ea;

}

_<a href = "https://codepen.io/retyui/pen/ByoaXV">"6 Buttons Animated"</a>_

Follow link to view code.

_<a href = "https://codepen.io/akshaychauhan/pen/oAfae">"CSS3 Keyframes Animation"</a>_

Follow link to view code.

_<a href = "https://codepen.io/kieranfivestars/pen/MYdQxX">"404"</a>_

Follow link to view code.

_<a href = "https://codepen.io/dp_lewis/pen/gCfBv">"Pure CSS Bounce Animation"</a>_

Follow link to view code.

_<a href = "https://www.nytimes.com/2016/02/28/magazine/what-google-learned-from-its-quest-to-build-the-perfect-team.html">"What Google learned from its quest to build the perfect team"</a>_

Google started 'Project Aristotle' to find what made the best teams. The researchers concluded that understanding and influencing group norms were the keys to improving Google’s teams.

Group norms: Norms are the traditions, behavioral standards and unwritten rules that govern how we function when we gather. Norms can be unspoken or openly acknowledged, but their influence is often profound. When they gather, the group’s norms typically override individual proclivities and encourage deference to the team.

Researchers wanted to know if there is a collective I.Q. that emerges within a team that is distinct from the smarts of any single member. the researchers recruited 699 people, divided them into small groups and gave each a series of assignments that required different kinds of cooperation. Teams that did well on one assignment usually did well on all the others. Conversely, teams that failed at one thing seemed to fail at everything.

First, on the good teams, members spoke in roughly the same proportion, a phenomenon the researchers referred to as ‘‘equality in distribution of conversational turn-taking’’.

Second, the good teams all had high ‘‘average social sensitivity’’ — a fancy way of saying they were skilled at intuiting how others felt based on their tone of voice, their expressions and other nonverbal cues.

Psychological safety is ‘‘a sense of confidence that the team will not embarrass, reject or punish someone for speaking up’’.

**<a href = "https://github.com/scottie-l/reading-notes/blob/main/reading-notes-201/README.md">Back</a>**
