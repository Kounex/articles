# How to handle configurations for Single Page Applications in a cloud-native environment

Applications / services need the ability to be configured without changing the source code. This is nothing new and is being used in a lot of occasions, especially because a lot of languages / frameworks offer such a feature out of the box. In cloud-native environments, this becomes even easier and more straight forward with for example frameworks like Quarkus, NestJS, Flask and so on. Doing that for static files which have already been compiled (often [Single Page Applications](https://developer.mozilla.org/en-US/docs/Glossary/SPA)) and are being served by a web server, for example [Angular](https://angular.io/) or [Flutter](https://flutter.dev/) being served by something like [NGINX](https://www.nginx.com/), has to be tackled differently though but is still something you want to be able to do.

## Preface

What I'm talking about: in order to customise applications so they can be used more generically, we need the ability to change specific configurations. This can be feature toggles to decide which parts of the application are active and useable or branding the application with custom colors or assets or even set credentials and change API endpoints. This will elevate applications to be used by a much broader audience and offer the customimsation needed to reuse such applications instead of writing them over and over again just to fit precisely as needed although available solutions often almost fit the needs.

How to enable such configurations depends on the stack and how the application is being served. A lot of classic services have an easier time dealing with this while the stack mentioned in the beginning and which we will focus on here does have some challenges. I will give you a short overview how it looks like with Quarkus as an easy example before going through the mentioned stack.

## The Quarkus Way
