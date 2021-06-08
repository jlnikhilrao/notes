# Usage and quirks of django FielField and ImageField

- There is kwarg `save=False` used in an article https://python.plainenglish.io/generating-barcodes-with-django-52e450fd960b.

  - https://stackoverflow.com/questions/25407982/django-filefield-in-model-maximum-recursion-depth-exceeded-while-calling-a-pytho/25408209#25408209 
explains why when saving a `FileField` automatically saves the django Model instance as well.

  - Since `ImageField` is inherited from FileField the same thing happens here.
  - Alternatively we can also use a condition to check if the field is populated by using a simple `if` block

- Below link has a little more info on how to use `ImageField`
  - https://stackoverflow.com/a/1309682
