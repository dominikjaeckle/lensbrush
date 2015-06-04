# Lensbrush

Lensbrush is a simple d3 plugin, which allows you to perform a selection based on a lens. You can initiate the lensbrush the same way as d3.svg.brush:   

```javascript
var brush = d3.svg.lensbrush();
```

Please note that the extent method returns an array which contains three values:

1.center x-value of the lens
2.center y-value of the lens
3.radius

```javascript
brush.extent();
```

In order to test if a specific point lies within the lens, you can use the following method, which expects a x- and y-value:

```javascript
if (brush.isWithinLens(x, y)) {
	console.log(“Within the lens: (”, x, y, “)”);
}
```

## Usage

- **Create a new lens:** Press and hold the left mouse button. Moving the mouse will change the radius of the lens. Release the mouse button to conclude your selection.
- **Relocate the lens:** Drag and drop the lens. 
- **Resize the lens:** Position the mouse on the border of the lens. Press and hold the left mouse to change the radius. Release the mouse button to conclude your selection.
- **Delete the lens:** Click somewhere outside the lens.

## Files

The file d3.lensbrush.js contains the plugin and the file lens.html contains a simple example on how to use the plugin. 