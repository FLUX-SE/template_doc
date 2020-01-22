# 1. Login to github
Then, go to https://github.com/FLUX-SE

# 2. Create repository
Create a new repository called "<plugin_name>_doc"

# 3. Add mandatory files
## Option 1 (recommended) :
Copy the files from https://github.com/FLUX-SE/template_doc

## Option 2 :
Add a file named ".gitignore" containing:
```
.idea/
.vs*/
```

Add empty file named ".nojekyll"

Add a file named "index.html" containing:
```<!-- index.html -->

<!DOCTYPE html>
<html>
<head>
  <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <meta charset="UTF-8">
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/docsify-themeable@0/dist/css/theme-simple-dark.css">
  <style>
    .sidebar-nav a::before
    {
      content: "" !important;
      margin: auto;
    }
    :root
    {
      --table-row-even-background: hsl(201, 18%, 13%)/*var(--mono-shade3)*/
    }
  </style>
</head>
<body>
  <div id="app"></div>
  <script>
    window.$docsify = {
      name: 'Flux:: Documentation',
      loadSidebar: true,
      alias: {
        '/_sidebar.md': '/sidebar.md'
      },
      subMaxLevel: 4,
      homepage: 'documentation/<NAME_OF_THE_HOMEPAGE>.md',
      auto2top: true
    }
  </script>
  <script src="https://unpkg.com/docsify/lib/docsify.min.js"></script>
</body>
</html>
```

Add a file named "sidebar.md" with links to your pages :
```
[Page Name](/documentation/PAGE_NAME.md)
```

# 4. Create documentation
If you are converting an existing documentation, here are useful links :
- pdf2md (https://pdf2md.morethan.io/) - Makes a big part of the job when converting from pdf to markdown (still need to fix details)
- Python scripts (https://github.com/FLUX-SE/scripts_doc):
    - _split_into_md_files : To split a big markdown documentation into smaller files in a tree organization based on titles
    - _generate_sidebar : Generates the sidebar based on files in documentation/ folder

Then, you need to write documentation or fix details of the converted one in markdown:

https://guides.github.com/features/mastering-markdown/

You can write markdown using PyCharm, it's very easy.

If you have images :
- Add image into the include/ folder
- Add it to file like this : 
```
 ![](/include/image_name.png)    // If homepage. You won't see in in PyCharm but it is needed for Github
 ![](../include/image_name.png)  // Else 
```

![](/include/flux-logo.png)

# 5. Create GitHub Page

When you are done, push to GitHub

Go to **settings**

Scroll to **GitHub Pages** 

In **Source**, select **master branch**

Wait and refresh until the page is ready

![](/include/done.PNG)