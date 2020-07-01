# Setup GreenSock As A Module With Parcel

📹 [Video](https://egghead.io/lessons/greensock-setup-greensock-as-a-module-with-parcel)

Start by creating a folder for your new project, then add [parcel bundler](https://parceljs.org/getting_started.html) as a dev dependency

```
yarn add -D parcel-bundler
```

Now you have a package.json where you can add a script called dev that will use parcel to run the index.html file.

```js
{
    "scripts": {
        "dev": "parcel index.html"
    },
    "devDependencies": {
        "parcel-bundler": "version#"
    }
}
```

Create an index.html file, a default template ( ! tab inside index.html ) is sufficient.

You can now run the command

```
yarn dev
```

and go to the corresponding url (defaults to http://localhost:1234) to see your project.

stop your server before adding index.js script

Add an index.js file and add a script tag to index.html to bring it in.

 ```js
 <script src='./index.js'></script>
 ```

Restart your server after adding index.js script

You can now test your js by adding some `innerHTML` to the `document.body`

## Install Greensock

Now import from 'gsap' at the top of index.html

```
import { TweenMax } from 'gsap'
```

Parcel bundler will automatically add the dependency, if you aren't using parcel-bundler then run

```
yarn add gsap
```

to install greensock

You can now create an element in index.html, and then run a gsap animation in index.js

```js
TweenMax.to("element", duration, {properties})
```

Take a look at your animation in the browser.


📹 [Next Lesson](https://egghead.io/lessons/greensock-animate-and-center-an-element-to-a-click-event-with-greensock)