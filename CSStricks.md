# CSS Updates To Make Sure Widgets Drag Correctly #

Two important things to do here:
  1. Make sure the class that you gave the GWT widgets (in this case .window) has position: relative, so they drag properly when the connectors move.
  1. The z-index of the GWT widgets must be greater than that of what is specified for the jsPlumb connectors, otherwise they will prevent you from dragging the GWT widget underneath.


# gwtjsplumb.css #

```
.window {
	border: 1px solid black;
	height: 100px;
	width: 100px;
	position: relative;
	margin:10px;
	z-index:4000;
}

#window2 {
	left: 200px;
	top:10px;
}

#window4 {
	left: 200px;
	top:10px;
}

#window3 {
	height: 20px;
}
```