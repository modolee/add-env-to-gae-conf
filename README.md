| 🚨 I found an awesome library to solve this problem. [envsub](https://github.com/danday74/envsub) can substitute env variables in file to values. If you are having the same problem, try using that library instead of this script.

# Add env to Google App Engine config file

## What is it?

- It's a shell script to add environment variables to Google App Engine config file (app.xml)
- It add environment variables to `app.xml` at deployment stage.

## Why did you made it?

- Google App Engine config file have been exposing environment variables in the form of plain text.
- I wanted it to me more secure.

## When can I use the script?

- When you deploy your code to Google App Engine via CD(Continuous Delivery) tool (e.g. Github Actions, Bitbucket pipelines, Circle CI, Etc.)

## How do I use it?

- Add name of environment variables that you want to add to `.env.array` in `app.xml`
- Add key/value of environment variable in your CD tool settings.
- Add commands to run this script to your CD tool config file.

## Warning

- It is expected to run correctly only when `app.xml` doesn't have `env_variables` field.
- You have to migrate all the environment variables from `app.xml` to CD tool settings.

## Example
- [Bitbucket pipelines](./bitbucket-pipelines.yml)
