<script>
	import SwitchTheme from './switch/SwitchTheme.svelte';
	import Link from '$lib/components/link/Link.svelte';
	import Form from '$lib/components/form/Form.svelte';
	import Input from '$lib/components/form/Input.svelte';
	import Button from './button/Button.svelte';
</script>

<footer class="p-4 shadow md:p-6 bg-neutral-900 text-neutral-50">
	<div class="flex flex-col items-center justify-center mb-8" id="mail-subscribe">
		<h1>Subscribe to our Mailing List</h1>
		<p>Get news on any big updates! Your info won't be used for anything else; we promise.</p>
		<!-- <Form bg="transparent" customClass="lg:w-1/2 w-full flex flex-row justify-center items-center">
			<Input type="email" name={null} placeholder="Email Address" id="email" />
			<Button type="submit" customClass="flex-auto ml-2">Subscribe!</Button>
		</Form> -->
		<div id="mc_embed_shell" class="w-full max-w-xl">
			<link
				href="//cdn-images.mailchimp.com/embedcode/classic-061523.css"
				rel="stylesheet"
				type="text/css"
			/>
			<div id="mc_embed_signup" class="m-0">
				<form
					action="https://gmail.us12.list-manage.com/subscribe/post?u=a9a82755ff66d6888b02e6475&amp;id=43133820e0&amp;f_id=006e48e0f0"
					method="post"
					id="mc-embedded-subscribe-form"
					name="mc-embedded-subscribe-form"
					class="validate m-0"
					target="_blank"
				>
					<div id="mc_embed_signup_scroll">
						<div class="pb-0 h-9 mb-4" style="width: 96%;">
							<input
								type="email"
								name="EMAIL"
								class="required email bg-neutral-600 w-full h-9"
								id="mce-EMAIL"
								required=""
								value=""
								placeholder="Email Address"
							/>
						</div>
						<div id="mce-responses" class="clear foot">
							<div class="response" id="mce-error-response" style="display: none;"></div>
							<div class="response" id="mce-success-response" style="display: none;"></div>
						</div>
						<div style="position: absolute; left: -5000px;" aria-hidden="true">
							/* real people should not fill this in and expect good things - do not remove this or
							risk form bot signups */
							<input
								type="text"
								name="b_a9a82755ff66d6888b02e6475_43133820e0"
								tabindex="-1"
								value=""
							/>
						</div>
						<div class="optionalParent">
							<div class="clear foot">
								<input
									type="submit"
									name="subscribe"
									class="subscribe bg-purple-700 hover:bg-purple-400 max-w-xs h-10 cursor-pointer"
									value="Subscribe"
								/>
								<p style="margin: 0px auto;">
									<a
										href="http://eepurl.com/iEKowE"
										title="Mailchimp - email marketing made easy and fun"
										><span
											style="display: inline-block; background-color: black; border-radius: 4px;"
											><img
												class="refferal_badge"
												src="https://digitalasset.intuit.com/render/content/dam/intuit/mc-fe/en_us/images/intuit-mc-rewards-text-light.svg"
												alt="Intuit Mailchimp"
												style="width: 220px; height: 40px; display: flex; padding: 2px 0px; justify-content: center; align-items: center;"
											/></span
										></a
									>
								</p>
							</div>
						</div>
					</div>
				</form>
			</div>
			<script
				type="text/javascript"
				src="//s3.amazonaws.com/downloads.mailchimp.com/js/mc-validate.js"
			></script><script type="text/javascript">
				(function ($) {
					window.fnames = new Array();
					window.ftypes = new Array();
					fnames[0] = 'EMAIL';
					ftypes[0] = 'email';
					fnames[1] = 'FNAME';
					ftypes[1] = 'text';
					fnames[2] = 'LNAME';
					ftypes[2] = 'text';
					fnames[3] = 'ADDRESS';
					ftypes[3] = 'address';
					fnames[4] = 'PHONE';
					ftypes[4] = 'phone';
					fnames[5] = 'BIRTHDAY';
					ftypes[5] = 'birthday';
				})(jQuery);
				var $mcj = jQuery.noConflict(true);
			</script>
		</div>
	</div>
	<div class="md:flex md:items-center md:justify-between">
		<span class="text-sm sm:text-center"
			>© {new Date().getFullYear()}
			<Link href="/">Cupkek Games</Link>. All Rights Reserved.
		</span>
		<ul class="flex flex-wrap items-center mt-3 text-sm sm:mt-0">
			<li class="mr-4 md:mr-6">
				<Link href="#">About</Link>
			</li>
			<li class="mr-4 md:mr-6">
				<Link href="#">Privacy Policy</Link>
			</li>
			<li class="mr-4 md:mr-6">
				<Link href="#">Terms of Service</Link>
			</li>
			<!-- <li class="mr-4 md:mr-6">
				<SwitchTheme />
			</li> -->
		</ul>
	</div>
</footer>

<style>
	#mc_embed_signup input {
		border: none;
	}
</style>
