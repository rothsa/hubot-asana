# Asana for Hubot

* Add tasks to Asana using Hubot automatically
    - Listens for match to regex string on specific Slack channels
    - Posts task to Asana when regex string is satisfied. 

## Installation

Add `hubot-asana-listener` to your `package.json` file:

    "dependencies": {
      "hubot": ">= 2.5.1",
      "hubot-scripts": ">= 2.4.2",
      "hubot-asana-listener": ">= 0.0.0"
    }

Then add "hubot-asana" to your `external-scripts.json` file:

    ["hubot-asana-listener"]

Finally, run `npm install hubot-asana-listener` and you're done!

### Configuration

- ASANA_WORKSPACE_ID - Your workspace's ID.
- ASANA_TEAM_ID - Your team's ID.
- ASANA_DEFAULT_PROJECT_ID - Your default project's ID.
- ASANA_DEFAULT_PROJECT_NAME - Your default project's name.
- SLACK_CHANNEL_NAMES - Channels to listen to
- SLACK_REGEX_STRING - String to post tasks for

### Usage


Hubot will listen for the strings you specify in the channels you specify, and will post a timestamped task to Asana based on posts that match.
A task added to Asana must have a name. Both an assignee and a project are optional. Some examples:
    <detected regex string>
    <detected regex string> #bugs
    @travis <detected regex string>
    @steve <detected regex string> #bugs
