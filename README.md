### Hi there 👋

<!--
**Caplay/Caplay** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
<!--START_SECTION:waka-->
name: Waka Readme

on:
  # for manual workflow trigger
  workflow_dispatch:
  schedule:
    # runs at 12 AM UTC (5:30 AM IST)
    - cron: "0 0 * * *"

jobs:
  update-readme:
    name: WakaReadme DevMetrics
    runs-on: ubuntu-latest
    steps:
        # this action name
      - uses: athul/waka-readme@master # do NOT replace with anything else
        with:
          
          WAKATIME_API_KEY: ${{ secrets.WAKATIME_API_KEY }} # required
          ### meta
          API_BASE_URL: https://wakatime.com/api # optional
          REPOSITORY: YOUR_GITHUB_USERNAME/YOUR_REPOSITORY_NAME # optional
          ### content
          SHOW_TITLE: true # optional
          SECTION_NAME: waka # optional
          BLOCKS: -> # optional
          CODE_LANG: rust # optional
          TIME_RANGE: all_time # optional
          LANG_COUNT: 10 # optional
          SHOW_TIME: true # optional
          SHOW_TOTAL: true # optional
          SHOW_MASKED_TIME: false # optional
          STOP_AT_OTHER: true # optional
          IGNORED_LANGUAGES: YAML JSON TOML # optional
          ### commit
          COMMIT_MESSAGE: Updated waka-readme graph with new metrics # optional
          TARGET_BRANCH: master # optional
          TARGET_PATH: README.md # optional
          COMMITTER_NAME: GitHubActionBot # optional
          COMMITTER_EMAIL: action-bot@github.com # optional
          AUTHOR_NAME: YOUR_NAME # optional
          AUTHOR_EMAIL: YOUR@EMAIL.com # optional
          # you can populate email-id with secretes instead
<!--END_SECTION:waka-->
