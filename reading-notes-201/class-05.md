# Notes - Day 5

_Ch.5 "Images"_

Images should be: relevant, Convey information, correct mood, instantly recognizable and fit color palette.

Stock photos: istock photo, getty images, veer, fotolia, and sxc.hu

Images often stored in their own folder.

To add images use `<img>` tag with 2 attributes. `<src>` which is the path to image. `<alt>` text description of image if you can't see it. Can also add `<title>` tag which provides additional information about image.

Can also use height or width to specify size of image.

3 areas to place image: before p tag, where text will start under image. Inside start of p tag where image bottom aligns with text. Middle of p tag where image is placed between the words its placed between.

Align: Takes horizontal values left and right. Can also use top to align text with top of image. Middle is 1st line of surrounding text with middle of image. Bottom aligns text with bottom of image.

3 rules to create image: 1) save in the right format. 2) save image at right size. 3) measure image im pixels.

Format: JPEG: use when lots of different colors. GIF use with flat colors, or few colors, like logos.

Use `<figure>`  tag to add an image & `<figcaption>` tag inside figure tag to add text about image.

_Ch.11 "Color"_

Color: uses 3 types= RGB values, Hex code, Color names.

Color= text color, background-color= background

RGBA uses A or alpha for opacity. CSS uses last rule, so list RGB, hex, or color value then RGBA. Will use the RGBA value if it can, but older OS will use RGB.

HSL colors: made up of Hue (color), Saturation (amount of grey), Lightness (amount of black or white). Also has alpha value. (HSLA)

_Ch.12 "Text"_

Font-family= Generic fonts to licensed fonts. Serif is most generic, with times & Georgia less so. So start with most specific you want to use and end with most generic. Ex. font-family: Georgia, Times, Serif.

font-size: Use pixels or % to make size of text. Pixels is safest and most common.
Use font-face: this will install the font onto users system. Must have license to do so.

font-weight: normal, & bold, which makes text bold.

font-style: normal, & italic for italic text, & oblique for oblique text.

text-transform: `<uppercase>` all to uppercase, & `<lowercase>` all to lowercase, & `<capitalize>`: 1st letter of each word capitalized.

text=decoration: none, underline, overline, line-through & blink, which causes text to flash.

line-height: used to create space between text vertically. Best to use `<em>` for line height.

letter-spacing: the gap between each word.

word-spacing: gap between each word.

text-align; left, right, center, & justify= all lines take up full width except last line.

vertical align: used with inline elements.

text-indent: Used to indent text. Can be negative value to push off screen.

_<a href = "https://blog.imagekit.io/jpeg-vs-png-vs-gif-which-image-format-to-use-and-when-c8913ae3e01d">Blog Post JPEG vs. PNG vs. GIF</a>_

JPEG, PNG, & GIF make up 95% of all images.

2 types of compression: Lossless- all data available to recreate image, & Lossy- no data available other than what was compressed.

JPEG is used for lots of color. like photos of scenery.

JPEG is lossy. Averages out colors of pixels which is why high contrast areas or text make this not ideal.

JPEG supports 16 million colors

PNG is used when transparency or text is needed.

PNG is lossless for sharp images, but takes up more space on disk.

PNG has 2 formats. PNG8 supports 256 colors, while PNG24 supports 16 million.

GIF is lossless but PNG has better compression, so GIF is used mainly for animations.

GIF supports 256 colors. 1 maybe set to transparency, reducing it to 255. Only GIF supports animation.

GIF is used for animations.

**<a href = "https://github.com/scottie-l/reading-notes/blob/main/reading-notes-201/README.md">Back</a>**
