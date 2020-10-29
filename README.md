| 💡 I found awesome library to solve this problem. [envsub](https://github.com/danday74/envsub) can substitute env variables in file to values. Just use that library, if you have same problem. 
# Add env to Google App Engine config file

## What is it?

- It's a script to add environment variables to Google App Engine config file (app.xml)
- It adds environment variables to `app.xml` at deploy time.

## Why did you make it?

- Google App Engine config file is exposing environment variables in plain text.
- I just want to make it more secure.

## When can I use it?

- When you deploy your code to Google App Engine by CD(Continuous Delivery) tool (e.g. Github Actions, Bitbucket pipelines, Circle CI, Etc.)

## How to use?

- Add names of environment variable that you want to add to `app.xml` to `.env.array`
- Add key/value of environment variable in your CD tool settings.
- Add commands to run this script to your CD tool config file.

## Warning

- It's only run correctly when `app.xml` doesn't have `env_variables` field.
- You have to migrate all environment variables from `app.xml` to CD tool settings.

## Example
- [Bitbucket pipelines](./bitbucket-pipelines.yml)
