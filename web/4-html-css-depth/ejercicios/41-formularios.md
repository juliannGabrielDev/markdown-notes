# Entrada de usuario y formularios
#html #sintaxis #ejercicios

---
## Crear un formulario
```html
<form>
    <div>
        <label for="user_name">Nombre: </label>
        <input type="text" id="user_name" name="user_name" minlength="2" required>
    </div>
    <div>
        <label for="user_password">Contraseña: </label>
        <input type="password" id="user_password" name="user_password" minlength="12" required>
    </div>
    <button type="submit">Log in</button>
</form>
```
## Elementos de formulario interactivos
```html
<form method="POST">
    <div>
        <label for="booking_date">Booking date</label>
        <input type="date" id="booking_date" name="booking_date">
    </div>
    <div>
        <label for="booking_people">Number of people</label>
        <input type="range" id="booking_people" name="booking_people" min="1" max="10" value="4" oninput="this.nextElementSibling.value = this.value">
        <output>4</output>
    </div>
    <div>
        <label for="booking_location">Location</label>
        <input list="locations" id="booking_location" name="booking_location">
        <datalist id="locations">
            <option value="Downtown"></option>
            <option value="Updown"></option>
        </datalist>
    </div>
    <button type="submit">Book table</button>
</form>
```