---
tags: []
alias: [Longform notes]
cssclass: [cards, cards-cover]
banner_icon: 📘
---

# Longform notes

> [!tip] 
> This is a wiki, or "evergreen notes", or simply *long-term notes*.

---
## *latest pages*
```dataviewjs
dv.table(["Node","Created"], dv.pages('"00 Longform notes"')
	.where(b => b.id)
    .sort(b => b.file.mtime, 'desc')
	.limit(21)
    .map(b => [
    	"#### [["+b.file.name+"|"+b.title+"]]",
	"- **"+b.file.folder.replace("00 Bilinear notes/","")+"**: "+b.file.link+
	"\n- **created**: "+moment(b.created).format("D MMM yyyy hh:ss a") 
	//+"<li>Last modified: "+moment(b.updated).format("D MMM yyyy hh:ss a")
	//+"<li>Size: "+b.file.size+"<li>ID: "+b.id
	//+"<li>"+b.desc
			]))
```

> Note: the new note template for this folder is [[% new longform]]