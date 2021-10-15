<b>Ch.16 "Images"

Can control image size with height, width properties in CSS. Give each image an id or class & use its selector to adjust attributes.

Use float property with class/id & then it makes selectors easier to know what's going on/happening to it.

Images are inline elements by default. Change to block, then set margin-left/right to auto to center the image.

Background-image= place an image behind HTML element. Ex. background-image: url("images/pattern.gif");

Background-repeat, has 4 values; repeat= img repeated on both x & y axis. repeat-x= repeat img on X axis only (horizontal.) repeat-y= repeat img on Y axis only (vertical). no-repeat= image shown once, has 2 values: fixed, img stays in place. scroll= img moves up & down as user scrolls.

background-position= when not repeated, used to specify position in browser window; usually 2 values, x & y. If specify only 1, second value defaults to center.

Can set many states for same element. Called sprites.

Can specify gradient in CSS. First state background image for box & then provide alternatives.

To overlay text over image, use low contrast or place semi transparent background color behind text.

<b>Ch.19 "Practical Information"

Search Engine Optimization (SEO) - practice of trying to get site to appear nearer the top of search results. Often split between 2 techniques. On-page & Off page.

On page: Looking at keywords people will search for in text & HTML; alt text helps too. 7 Essential places to do this.

1) Page title 2) URL/Web address 3) Headings `<h1-6>` 4) Text= repeat keywords 2-3 times 5) Link-text= specific text in buttons, not just click here 6) image alt text 7) Page descriptions= live in the head element in a meta tag describing content of page.

Off Page is getting other sites to link to your page.

How to identify keywords & phrases: 1) Brainstorm 2) Organize 3) Research 4) Compare 5) Refine 6) Map 

Analytics: looking at how people found site, what they're looking at, & when they leave. i.e. Google Analytics
Overview page: number of visits, unique visits, page views, page visits, average time on site, date selectors, export

What visitors looking at on page, landing page, top exit page & bounce rate.

Where visitors are coming from.

<a href = "https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Client-side_web_APIs/Video_and_audio_APIs">"Video & Audio APIs"</a>

`<video>` & `<audio>` tags used to imbed video or audio into webpage.

Use with 'controls'. Without controls you get no playback options. Ex. `<video controls>` 

                `<source src = "rabbit320.mp4" type = "video/mp4>`

This is not good for cross-browsers.

Can use HTML5 spec= `<HTMLMediaElement>` with a play, pause, stop, etc. for controls.

<b>Ch.9 "Flash, video & Audio"

Animations or video files are all called flash.

Use .fla for flash files. Convert to support using .swf for conversion files using JavaScript files.

<a href="https://github.com/scottie-l/Reading-notes-201">Back</a>