notebook-styles
===============

A repo to hold various IPython notebook CSS files. Most of this was inspired by @nsonnad's [base16-ipython-notebook repo](https://github.com/nsonnad/base16-ipython-notebook). 

`custom.css` should be placed in your .ipython custom config at `~/.ipython/profile_default/static/custom/custom.css`, and will be the default style for all of your notebooks. Note that most of the styling happens via the CodeMirror CSS. 

For nbviewer, these styles need to be converted into `.highlight` selectors. Most of the style names (builtin, literal integer, etc) match 1:1, but there is some trial and error getting the color palette to match the CodeMirror styling. The static CSS can be loaded in nbviewer with the following code (using the correct relative path): 

```python
from IPython.core.display import HTML
styles = open("styles/custom.css", "r").read()
HTML(styles)
```

See an example of this in the [bearcart example directory](https://github.com/wrobstory/bearcart/tree/master/examples). 

I've included both `custom.css` and `nbviewer.css` in this repo to show how I've mapped one to the other.  
