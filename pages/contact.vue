<template>
	<div>
		<h1>
			Contact
		</h1>

		<div>
			<form name="contact" action="" method="post" netlify>

				<input type="hidden" name="form-name" value="contact">

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
