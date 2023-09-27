<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gardenia Brokers</title>
</head>
<body>
    <!-- JavaScript to load the chatbot asynchronously -->
    <script>
        function loadChatbotScript() {
            var script = document.createElement('script');
            script.src = 'https://cdn.botpress.cloud/webchat/v0/inject.js';
            script.async = true;
            document.body.appendChild(script);

            script.onload = function () {
                window.botpressWebChat.init({
                    "botId": "e6af95fa-3798-43ed-a982-388667fe3a11",
                    "clientId": "e6af95fa-3798-43ed-a982-388667fe3a11",
                    "hostUrl": "https://cdn.botpress.cloud/webchat/v0",
                    "messagingUrl": "https://messaging.botpress.cloud",
                    "botName": "Gardenia",
                    "avatarUrl": "https://i.postimg.cc/YC8DyGW1/Screenshot-2023-09-13-213012.jpg",
                    "containerWidth": "100%25",
                    "layoutWidth": "100%25",
                    "composerPlaceholder": "Start typing here",
                    "botConversationDescription": "Your Property Partner",
                    "hideWidget": true,
                    "useSessionStorage": true,
                    "disableAnimations": true,
                    "lazySocket": true,
                    "frontendVersion": "v1",
                    "stylesheet": "https://webchat-styler-css.botpress.app/prod/code/5ce2b2c8-4482-424a-8e12-ad6bba19692c/v17650/style.css",
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
