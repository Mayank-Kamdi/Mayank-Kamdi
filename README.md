```markdown
---

# GitHub Analytics

<div align="center">

<img height="180em" src="https://github-readme-stats.vercel.app/api?username=Mayank-Kamdi&show_icons=true&theme=tokyonight&hide_border=true&include_all_commits=true&count_private=true"/>

<img height="180em" src="https://github-readme-streak-stats.herokuapp.com/?user=Mayank-Kamdi&theme=tokyonight&hide_border=true"/>

</div>

<div align="center">

<img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Mayank-Kamdi&layout=compact&theme=tokyonight&hide_border=true"/>

</div>

<br/>

<div align="center">

<img src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=Mayank-Kamdi&theme=tokyonight"/>

</div>

---

# GitHub Trophies

<div align="center">

<img src="https://github-profile-trophy.vercel.app/?username=Mayank-Kamdi&theme=tokyonight&no-frame=true&row=2&column=4&margin-w=15&margin-h=15"/>

</div>

---

# Contribution Activity

<div align="center">

<img src="https://github-readme-activity-graph.vercel.app/graph?username=Mayank-Kamdi&theme=tokyo-night&hide_border=true&area=true"/>

</div>

<br/>

<div align="center">

<img src="https://github-profile-summary-cards.vercel.app/api/cards/productive-time?username=Mayank-Kamdi&theme=tokyonight&utcOffset=5.5"/>

</div>

---

# Contribution Snake

<div align="center">

<img src="https://raw.githubusercontent.com/Mayank-Kamdi/Mayank-Kamdi/output/github-contribution-grid-snake-dark.svg" alt="Snake Animation"/>

</div>

---

# Contribution Overview

<div align="center">

<img src="https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=Mayank-Kamdi&theme=tokyonight"/>

<img src="https://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=Mayank-Kamdi&theme=tokyonight"/>

</div>

<br/>

<div align="center">

<img src="https://github-profile-summary-cards.vercel.app/api/cards/stats?username=Mayank-Kamdi&theme=tokyonight"/>

<img src="https://github-profile-summary-cards.vercel.app/api/cards/productive-time?username=Mayank-Kamdi&theme=tokyonight&utcOffset=5.5"/>

</div>

---
```
.github/workflows/snake.yml

name: Generate Snake

on:
  schedule:
    - cron: "0 */12 * * *"
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - uses: Platane/snk@v3
        with:
          github_user_name: Mayank-Kamdi
          outputs: |
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark

      - uses: crazy-max/ghaction-github-pages@v4
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
