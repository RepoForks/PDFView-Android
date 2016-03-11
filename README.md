**Android PDFView** is a library which provides a fast PDFView component for Android, with ```animations```, ```gestures```, and ```zoom```. It's based on [VuDroid](https://code.google.com/p/vudroid/) for decoding the PDF file.

# Include PDFView in your layout

```xml
<com.joanzapata.pdfview.PDFView
        android:id="@+id/pdfview"
        android:layout_width="match_parent"
        android:layout_height="match_parent"/>
```

# Load a PDF file

```java
pdfView.fromAsset(pdfName)
    .pages(0, 2, 1, 3, 3, 3)
    .defaultPage(1)
    .showMinimap(false)
    .enableSwipe(true)
    .onDraw(onDrawListener)
    .onLoad(onLoadCompleteListener)
    .onPageChange(onPageChangeListener)
    .load();
```

* ```pages``` is optional, it allows you to filter and order the pages of the PDF as you need
* ```onDraw``` is also optional, and allows you to draw something on a provided canvas, above the current page

## License

```
The MIT License (MIT)

Copyright (c) 2016 TheFinestArtist, Joan Zapata

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
```