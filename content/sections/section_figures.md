# Inserting Figures in markdown

## Directly inline (quick insert)
Use:

`![Alt Image Text](path/or/url/to.jpg "Optional Title")`

## Using a reference style
Use:

`![Alt Image Text][image-id]`  

with the ``image-id`` defined on its own line elsewhere:

`[image-id]: path/or/url/to.jpg "Optional Title"`

## Using a reference style with control on image properties
Use:

```rst
:::{figure-md} ArgoFloat-cycle
<img src="/images/float_cycle_2_credits.png" alt="Argo floats cycle" class="mb-1" width="400px">

Illustration of the Argo float cycling program at sea.
:::
```

Here you note that you can control much more parameters of the insertion. The main advantage of this method is that you can use a reference to this figure anywhere in the documentation, not only this file.

You can then refer to the figure by its number using the definition keyword, eg: see {numref}`ArgoFloat-cycle`. This ref was coded like:
```
eg: see {numref}`ArgoFloat-cycle`
```

This method would render like this:

:::{figure-md} ArgoFloat-cycle
<img src="/images/float_cycle_2_credits.png" alt="Argo floats cycle" class="mb-1" width="400px">

Illustration of the Argo float cycling program at sea.
:::
