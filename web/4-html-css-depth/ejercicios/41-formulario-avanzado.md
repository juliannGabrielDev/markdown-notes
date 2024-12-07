```html
<form>
	<div>
		<label for="email_address">Email Address</label>
		<input type="email" id="email_address" name="email_address">
	</div>
	<div>
		<label for="booking_date">Date of Booking</label>
		<input type="date" id="booking_date" name="booking_date">
	</div>
	<div>
		<label for="people">Number of people</label>
		<input type="number" id="people" min="1" max="8" name="people">
	</div>
	<div>
		<label>
			<input type="checkbox" id="agree" name="agree" required>
			I agree to the cancellation policy
		</label>
	</div>
	<button type="submit">Book Now</button>
</form>
```