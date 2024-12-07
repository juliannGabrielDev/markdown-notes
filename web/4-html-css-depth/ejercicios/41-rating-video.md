# Valore el video

En este ejercicio, creará una página web para clasificar un vídeo. La página mostrará un reproductor de vídeo con controles de reproducción. También habrá un formulario HTML para calificar el vídeo. El formulario contendrá un elemento deslizante para valorar el vídeo entre 1 sobre 5 y 5 sobre 5.
```html
<video controls width="320" height="240">
	<source src="video.mp4" type="video/mp4">
</video>

<form>
	<div>
		<label for="rating">Rating</label>
		<input type="range" min="1" max="5" id="rating" name="rating" list="ratings">
		<datalist id="ratings">
			<option value="1" label="1"></option>
			<option value="2"></option>
			<option value="3"></option>
			<option value="4"></option>
			<option value="5" label="5"></option>
		</datalist>
	</div>
	<button type="submit">Submit Rating</button>
</form>
```
