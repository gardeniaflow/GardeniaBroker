<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>gardeniatest3</title>
</head>
<body>
    <!-- JavaScript to load the chatbot asynchronously -->
    <script>
        function generateClientId() {
            // Generate a random string, e.g., using a timestamp
            return 'client-' + Date.now();
        }

        function loadChatbotScript() {
            var clientId = generateClientId(); // Generate a unique clientId
            var script = document.createElement('script');
            script.src = 'https://cdn.botpress.cloud/webchat/v0/inject.js';
            script.async = true;
            document.body.appendChild(script);

            script.onload = function () {
                window.botpressWebChat.init({
                    "botId": "0e30855c-6873-4f87-9de6-b3352a0622b3",
                    "clientId": clientId, // Use the generated clientId
                    "hostUrl": "https://cdn.botpress.cloud/webchat/v0",
                    "messagingUrl": "https://messaging.botpress.cloud",
                    "botName": "Gardenia",
                    "avatarUrl": "https://i.postimg.cc/YC8DyGW1/Screenshot-2023-09-13-213012.jpg",
                    "containerWidth": "100%25",
                    "layoutWidth": "100%25",
                    "composerPlaceholder": "Start typing here",
                    "botConversationDescription": "Your Property Partner",
                    "hideWidget": true,
                    "disableAnimations": true,
                    "enableConversationDeletion": true
                });
                window.botpressWebChat.onEvent(function () {
                    window.botpressWebChat.sendEvent({ type: 'show' });
                }, ['LIFECYCLE.LOADED']);
            };
        }

        // Call the function to load the chatbot script
        loadChatbotScript();
    </script>
</body>
</html>
