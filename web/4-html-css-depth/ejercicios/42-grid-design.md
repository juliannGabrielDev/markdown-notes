# Crear un diseño de cuadrícula

---
```html
<div class="container">
	<header class="header"> Header </header>
	<main class="main"> Content </main>
	<div class="sidebar left"> Sidebar </div>
	<div class="sidebar right"> Sidebar </div>
	<footer class="footer"> Footer </footer>
</div>
```
```css
.container {
	display: grid;
	max-width: 900px;
	min-height: 50vh;
	grid-template-columns: 100%;
	grid-template-rows: auto auto 1fr auto auto;
	grid-template-areas: "header" "left" "main" "right" "footer";
}

  

@media (min-width: 440px) {
	.container {
		grid-template-columns: 150px 1fr 150px;
		grid-template-rows: auto 1fr auto;
		grid-template-areas: "header header header" "left main right" "footer footer footer";
	}
}

.header {
	grid-area: header;
	padding: 10px;
	background-color: black;
	color: #fff;
	text-align: center;
}

.main {
	grid-area: main;
	padding: 25px;
}

.left {
	grid-area: left;
	background-color: peachpuff;
}

.right {
	grid-area: right;
}

.footer {
	grid-area: footer;
	padding: 10px;
	background-color: black;
	color: #fff;
	text-align: center;
}

.sidebar {
	padding: 25px;
	background-color: darkcyan;
}
```