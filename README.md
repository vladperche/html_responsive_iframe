# html_responsive_iframe
How TO - Responsive Iframe

## Step 1

Use a container element, like <div>, and add the iframe inside of it:

### Example
```
<div class="container">
  <iframe class="responsive-iframe" src="https://www.youtube.com/embed/tgbNymZ7vqY"></iframe>
</div>
```

## Step 2
Add CSS:
Add a percentage value for padding-top to maintain the aspect ratio of the container DIV.
The following example will create an aspect ratio of 16:9, which is the default aspect ratio of YouTube videos.

### Example 16:9 Aspect Ratio
```
.container {
  position: relative;
  overflow: hidden;
  width: 100%;
  padding-top: 56.25%; /* 16:9 Aspect Ratio (divide 9 by 16 = 0.5625) */
}

/* Then style the iframe to fit in the container div with full height and width */
.responsive-iframe {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
  width: 100%;
  height: 100%;
}
```

## Other aspect ratios:

### Example 4:3 Aspect Ratio
```
.container {
  padding-top: 75%; /* 4:3 Aspect Ratio */
}
```

### Example 3:2 Aspect Ratio
```
.container {
  padding-top: 66.66%; /* 3:2 Aspect Ratio */
}
```

### Example 8:5 Aspect Ratio
```
.container {
  padding-top: 62.5%; /* 8:5 Aspect Ratio */
}
```

### Example 1:1 Aspect Ratio (Height and Width is Always Equal)
```
.container {
  padding-top: 100%; /* 1:1 Aspect Ratio */
}
```
### Without Aspect Ratio
Remove the: padding-top
Add: height
```
.container {
  height: 100%;
 }
 ```
 