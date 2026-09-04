<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&height=220&color=gradient&customColorList=2,3,5&text=Sanika%20Kangane&fontColor=ffffff&fontSize=48&fontAlign=50&fontAlignY=38&desc=B.Tech%20CSE%20'29%20·%20Builder%20·%20Explorer&descAlign=50&descAlignY=58&animation=fadeIn" alt="header banner" width="100%"/>

<br/>

<h3>
  <code>what if?</code> → <code>let's build it.</code>
</h3>

<sub>Turning curiosity into code, one experiment at a time.</sub>

<br/><br/>

<a href="https://linkedin.com/in/sanikakangane"><img src="https://img.shields.io/badge/LinkedIn-0A0A0A?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=0A0A0A" alt="LinkedIn"/></a>
<a href="https://twitter.com/sanika915623"><img src="https://img.shields.io/badge/Twitter-0A0A0A?style=for-the-badge&logo=x&logoColor=white&labelColor=0A0A0A" alt="Twitter"/></a>
<a href="https://instagram.com/sanikakangane_108"><img src="https://img.shields.io/badge/Instagram-0A0A0A?style=for-the-badge&logo=instagram&logoColor=white&labelColor=0A0A0A" alt="Instagram"/></a>

</div>

<br/>

## Now

```txt
role      Building small, working experiments
exploring Backend development, AI, databases & emerging tech
open to   AI tools, creative web apps & student-built products
seeking   Ambitious ideas that turn into polished, scalable builds
```

<br/>

## Overview

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=sanikakangane&show_icons=true&count_private=true&hide_border=true&theme=tokyonight&bg_color=0D1117&title_color=A78BFA&icon_color=A78BFA&text_color=C9D1D9&ring_color=A78BFA" alt="Sanika's GitHub stats" height="165"/>
<img src="https://github-readme-streak-stats.herokuapp.com/?user=sanikakangane&hide_border=true&theme=tokyonight&background=0D1117&ring=A78BFA&fire=A78BFA&currStreakLabel=A78BFA" alt="Sanika's contribution streak" height="165"/>

</div>

<div align="center">

<img src="https://github-readme-activity-graph.vercel.app/graph?username=sanikakangane&theme=tokyo-night&bg_color=0D1117&color=A78BFA&line=A78BFA&point=C9D1D9&hide_border=true&area=true" alt="Sanika's contribution activity graph" width="100%"/>

</div>

<div align="center">

<!--START_SECTION:contribution-snake-->
<img src="https://raw.githubusercontent.com/sanikakangane/sanikakangane/output/github-contribution-grid-snake-dark.svg" alt="Sanika's contribution snake animation" width="100%"/>
<!--END_SECTION:contribution-snake-->

</div>

<sub>Analytics update automatically — numbers reflect live GitHub activity, not static claims.</sub>

<br/>

## Stack

<div align="center">

<img src="https://skillicons.dev/icons?i=cpp,py,js,html,css,nodejs,mongodb,postgres,git,linux&theme=dark" alt="tech stack icons"/>

</div>

<div align="center">

| Languages | Backend & Data | Tools |
|:---:|:---:|:---:|
| C++ · Python · JavaScript | Node.js · MongoDB · PostgreSQL · Pandas | Git · Linux |

</div>

**Currently learning:** system design fundamentals, applied AI/ML, and scalable backend architecture.

<br/>

## Philosophy

<div align="center">

*Most of my projects start with a question I probably should've ignored — and end as something I'm glad I didn't.*

</div>

<br/>

## Build in Motion

<div align="center">
<sub>Reserved for future demo GIFs and project walkthroughs.</sub>
</div>

<br/>

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&height=100&color=gradient&customColorList=2,3,5&section=footer" alt="footer banner" width="100%"/>

<sub>© Sanika Kangane · Let's connect through GitHub, LinkedIn, or a good idea.</sub>

</div>

name: generate snake animation
on:
  schedule:
    - cron: "0 */12 * * *"
  workflow_dispatch: {}
  push:
    branches: [ main ]

permissions:
  contents: write

jobs:
  generate:
    runs-on: ubuntu-latest
    steps:
      - uses: Platane/snk/svg-only@v3
        with:
          github_user_name: sanikakangane
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark
      - uses: crazy-max/ghaction-github-pages@v4
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
