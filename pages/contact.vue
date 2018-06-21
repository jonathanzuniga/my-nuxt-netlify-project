<template>
	<div>
		<h1>
			Contact
		</h1>

		<div>
			<form name="contact" action="/thank-you" method="post" netlify netlify-honeypot="bot-field">

				<input type="hidden" name="form-name" value="contact">

				<p class="hidden">     
  					<label>Don’t fill this out: <input name="bot-field"></label>
  				</p>

				<p>
					<label for="name">
						Name:
					</label>
					<input name="name" id="name">
				</p>

				<p>
					<label for="email">
						Email:
					</label>
					<input name="email" id="email">
				</p>

				<p>
					<label for="message">
						Message:
					</label>
					<textarea name="message" id="message"></textarea>
				</p>

				<input type="submit" value="Send message">

			</form>
		</div>
	</div>
</template>

<style type="text/css">

	.hidden {
		display: none;
	}
	
</style>
