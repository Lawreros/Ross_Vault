Created from: https://talk.macpowerusers.com/t/finding-ghost-notes-in-obsidian/27545

```dataviewjs
let d = {}
function process(k, v) {
  Object.keys(v).forEach(function (x) {
    x = dv.fileLink(x);
    if (d[x]==undefined) { d[x] = []; }
	d[x].push(dv.fileLink(k));
  });
}
Object.entries(dv.app.metadataCache.unresolvedLinks)
	.filter(([k,v])=>Object.keys(v).length)
	.forEach(([k,v]) => process(k, v));
dv.table(["Non existing notes", "Linked from"],
         Object.entries(d).map(([k,v])=> [k, v.join(" • ")]))
```