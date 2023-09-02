# action-test

## Check your secrets !
When someone fork your repo, this is common that he didn't have all api keys in his secrets tabs... But when they are compiling, the build will fail because secrets are invalid, build time is longer...
Now, there is two options:
- Use a action that do builds for any `push` and do not use any secrets, and only for when a tag is detected (or when you release) use a another action, OR
- Filter which jobs (and not only steps) that couldn't run without specific secrets, and skip theses

I made some scripts to simplifie this second possibility. Every thing is here [`efc748b`/.github/workflows/variable-checker.yml](https://github.com/Starmania/action-test/blob/efc748b46f2f9a2b48428752a947aa22a2b800e5/.github/workflows/variable-checker.yml)
