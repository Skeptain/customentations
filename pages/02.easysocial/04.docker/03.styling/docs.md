---
title: Styling
taxonomy:
    category:
        - docs
---

**Joomla**: 3.7.2</br>
**EasySocial**: 2.0.19</br>
**Docker**: 2.0.6</br>

Styling is important since the docker looks a bit boring by default in my opinion. Therefor we have several possibilities. I prefer modern design and at the moment, gradients have a big comeback for material design. But if you like you can just change the color of the whole docker. Let's start with the background color. All things here are made by pure CSS so I assume you know where your custom.css for your template is to add the codes there.

To change the background color of the Docker use this:

```css
#es.es-docker {
	background: #045979; }
```

Replace this to your favorite color (FFFFFF for white / 000000 for black):

```css
045979
```

To have a cool looking gradient you can add this instead of the above one:

```css
#es.es-docker {
	background: #045979;  /* fallback for old browsers */
	background: -webkit-linear-gradient(to right, #1080aa, #045979);  /* Chrome 10-25, Safari 5.1-6 */
	background: linear-gradient(to right, #1080aa, #045979); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */ }
```

We want to make sure that it works for as much browsers as possible. That is what the lines are for. The first line is your background color in case the browser does not support gradient. The next lines are the gradients related to the browser the visitor is using. The first color is the left one and the second the right one. The gradient goes from left to right. To change the direction of your gradient replace the "to right" by "to left", "to bottom" or "to top".

Additionally I like that fact of having a big border below the docker. You should play around with it because it looks awesome.

```css
#es.es-docker {
border-bottom: 5px solid #f4ab00; }
```

Of course you can change the color the same way as before. If you want the whole package you can use it like this:

```css
#es.es-docker {
	background: #045979;  /* fallback for old browsers */
	background: -webkit-linear-gradient(to right, #1080aa, #045979);  /* Chrome 10-25, Safari 5.1-6 */
	background: linear-gradient(to right, #1080aa, #045979); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
	border-bottom: 5px solid #f4ab00; }
```

