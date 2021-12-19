

# DE | Mongoose Recipes

## Requirements

- [Fork this repo](https://guides.github.com/activities/forking/).
- Clone your fork into your `~/code/labs` folder.

## Submission

Upon completion, run the following commands:

```bash
$ git add .
$ git commit -m"done"
$ git push origin master
```

Navigate to your repo and create a Pull Request -from your master branch to the original repository master branch.

In the Pull Request name, add your Campus, name, and the last name separated by a dash "-".

## Introduction

We learned how to run a server using **NodeJS**, and adding **Express** framework for structuring our routes and some other stuff. Today we will create our first server and analyze a bit the `request` object we receive every time we navigate to an URL.

Some of the coolest web analytics software works this way, analyzing every request. For example **Google Analytics** have a report where they display from which web browser the user is getting into your webpage.

![image](https://user-images.githubusercontent.com/23629340/38502468-c0752c90-3c0f-11e8-87eb-d9eb0bc405d1.png)

## Iteration 1

First, we need to create our project. After cloning this repo, you will find an empty `app.js` file. Go ahead and create your server using `Express`. 

:::info
**Remember to run `$ npm install` on the console to install every package you have on the `package.json`.** And run the file using `nodemone` so you don't need to restart the server after every change!
:::

You should also create your first route `/`, where we will display **"Hello Ironhacker"** and two links:

- Analyze the Request! ---> will navigate to `/request`
- Get the Web Browser! ---> will navigate to `/web-browser`

![image](https://user-images.githubusercontent.com/23629340/38502701-5e6778b8-3c10-11e8-9707-4750ea2647d1.png)

## Iteration 2

You should create a `request` route using *Express*. Before sending the `response` you should get the following from the `request`:

- **User-Agent**. On the request object, we have the `headers` key, that includes this info. 
- **Method**. Also on the request object, you will find the method.
- **URL**. On the request object, there is a URL field.
- **Host**. On the request object as well, there is a host field.
- **Image**. You should also add an image. On the `image` folder, inside `public` you will find some images you can use here! :wink:

After getting all the info, you should send a response including all these fields and print them like this:

![image](https://user-images.githubusercontent.com/23629340/38502945-1576bb18-3c11-11e8-8280-fb39304ec756.png)

:::info
**Remember you should use `app.use(express.static('public'))` to tell `Express` where are all your `static` files, such as `stylesheets`, `images`, etc. **
:::

## Iteration 3

Finally, let's get a bit hackier! For the final iteration, we need to create a custom middleware `checkTheAgent()`. This middleware will check which **agent family** we are using, and will attach that info to the `request`.

Getting the **agent family** could be a bit more tricky, so we will use a **NPM package** that will do this job for us. You should require the package on the top of the `app.js` file, and inside your middleware, call the `parse` method.

```javascript
const useragent = require('useragent');
useragent(true);

//.....

checkTheAgent = (request, response, next) => {
  const agent = useragent.parse(request.headers['user-agent']);
  //....more code here
}
```

:::info
**Remember to call the `next()` method on the middleware, to continue the execution!
:::
