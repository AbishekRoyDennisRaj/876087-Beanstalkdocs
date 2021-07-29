---
layout: post
title: Feature Module in Blazor PDF Viewer Component | Syncfusion 
description: Learn about Feature Module in Blazor PDF Viewer component of Syncfusion, and more details.
platform: Blazor
control: PDF Viewer
documentation: ug
---

# Feature modules

The PDF Viewer features are segregated into individual feature-wise modules to enable selectively referencing in the application. The required modules should be injected to extend its functionality. The following are the selective modules of PDF Viewer that can be included as required:

The available PdfViewer modules are:

* **Toolbar**:- Built-in toolbar for better user interaction.
* **Magnification**:- Perform zooming operation for better viewing experience.
* **Navigation**:- Easy navigation across the PDF pages.
* **LinkAnnotation**:- Easy navigation within and outside of the PDF document.
* **ThumbnailView**:- Easy navigation with in the PDF document.
* **BookmarkView**:- Easy navigation based on the bookmark content of the PDF document.
* **TextSelection**:- Select and copy text from a PDF file.
* **TextSearch**:- Search a text easily across the PDF document.
* **Print**:- Print the entire document or a specific page directly from the browser.
* **Annotation**:- Annotations can be added or edited in the PDF document.

>In addition to injecting the required modules in your application, enable corresponding properties to extend the functionality for a PDF Viewer instance.
Refer to the following table.

| Module | Property to enable the functionality for a PDF Viewer instance |
|---|---|
|Toolbar|`<EjsPdfViewer enableToolbar= "true" ></EjsPdfViewer>`|
|Magnification|`<EjsPdfViewer enableMagnification= "true" ></EjsPdfViewer>`|
|Navigation|`<EjsPdfViewer enableNavigation= "true" ></EjsPdfViewer>`|
|LinkAnnotation|`<EjsPdfViewer enableHyperlink= "true" ></EjsPdfViewer>`|
|ThumbnailView|`<EjsPdfViewer enableThumbnail= "true" ></EjsPdfViewer>`|
|BookmarkView|`<EjsPdfViewer enableBookmark= "true" ></EjsPdfViewer>`|
|TextSelection|`<EjsPdfViewer enableTextSelection= "true" ></EjsPdfViewer>`|
|TextSearch|`<EjsPdfViewer enableTextSearch= "true" ></EjsPdfViewer>`|
|Print|`<EjsPdfViewer enablePrint= "true" ></EjsPdfViewer>`|
|Annotation|`<EjsPdfViewer enableAnnotation= "true" ></EjsPdfViewer>`|

## See also

* [Toolbar items](./toolbar)
* [Toolbar customization](./how-to/toolbar-customization)