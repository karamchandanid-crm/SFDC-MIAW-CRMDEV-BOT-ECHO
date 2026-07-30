<html>
  <head>
    <title>
      MIAW Demo: CRMDEV (sandbox)
    </title>
    <style>
      h1{
        display: none;
      }
    </style>
  </head>
  <body>
    <h2> MIAW Demo: CRMDEV (sandbox)</h2>
    <script type='text/javascript'>
    	function initEmbeddedMessaging() {
		try {
			embeddedservice_bootstrap.settings.language = 'en_US'; // For example, enter 'en' or 'en-US',
			// Override default behavior and hide the chat button at initialization
			embeddedservice_bootstrap.settings.hideChatButtonOnLoad = true;
			// Messaging for Web init call
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
	<!-- Create a custom button or invitation to launch the web chat client. -->
	<button id="launchChatButton" onclick="launchChat()">Click to contact support</button>
	<!-- Call Launch Chat API. -->
	<script>
	    function launchChat() {
	    	embeddedservice_bootstrap.utilAPI.showChatButton();
	        embeddedservice_bootstrap.utilAPI.launchChat()
	            .then(() => {
	                // Success handler used to perform actions
	                // when the chat client launches successfully.
	                // For example, create a method that disables the launch chat button.
	                disableLaunchChatButton();
	            }).catch(() => {
	                // Error handler used to perform actions
	                // if the chat client fails to launch.
	                // For example, create a method that hides the launch chat button.
	                hideLaunchChatButton();
	            }).finally(() => {
	                // Finally handler used to perform any clean-up actions
	                // regardless of whether the chat client launches successfully or not.
	                // For example, create a method that logs the user’s attempt to chat.
	                logEndUserAttemptToChat();
	            });
	    }
	</script>
  </body>
</html>
