# Sample

Click on the image for full scale screenshot.

**Warning:** really big image file.

[![](http://i.imgur.com/jwBDM8Dl.png)](http://i.imgur.com/jwBDM8D.png)

# Code
```python
import sark.qt

widget = sark.qt.get_widget("IDA View-A")
sark.qt.resize(widget, 7000, 18000)

# Move the view about a bit to capture the entire function

sark.qt.capture_widget(widget, "huge-screenshot.png")

# Crop the image to remove extra background.
```