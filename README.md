// profile-readme-generator.js
const fs = require("fs");
const fetch = require("node-fetch");

const USERNAME = "aimaniahub";

async function generateReadme() {
  // Fetch repos
  const reposRes = await fetch(`https://api.github.com/users/${USERNAME}/repos?sort=updated&per_page=6`);
  const repos = await reposRes.json();

  let projectsMarkdown = repos
    .map(
      (repo) => `- [**${repo.name}**](${repo.html_url}) → ${repo.description || "No description"}`
    )
    .join("\n");

  // Profile Template
  const content = `# Hi there, I'm Sumanth Prasad T M 👋

![Profile Views](https://komarev.com/ghpvc/?username=${USERNAME}&label=Profile%20views&color=0e75b6&style=flat)

Motivated **Data Analyst** specializing in statistical analysis and visualization.

---

## 📊 GitHub Stats
<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=${USERNAME}&show_icons=true&theme=radical" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=${USERNAME}&layout=compact&theme=radical" />
</p>

---

## 🔥 Featured Projects
${projectsMarkdown}

---

⭐ *Auto-generated profile README*  
`;

  fs.writeFileSync("README.md", content);
  console.log("✅ README.md generated!");
}

generateReadme();
