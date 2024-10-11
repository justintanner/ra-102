## Rails Academy: Lesson 102 - Rails Hello World

At the end of this lesson you with have a created your first rails project.

### Topics

- Rails New
- Rails Controllers
- Rails Views

### Prerequisites

[Lesson 101](https://github.com/justintanner/ra-101)

### 1. Get into the lesson repository

First, let's make sure we are in the correct directory:

```bash
cd ~/lessons/ra-102
```

### 2. Branch and checkout

Next, we'll create a personal branch to work out of named after your Github username:

```bash
git checkout -b YOUR_GITHUB_USERNAME
```

A quick way to get your Github username is to run:

```bash
gh api user --jq '.login'
```

After that you should see a terminal like:

```bash
~/lessons/ra-102 (branch: github_username)
$ _
```

### 3. Create a new rails project

Still in the `ra-102` directory, run the following command to create a new Rails project:

```bash
rails new . --skip-git
```

This will create a new Rails project in the current directory, skipping git because the lesson already has a git repository.

Now lets our ruby gems by running:

```bash
bundle install
```

### 4. Launch a local server

```bash
rails server
```

Visit [http://localhost:3000](http://localhost:3000) in your browser to see your new app running with the default Rails welcome page.

### 5. Save your changes to git

```bash
git add .
git commit -m "Installed Rails"
```

### 6. Create a home controller

```bash
rails generate controller home index
```
This will create a new controller called `home` with an action called `index`.

### 7. Update the routes

Open the `config/routes.rb` file and add the following line
    
```ruby
root 'home#index'
```

This will set the `home#index` action as the root of the application.

### 8. Update the view

Open the `app/views/home/index.html.erb` file and add the following line:

```html
<h1>Hello World</h1>
```

### 9. Double check your work

Start the local server by running:

```bash
rails server
```

If you see "Hello World" on [http://localhost:3000](http://localhost:3000) it's working.

### 10. Save your changes to git

```bash
git add .
git commit -m "Added home controller"
```

### 11. Create a Pull Request

```bash
gh pr create
```

* Visit your PR on Github.

The automatic check will run if your code passes, you'll see:

:white_check_mark: All checks have passed

### :tada: You're Done! :tada:

#### Next Lesson

To start the [next lesson](https://github.com/justintanner/ra-103) run:

```bash
git clone https://github.com/justintanner/ra-103.git ~/lessons/ra-103
```

#### Additional Resources

- :book: [Action View](https://guides.rubyonrails.org/action_view_overview.html)
- :book: [Routing](https://guides.rubyonrails.org/routing.html)
- :tv: [Ruby on Rails](https://rubyonrails.org/)
- :tv: [Ruby on Rails in 100 Seconds](https://www.youtube.com/watch?v=2DvrRadXwWY)
