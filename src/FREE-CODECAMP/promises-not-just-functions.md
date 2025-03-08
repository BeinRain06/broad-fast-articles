## Why The Need of Promises, why not Just Functions ?

### Introduction

The core value concept of javascript **promise** remains hidden to me for while. I could grasp the definition saying is a kind of function that basically helps you, achieve another performance at the end of it using the methods **then()** and **catch()** to enable the execution of a new show. But couldn't help Questions myself why all these trouble ? Why not just a simple function and then a result ? Why so much effort to get to `promise` something before actually renders it ?

### Body

In Real world, time is the ultimate metric from which we can measure changes over everything. A promise made need to be fulfilled in a set time or not.

In 2015 Javascript's Team release a new feature under ECMA Script (standard for scripting languages) called **promises**. This new concept must be a new alternative to **callback** functions, returning error message in case it produces.

<br/>

### Why Not Just Functions ?

Javascript manipulates data through **functions**, each one of them output a result at their end. The idea of dynamic websites is supported by writing many scripts inside declared functions in Javascript. Their are special one compose of other(s) function(s) past as parameter(s) into it. The function that becomes a parameter to another are known as **callback** function. Their use shorten code to write much of the times , bringing elegance to lines of code, and also adaptability of troubleshoot quickly.

Imagine you are at School. It's the break down , you reach the canteen. Enough Hungry, but proud of you. So proud that you earlier in the start of the week put some really huge nerves to your mom and dad ; and angry they decided you will be left without money for school for a week. You usually supports these vibe, it is not the first time. But this black friday something seems different, this particular day you don't know why hunger beats you. Seeing foods spred everywhere over multiple box's canteens, and people serving it with smile to customers. You say to yourself : "Their might be a way to live for you, before you collapse". You take courage on hand to ask "Jimmy" one of your friend : "Hey Dude. Can you command meal for two, for two !" while smiling like a crocodile. He takes a moment before looking at your side for while and then smile back saying: " don't worry, i will definitely do it for you".

You know , you just made a callback function. Here is how we can resume all this:

<br/>

```js
function helpFromJimmy() {
  const jimmyGuy = "I have the foods proud man";
  return jimmyGuy;
}

function hungryDonald(helpFromJimmy) {
  const myThought = "A Thanks You , will be Good";
  return `${helpFromJimmy()} + "." + ${myThought}`;
}
```

<br/>

In the above example `helpFromJimmy` is a callback function to **hungryDonald**.

Anytime you find yourself repeating a couples lines of javascript code or any other languages under your app in development, you need to condense these lines into a reusable function (**callback**). One that in case of need you just called from anywhere in the app and run. Reducing latency loading app and enhancing a common good experience to users's browsing.

e.g : a `loading page` can be made as a callback function to process both before the home page fully render and after a form submittion button is clicked waiting to gather data entered before closing the form's assistance box.

### Why Promises ?

Donald does well earlier with callback function, and we quite find ourself out of trouble. In a real app , things doesn't work smoothly like that our Jimmy here we don't see him face to face , he works under the tcp/ip model and we need **internet connection** to have a word with him. You may have access to some functionnalities **offline** but for fully browsing all contents in a website, you need a running internet connection. And without connection some **meta data** like images, data load from database, or deep action on button clicked sending or getting information from/to distance resources become unavailable and not effective.

Real built application is composed of pieces data at one side coming from your local computer and the other side from remote **web servers**, the both periodically exchanging informations, based on the use of the app. This process of communication involves access to several resources, and programs, lying into remote devices(tcp/ip model), and when i said many, their are really **many**.

While browsing a website, these informations captured need to be sent as in no time, optimized quickly and render almost instantly to our browser, for good experience; it has to be all about **time efficiency**. This is one of the **purpose** that leads to understand **promises**. We gives somes times(to many remote devices, routers), to send or get our **data** right to the entrance's door of the computer in need (server side or client side), and we make a **play** out of it (specific actions).

**Promise** helps perform shadow communication with others resources, out the scene of standard script syntax for dynamic webpage. To get some data back to your local computer or sent it under a specific form to a dedicated remote computer (web server). The promise (_Jimmy helps_) everytime whispers: `"i know you can't do it all by yourself but i promise to help you go through it. Supporting the system communication. Leaving you the choice to Next do what you want"`. This willing structure of the promise gives opportunity to catch and print **errors** in case there is a mess that cease the transmission between distance computer that are backbones for your app , disrupting work with online resources implemented inside.

<br/>

```js
function fetchAllRegisteredUsers() {
  return new Promise(async function (resolve, reject) {
    const users = await UserDB.find(); // mongodb database syntax example

    if (!users) {
      reject("There is a problem fetching users in mongoDB Database");
    }

    resolve(users);
  });
}
```

<br/>

If you get **users** the function `fetchAllRegisteredUsers()` has **fulfilled** its promise (_new Promise (...)_ ) , if not an error message will be sent via **reject()** method inside the console of the integrated terminal of your editor.

When the action is a success, you can make further operations. Like For example : `"filter users that name begins with the character 'a'"` .

<br/>

```js
const usersFirstLetterA = fetchAllRegisteredUsers()
  .then((response) => response.filter((user) => user[0].toUpperCase() === "A"))
  .catch((err) => {
    console.log(`error filter : ${err}`);
  });

console.log(usersFirstLetterA);
```

<br/>

This way you will retrieve all users that starts with the letter "a". And so actually made an action out of `promise`. That is the beauty of how it looks melting different functions in **chain** at a specific times. You can also do of the second function **usersFirstLetterA** a **promise** and continue the process of getting or sending data in a deep nested level structure. You can add any action after a successfull promise. Even a simple message that state a greeting fit perfectly, all is by your choice and what exactly you intend to do.

Though **promise** are part of the process of exchanging data between remote and local computer, it is not in fact a **protocol** of communication. While many websites need to communicate following a specific scheme, the **http/https** protocol. The gain attraction that add up other parameters to configure aren't primarly integrated in the **promise** standard. Programmers aware of that decided to develop library as **fetch API** or **axios** to give simple way to configure parameters of communication between websites and use **promise** structure to send or get data. This reduce a lot the amount of code's written that are due to configurating your app to exhange data with secure resource held on server side out of your computer, giving you ability to build your app focusing just on data directly related to the problem you are trying to solve.
