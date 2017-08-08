# GitHub Summary Daily Project
### The Iron Yard Houston

GitHub provides data on users and their open-source projects via its API. You can get info about a single user or about a user's repositories.

For this project, you will make a Rails application that shows a summary of GitHub activity for a user. There should be a homepage where you can enter a GitHub username, and then a route that shows the summary, like /summaries/:username. When someone enters a username on the front page, they should be redirected to the appropriate summary page.

That summary page should look something like the following:
![GitHub Resume](https://github.com/Xiupan/GitHubSummary/blob/master/github-resume.png)

To build this page, you will need to make a few API requests. There are many libraries to do this with Ruby. We recommend HTTParty for its ease of use with JSON.

When someone requests a summary page, check to see if you have already made the API requests to build it. If so, show it. If not, use ActiveJob to make the requests and show the user a page that says that building the page is in progress. When the job is over, show the user the completed page.

Tips  

The majority of what you need to make this work is under "Creating a Job" in your Background Processes lesson.
When you get data back from the API, store the parts you need in a database. You will likely have a User model, Language model, and Repo model.
