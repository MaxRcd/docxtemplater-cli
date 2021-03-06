docxtemplater CLI (with Open Source Image Module)
==========================================
This fork of docxtemplater CLI includes the support for [open-docxtemplater-image-module](https://github.com/MaxRcd/open-docxtemplater-image-module).

Installation
------------
The package below includes a copy of docxtemplater and open-docxtemplater-image-module.
```
npm install -g docxtemplater-cli-open-image-module
```

Try it out
----------
Browse to folder 'examples' and run the following in your console
```
docxtemplater input.pptx data.json output.pptx
```

data.json file structure
------------------------
This is a simple JSON file. Assuming we are working on the template 'input.pptx' provided with this package in 'examples' folder, we write below JSON to replace tags in the template by their respective value.
```json
{
    "first_name": "John",
    "last_name": "Doe",
    "description": "He is awesome",
    "phone": "+4412345678",
    "picture": "johndoe.png"
}
```

As you can see we have included a picture of John Doe (johndoe.png). For this picture to be correctly rendered in the output, we must explicitly activate the Open Source Image Module [open-docxtemplater-image-module](https://github.com/MaxRcd/open-docxtemplater-image-module). Note that all images must be under the directory 'imageDir'.
```json
{
    "first_name": "John",
    "last_name": "Doe",
    "description": "He is awesome",
    "phone": "+4412345678",
    "picture": "johndoe.png",
    "config": {
      "modules": ["open-docxtemplater-image-module"],
      "imageDir": "."
    }
}
```

Template tags
-------------
More on how to write your templates in [docxtemplater documentation](http://docxtemplater.readthedocs.io/en/latest/tag_types.html).