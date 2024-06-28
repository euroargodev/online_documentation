# Links and bibliography in markdown

## Links and Email

### Inline
Just put angle brackets around an email and it becomes clickable: <contact@euro-argo.eu>  
`<contact@euro-argo.eu>`  

Same thing with urls: <https://github.com/euroargodev>  
` <https://github.com/euroargodev>`  

Perhaps you want to some link text like this: [Euro-Argo Dev Website](https://github.com/euroargodev "Title")  
`[Euro-Argo Dev Website](https://github.com/euroargodev "Title")` (The title is optional)  


### Reference style
Sometimes it looks too messy to include big long urls inline, or you want to keep all your urls together.  

Make [a link][arbitrary_id] `[a link][arbitrary_id]` then on its own line anywhere else in the file:

`[arbitrary_id]: https://github.com/euroargodev "Title"`
  
If the link text itself would make a good id, you can link [like this][] `[like this][]`, then on its own line anywhere else in the file:  

`[like this]: https://github.com/euroargodev`  

[arbitrary_id]: https://github.com/euroargodev "Title"
[like this]: https://github.com/euroargodev 


### Bibliography

It is possible to include a bibliography with the `bib` format, and add references in the documentation. The {numref}`section-biblio` will automatically be filled.

For instance, talking about a software, it is important to cite the corresponding paper like {cite:t}`maze-2020`.

Add new references in the `biblio.bib` file.
