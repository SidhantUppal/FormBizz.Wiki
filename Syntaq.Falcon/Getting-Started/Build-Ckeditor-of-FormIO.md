**Intro**

Ckeditor is an optional editor of TextArea component of Formio, it can be customized to have different coverage of features, such as image upload, heading levels, font styles, etc. This document is to introduce how to customize and implement it in Dev environment. 

**Step 1**

Visit [https://ckeditor.com/ckeditor-5/online-builder/](), choose the editor type, which at the moment is Classic Editor: 

![image.png](/.attachments/image-13f42a02-d836-411b-b50d-93d7a9404506.png)

**Step 2**

Select required plgins or features in other word, below is the required plugins at the moment: 

1.Undo
2.Redo
3.Heading
4.Font family
5.Font size
6.Bold
7.Italic
8.Underline
9.Strikethrough
10.Special Charaters
11.List(Bulleted list and numbered list)
12.Alignment
13.Indent(Decrease and increase)
14.Table
15.Image(Image and Image Upload)  ** Require Base64 upload adapter plugin
16.Link
17.Block quote
18.Find and replace
19.Remove format
20.Source

Also in the bulder as below: 

![image.png](/.attachments/image-65571001-28a8-402e-ab0f-a096dd24c1df.png)

**Step 3**

Drag the selected plugins from Available items to Picked items as below: 

![image.png](/.attachments/image-040aa631-729b-4db1-b177-3e0417986ba1.png)

**Step 4**

Choose the default editor language, which at the moment is English Australia: 

![image.png](/.attachments/image-3400934d-456a-46cb-b17b-4109d40601df.png)

**Step 5**

Start builiding the sample editor and download the package

**Step 6**

Extract the downloaded package and go to folder: build, and copy the codes in ckeditor.js paste in our assets/ckeditor/ckeditor.js, gulp build and refresh the form page. 
