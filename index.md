<script type='text/javascript'>
	function initEmbeddedMessaging() {
		try {
			embeddedservice_bootstrap.settings.language = 'en_US'; // For example, enter 'en' or 'en-US'

			embeddedservice_bootstrap.init(
				'00DOz000004sefh',
				'Github',
				'https://legrandav--crmdev.sandbox.my.site.com/ESWGithub1722163913919',
				{
					scrt2URL: 'https://legrandav--crmdev.sandbox.my.salesforce-scrt.com'
				}
			);
		} catch (err) {
			console.error('Error loading Embedded Messaging: ', err);
		}
	};
</script>
<script type='text/javascript' src='https://legrandav--crmdev.sandbox.my.site.com/ESWGithub1722163913919/assets/js/bootstrap.min.js' onload='initEmbeddedMessaging()'></script>
