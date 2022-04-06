---
title: "Activity History"
status: 🌱🪴🌲🍇
words:
tags:
---
```ActivityHistory
/

```
What I want to create with this tool
Show world count on mouse hover
Rearrange the thing so it can show yearly and monthly if possible.
also on early one there should be some shading to show different months so you know where the boundaries are.

question: 
How and where do I start???

```dataviewjs
const calendarData = {
	entries: []
}
for(let page of dv.pages(). where(p=>p.words).sort(p=>p.file.name)){
	calendarData.entries.push({
		date: page.file.cday,
		intensity: page.words
	})


}
renderHeatmapCalendar(this.container, calendarData)

```

```dataviewjs
dv.span("**Words Activity**")

const calendarData = {
    entries: []
}

for(let page of dv.pages().where(p=>p.words).sort(p=>p.file.name)){
    calendarData.entries.push({
        date: page.file.cday,
        intensity: page.words
    })
       
}

renderHeatmapCalendar(this.container, calendarData)

```

tables
```dataviewjs
dv.table(["Title", "Words"], dv.pages()
	.sort(b => b.file.size)
	.map(b => [b.file.link, b.file.size]))


```