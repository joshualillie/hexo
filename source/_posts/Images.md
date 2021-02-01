---
title: Images
date: 2021-01-31 09:05:00
tags:
---
I have very primitive markdown knowledge, and need to practive using it some (or a lot). 

!["Pop!"](/images/laquerhead.jpg)

Let's see if this one renders smaller.

!["Smaller Pop"](/images/laquerhead.jpg) =200x

Ok... that one didn't seem to work.. how about we try embedding some HTML in our Markdown.

Let's try...

```html
<img src="/images/laquerhead.jpq" style="width:100px" >
<br>
<img src="/images/laquerhead.jpq" style="width:200px" >
```
<img src="/images/laquerhead.jpq" style="width:100px" >
<br>
<img src="/images/laquerhead.jpq" style="width:200px" >

How about a simple HTML Table?

<table>
  <thead>
    <tr><th>#</th><th>Name</th></tr>
  </thead>
  <tbody>
    <tr><td>1</td><td>Mercury</td></tr>
    <tr><td>2</td><td>Venus</td></tr>
    <tr><td>3</td><td>Earth</td></tr>
    <tr><td>4</td><td>Mars</td></tr>
    <tr><td>5</td><td>Jupiter</td></tr>
    <tr><td>6</td><td>Saturn</td></tr>
    <tr><td>7</td><td>Uranus</td></tr>
    <tr><td>8</td><td>Neptune</td></tr>
  </tbody>
</table>

How does it look?