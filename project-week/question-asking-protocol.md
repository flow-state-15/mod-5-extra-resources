# React Solo Week Question Protocol

<a name="#readme-top"></a>

<p align="right" style="font-size:10px">
  <a href="../README.md">Back to project week README</a>
</p>

Questions during project week will be asked on Slack! Please do so in your
cohort's online lecture questions channel. This way other students, not in your
circles, may benefit from the shared knowledge of those questions being
resolved.

## How to Ask A Question During Solo Project Week

After spending around 15 minutes debugging on your own:

Your peers and instructional team will attempt to help you with the question
via Slack first. If unable to solve the issue via slack, a member of the
Instructional team will come to your Breakout Room. Please remember wait times
may be long during project week.

When posting on Slack please utilize the following format:

### Question Asking Protocol

Your questions will be a copy of this form, filled out:

```
Problem: <what you expected but what is actually happening>

What you’ve tried: <self explanatory>

Github branch: <all students must make a branch for debugging, please provide a direct link to the branch>

Screenshots: <snippets/ss of code that you think we would need to solve the problem, always provide screenshot of any errors in the terminal or console>
```

### Example of Question Asking Protocol

> Problem: I'm having an issue when creating a pokemon. When creating a pokemon, the pokemon is created in the database, but only appears when refreshing the page.
>
> What you’ve tried: I've tried tracing the data flow from the submission of the create pokemon form to the database. I found that the pokemon was created in the database, so the error must be in my store file for pokemon. I've checked my thunk, reducer, and actions but I'm unsure of what the error could be. There are no errors in the console or backend terminal. Attached below are my handleSubmit, thunk, action, reducer, and backend route.

Github branch: http://github.com/jdrichardsappaca/my-solo-project

Screenshots:

## Reminders

- It is unacceptable to just post “Can someone come help me in my room”. You
  must, first, ask a question on Slack.
- Please do not DM the instructors for help.
- Instructors are not there to pair program or build your app, they are only
  there to guide you in the right direction

## Why Are We Using This Protocol?

Please keep in mind, the goal of this process is not to arbitrarily make the
project more challenging. This question asking process is simulating how you
might request assistance on the job as a software engineer.

Outside of a/A, you will not have anyone on standby to help. Anyone that could
help likely has responsibilities of their own. This means, the most effective
way to receive help is by making it as easy as possible to be helped!

This process is to practice and improve your abilities at requesting assistance.

## How to Take Screenshots and Format Code on Slack?

Taking screenshots is an easy way to improve the quality of your questions.
Once you learn the keyboard shortcuts it takes seconds to consistently acquire
multiple screenshots that can be used to convey the nature of your bug.

Consult the documentation linked below to learn more about taking screenshots
on your operating system. These keyboard shortcuts below will work for most
purposes:

- [Windows][windows-screenshot]:
  - `Windows logo key + Shift + S`
- [MacOS][macos-screenshot]:
  - `Shift + Command + 4`
- [Linux][linux-screenshot]:
  - `Shift + PrtScn`

Formatting text and code can be done in a Slack message with either Markdown
syntax directly or utilizing the built in user interface buttons. Check out
this documentation link for examples:

- [Format your messages on Slack][slack-format-messages]

## Industry Guides on How to Ask a Question

- [Stack Overflow's question guide][stack-overflow-question-guide]
- [Writing the perfect question][the-perfect-question]
- [How to be great at asking coding questions][great-at-asking-questions]

<p align="right" style="font-size:10px">
  <a href="#readme-top">Back to the top</a>
</p>
<p align="right" style="font-size:10px">
  <a href="./README.md">Back to project week README</a>
</p>

<!-- screenshots documentation links -->

[windows-screenshot]: https://support.microsoft.com/en-us/windows/use-snipping-tool-to-capture-screenshots-00246869-1843-655f-f220-97299b865f6b#:~:text=Press%C2%A0Windows%20logo%20key%C2%A0%2B%C2%A0Shift%C2%A0%2B%C2%A0S.
[macos-screenshot]: https://support.apple.com/guide/mac-help/take-a-screenshot-or-screen-recording-mh26782/mac#:~:text=Take%20pictures%20using%20keyboard%20shortcuts
[linux-screenshot]: https://www.wikihow.com/Take-a-Screenshot-in-Linux#:~:text=Press%20.%E2%87%A7%20Shift%2BPrtScn%20to%20select%20what%20you%20capture

<!-- resources links -->

[slack-format-messages]: https://slack.com/help/articles/202288908-Format-your-messages
[stack-overflow-question-guide]: https://stackoverflow.com/help/how-to-ask
[the-perfect-question]: https://codeblog.jonskeet.uk/2010/08/29/writing-the-perfect-question/
[great-at-asking-questions]: https://medium.com/@gordon_zhu/how-to-be-great-at-asking-questions-e37be04d0603
