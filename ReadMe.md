# 💫 About Me:
Estudante de Front End em busca de oportunidades.


## 🌐 Socials:
[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://linkedin.com/in/https://www.linkedin.com/in/emersonmartinscorrea/) 

# 💻 Tech Stack:
![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=plastic&logo=html5&logoColor=white) ![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=plastic&logo=javascript&logoColor=%23F7DF1E) ![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=plastic&logo=css3&logoColor=white) ![MySQL](https://img.shields.io/badge/mysql-%2300000f.svg?style=plastic&logo=mysql&logoColor=white) ![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=plastic&logo=postgresql&logoColor=white) ![AZUREDEVOPS](https://img.shields.io/badge/azuredevops-0078D7.svg?style=plastic&logo=azuredevops&logoColor=white&color=%230078D7)
# 📊 GitHub Stats:
![](https://github-readme-stats.vercel.app/api?username=Emerson-Correa&theme=midnight-purple&hide_border=false&include_all_commits=false&count_private=false)<br/>
![](https://github-readme-streak-stats.herokuapp.com/?user=Emerson-Correa&theme=midnight-purple&hide_border=false)<br/>
![](https://github-readme-stats.vercel.app/api/top-langs/?username=Emerson-Correa&theme=midnight-purple&hide_border=false&include_all_commits=false&count_private=false&layout=compact)

name: Generate snake animation

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"

  workflow_dispatch:

  push:
    branches:
    - master

jobs:
  generate:
    permissions:
      contents: write
    runs-on: ubuntu-latest
    timeout-minutes: 5

    steps:
      - name: generate snake.svg
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: dist/snake.svg?palette=github-dark


      - name: push snake.svg to the output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

---
[![](https://visitcount.itsvg.in/api?id=Emerson-Correa&icon=5&color=8)](https://visitcount.itsvg.in)

<!-- Proudly created with GPRM ( https://gprm.itsvg.in ) -->
