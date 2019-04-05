# cordova-plugin-apns-push

> Register and receive APNS push notifications

# Install

Install via npm :-  `cordova plugin add cordova-plugin-apns-push`

# Usage

```js 

    var push = window['APNSPushNotification'].init({
        ios: {
            alert: "true",
            badge: "true",
            sound: "true"
        }
        });


    push.on('registration', (data) => {
        // data.registrationId
        this.sendRegDetails(data.registrationId);
    });

    push.on('notification', (data) => {
        window['cordova'].plugins.notification.local.schedule({
        title: data.title,
        text: data.message,
        sound: data.sound,
        at: new Date().getTime()
        });
    });

    push.on('error', (e) => {
        // e.message
        console.error(e);
    });

```

# Supported Platforms
 
 - iOS

# More about us
Find out more or contact us directly here :- http://www.neutrinos.co/

Facebook :- https://www.facebook.com/Neutrinos.co/ <br/>
LinkedIn :- https://www.linkedin.com/company/25057297/ <br/>
Twitter :- https://twitter.com/Neutrinosco <br/>
Instagram :- https://www.instagram.com/neutrinos.co/

[![N|Solid](https://image4.owler.com/logo/neutrinos_owler_20171023_142541_original.jpg "Neutrinos")](http://www.neutrinos.co/) 

