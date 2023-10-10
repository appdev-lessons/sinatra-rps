# Sinatra: Rock, Paper, Scissors

In this project, you will build a simple game: Rock, Paper, Scissors.

Here is your target: 

[rps.matchthetarget.com](https://rps.matchthetarget.com/)

## Set up codespace

This project includes automated tests, so click on this button to get started:

LTI{Load Sinatra RPS assignment}(https://grades.firstdraft.com/launch)[S9ymPy6WCsn18gLbByVbZQ7k]{vfdtzJb5bLYqYwuqgeRKpc5d}(10)[Sinatra RPS Project]

Then, fork the repository and create your codespace. 

If you need a refresher on forking projects, creating codespaces, and running `rake grade`, then please watch this video again (you should watch at 2x speed for a quick review): [Link in bio Video](https://share.descript.com/view/Y4oUaIaI1pU). **Note**, in that video we ran our web server with the command `rackup`, but from now on we will use `bin/dev`. You will see that difference below.

## Starter code

<div class="bg-blue-100 py-1 px-5" markdown="1">

[Here is a video for the rest of this lesson](https://share.descript.com/view/9QqsWtzkTaz). You should not rely entirely on the video. PLEASE READ the below lesson as you are going through the steps, since there is much more detail in the text than in the video. As you watch the video, pause it frequently to experiment and write the code being demonstrated.
</div>

[In our first web app with Sinatra](https://learn.firstdraft.com/lessons/103-our-first-sinatra-app), we started from scratch. However, along the way, we made a few helpful changes that we decided we would make to every project moving forward from the get-go:

- Automatically reloading code changes without having to restart the web server with the `sinatra-contrib` gem.
- Better error pages with the `better_errors` gem.
- Create a `/views` folder to store our ERB templates.
- Create a `/views/layout.erb` file with standard HTML boilerplate in it.

With each app you build, you will find that you carry forward more and more tricks like this into a baseline set of starter code.

In this project, we've included a bunch of configuration that we've picked up through experience:

- There is a folder called `bin/` in which we placed a few useful scripts:
  - `bin/dev` starts up our web server, along with a few other niceties.

  <div class="bg-blue-100 py-1 px-5" markdown="1">

  From now on, we will _always_ start our live app preview (web server) by typing:

  ```
  % bin/dev
  ```

  At the bash prompt.

  We built up to this by first running `rackup` in early projects, and then running just our app file with e.g. `ruby dice.rb`. If you open the `bin/dev` file (look in the `bin/` folder) you will see that this is mostly just a fancy wrapper for our original `rackup` command, which is launched on the last line of the file with `rackup --port=3000`!
  </div>

  - `bin/setup` will `bundle install` and perform other initial setup work.
- There is a `spec/` folder that includes automated tests.
- The `rake grade` command is included to run the automated tests.
- We started you off with a file called `app.rb` in which to add your routes.
- There are changes related to getting the app ready to deploy on fly.io.

If you're curious, you can read through the starter code and try to get a sense of what it's all doing, but the important things to know are:

- Use `bin/dev` to start your web server from now on.
- You can run `rake grade` to check your work.

## Match the target

Spend some time exploring [the target](https://rps.matchthetarget.com/). How many paths are you able to visit? (Hint: that is how many routes you will have to create.) What must be happening in each action to generate the HTML that you see?

Try to use what you learned while building [our first web app with Sinatra](https://learn.firstdraft.com/lessons/103-our-first-sinatra-app), and the [subsequent lesson on view templates and embedded Ruby](https://learn.firstdraft.com/lessons/105-sinatra-view-templates), to make your app exactly match the target. It's okay to View Source on the target to see what HTML tags we used, and it's okay to copy-paste content (e.g. the rules from the homepage). But you'll have to figure out what Ruby is running on the back-end to make each dynamic page work on your own.

When you think you have the target matched, run `rake grade` to get automated feedback.

---
