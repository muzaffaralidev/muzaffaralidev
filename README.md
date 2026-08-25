<h1 align="center">Hi, I'm Muzaffar</h1>

<p align="center">
  <a href="https://muzaffarali.vercel.app/"><img src="https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white" /></a>
  <a href="https://www.linkedin.com/in/muzaffar-ali-0b3939315/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
  <a href="https://youtube.com/@muzaffaritacademy"><img src="https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white" /></a>
  <a href="https://x.com/muzafark_ali"><img src="https://img.shields.io/badge/X-000000?style=for-the-badge&logo=x&logoColor=white" /></a>
  <a href="https://www.facebook.com/profile.php?id=100093557110026"><img src="https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white" /></a>
</p>

<p align="center">
AI-Powered Web & Agent Developer building full-stack apps and intelligent agents.<br/>
Currently focused on Agentic AI through GIAIC & SMIT.
</p>

---

### 🛠️ Skills

**Frontend**
<div align="left">
  <img src="https://skillicons.dev/icons?i=html,css,js,ts,react,nextjs,tailwind,figma" />
</div>

**Backend**
<div align="left">
  <img src="https://skillicons.dev/icons?i=nodejs,express,fastapi,python,postgres,mongodb,mysql,supabase" />
</div>

**AI & Tools**
<div align="left">
  <img src="https://skillicons.dev/icons?i=git,github,vercel,docker,firebase" />
</div>

---

### 📊 GitHub Stats

<p align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=muzaffaralidev&show_icons=true&theme=radical&count_private=true" />
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=muzaffaralidev&layout=compact&theme=radical" />
</p>

### 📈 Contribution Graph

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=muzaffaralidev&theme=react-dark&area=true&hide_border=true" />
</p>

### 🐍 Contribution Snake

name: Generate Snake Animation

on:
  schedule:
    - cron: "0 0 * * *"  # runs once a day
  workflow_dispatch:      # lets you trigger it manually
  push:
    branches:
      - main

permissions:
  contents: write

jobs:
  generate:
    runs-on: ubuntu-latest
    steps:
      - name: Generate Snake SVG
        uses: Platane/snk@v3
        with:
          github_user_name: muzaffaralidev
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark

      - name: Push to output branch
        uses: crazy-max/ghaction-github-pages@v4
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
