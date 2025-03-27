## Why The Need of Promises, why not Just Functions ?

### Introduction

Back in time when i was learning the ES6 javascript’s standard **promise**. The core concept of this new feature ( looking like an object inside a function ) remains hidden to me. The fact that it allows you basically attach one or many others functions at the end of their instantiation for outputting others performance was understandable. What it wasn’t was the reasons. Why? Why all these trouble? Why not just a simple function and then a result ? Why so much effort to get to promise something before actually renders it ?

### Metric

In Real world, time is the ultimate metric from which we can measure changes over everything. Strongly a promise also need some times to be fulfilled or not.

In 2015 Javascript's Team release a new feature under ECMA Script (standard for scripting languages) called **promises**. This new concept must be a new alternative to **callback** functions, returning error message in case something come up messy.

<br/>

### Why Not Just Functions ?

Javascript most of the times manipulates data through **functions**, where each one of them is expected to output a result at their end’s process. The idea of developing dynamic websites was largely supported by writing scripts under these functions. Because some lines of code where repetitive between different functions, one cooking specialization was to wrap them as function and further pass them in any other function in need. We talk of these functions under the name of callback. **Callback** is the meaningful name given **to function that are past like parameter** into one another, representing an argument of that latter function. Their use shorten code and bring elegance and more reliability in case of issue to fix. But what are we even talking about callback.

Well, imagine yourself at School. It’s the recess, you move to the canteen. Enough Hungry, but proud of you. So proud that with the beginning of the week you put really huge nerves to your dad and mom. Cause you are a grown man!? To teach you some lessons they whatsoever cut your allowance for the week. You usually go through that vibes and it means nothing. But this day , this particular black Friday, you don't know why hunger beats you like a nobody. Seeing foods spread everywhere over multiple box's canteens; Sellers attending students buying foods with smile. You can’t believe you will collapse before the world who knows you. You take courage and reach to one of of your guy “Jimmy“ saying : “Hey Dude. Can you command meal for two, for two !“ smiling like a crocodile. he take a while and comes to look at you for a little good time and says smiling back gently : “don’t worry , i will definitely do it for you“.

You know what , you just made a callback function.

Here is how we can **resume** all this:

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

Anytime you find yourself repeating a couples lines of javascript code or any other programming languages inside your project, you need to condense those lines into a reusable function (**callback**). Where living case could be called from anywhere in the app and run. This reduces load times in running app as well as enhance common good experience to the users's browsing.

e.g : a `loading page` can be made as a callback function to process both before the home page fully render and after a form submittion button is clicked waiting to gather data entered before closing the form's assistance box.

<br/>

### Why Promises ?

Donald does amazing well earlier using callback function to pull himself out of trouble. Much as In a real app ,things doesn't happen straightforward like it did. Our Jimmy we mentioned earlier we can't access to him directly. He plays the role of deliverer under the tcp/ip model. And we need **internet connection** to have a word with him. Functionalities **offline** are not fully operational. To browse along all contents in a website, you need a running internet connection. And without that, some **meta data** like images, data load from database, or deep action on button clicked, sending or getting information from/to distance resources become unavailable and ineffective.

Real built **applications** are organized in pieces of components that run upon data coming from either your local computer or other remote computer connected online **web servers**. The browser (**client side**) represent the screen of your website. And information sent back and forth from the client-side to web servers, allow applications to fully perform all the programmed tasks when a user interact with it. This process of communication involves access to several resources, and programs, lying into remote devices(tcp/ip model), and when i said many, their are really **many**.

While browsing a website, these information captured need to be sent, as in no time, optimized quickly and render almost instantly to our browser. This to ensure good experience. Because of time efficiency we need a system to process all data not directly available to us and make them accessible at the moment they are taken back into our app. We then a **purpose** that leads to **promises**. We gives some times (to many remote devices, routers), to send or get our **data** right to the entrance's door of the concern's computer (server side or client side), and we further make one or several **play** out of those (specific actions).

**Promise** helps perform shadow communication with others resources, out the scene of standard script syntax for dynamic webpage. As result they sent back data to your local computer or any specific remote computer (web server) joined in the protocol communication established by **HTTP**. Promise (_Jimmy helps_) every time whispers: `"i know you can't do it all by yourself but i promise to help you go through it. Supporting the system communication. Leaving you the choice to Next do what you want"`. This willing structure of the promise gives opportunity to catch and print **errors** in case there is a mess in your syntax or an online security that cut off the transmission with distance computer that are backbones for your app.

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

This way you will retrieve all users that starts with the letter "a". And so actually made an action out of `promise`. That is the beauty of how it looks melting different functions in **chain** at specific time. You can also transform the second function **usersFirstLetterA** into **promise** and continue the process of getting or sending data in a deep nested level structure. Undoubtedly, You can add any action after a successful promise. Even a simple message that state a greeting fit perfectly. Is all up to you, you have the choice to bring out as result whatever you want in terms of the data sent.

Though **promise** are part of the process of exchanging data between remote and local computer, it is not in fact a **protocol** of communication. While many websites need to communicate following a specific scheme, the **HTTP/HTTPS** protocol. The gain attraction that add up other parameters to configure aren't primarily integrated in the **promise** standard. Programmers aware of that decided to develop library as **fetch API** or **axios** to give simple way to configure parameters of communication between websites (client side and web servers) and use **promise** structure to send or get data. This reduce a lot the amount of code to write to configure your app to exchange data with secure resource held on **server side** out of your computer. And also enhance ability to build your app while focusing just on data directly related to the problem you are trying to solve.
