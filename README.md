#!/usr/bin/env python3
# GitHub Profile README Generator for aimaniahub (Sumanth Prasad TM)
# Enhanced with resume details: Education, Skills, Projects, Experience, Certifications
# Analyzed repos: Focus on AI/ML, Data Analysis, Finance, Web Dev with Python & TypeScript
# Includes dynamic badges for stats, streak, and attractive Markdown visuals

import datetime

USERNAME = "aimaniahub"
NAME = "Sumanth Prasad T M"
BIO = """Motivated Data Analyst specializing in statistical analysis and data visualization. Proficient with Python, SQL, and Power BI to conduct in-depth exploratory data analysis (EDA), identify key trends, and build predictive models. Experienced in developing data-centric applications and eager to contribute to leading tech companies."""
LOCATION = "Chitradurga, Karnataka, India"
EMAIL = "prasadsumanth8@gmail.com"
PHONE = "+91-9353789909"
LINKEDIN = "https://in.linkedin.com/in/sumanth-prasad-tm-74291927b"
TWITTER = ""  # Add if available
WEBSITE = ""  # Add portfolio if available

# Education from resume
EDUCATION = """
- 🎓 **Bachelor of Engineering in Artificial Intelligence & Machine Learning**  
  Government Engineering College Challakere, Challakere, India  
  Expected: June 2026 | CGPA: 7.8 / 10.0
"""

# Skills from resume - grouped for visuals
CORE_SKILLS = ["Data Analysis", "Data Visualization", "Statistical Analysis", "Data Cleaning", "ETL Processes", "Predictive Modeling"]
PROGRAMMING = ["Python (Pandas, NumPy, Scikit-learn)", "SQL", "NoSQL", "R (Basic)", "C++"]
BI_TOOLS = ["Power BI", "Tableau (Basic)", "Matplotlib", "Seaborn"]
DEV_TOOLS = ["Git", "GitHub", "Docker", "Next.js", "ReactJS", "NodeJS"]

# Enhanced Projects from resume + GitHub analysis
PROJECTS = [
    {
        "name": "Synthara",
        "desc": """Intelligent Dataset Generation Engine.  
Developed a platform to transform unstructured natural language queries into structured, analyzable datasets in CSV format.  
Engineered an automated pipeline that scrapes web data, synthesizes information with AI, and validates datasets with Zod schemas.  
Visualized real-time processing for users via a Server-Sent Events (SSE) interface, improving transparency and usability.""",
        "tech": "Python, Next.js, Puppeteer, AI Models, Zod",
        "lang": "TypeScript",
        "url": f"https://github.com/{USERNAME}/Synthara"
    },
    {
        "name": "option-chain-analyser-fyers-",
        "desc": """AI-Powered Options Analysis with Fyers API Integration.  
Developed a comprehensive options analysis tool integrating with Fyers API for real-time option chain data and AI-powered insights.  
Built a batch analysis system to scan entire watchlists and identify top trade opportunities, enhancing trader efficiency (Reducing 60% of Manual Stock Analysis).  
Implemented institutional-level analysis to detect phenomena such as volume-OI spikes, dealer gamma exposure, and smart money flows.""",
        "tech": "Python (Flask, Pandas, NumPy), Google Gemini 2.0, Fyers APIv3, HTML, CSS, JavaScript",
        "lang": "Python",
        "url": f"https://github.com/{USERNAME}/option-chain-analyser-fyers-"
    },
    {
        "name": "Blockchain_AI_fraud-_detection",
        "desc": "AI-powered fraud detection system for blockchain transactions using machine learning models.",
        "tech": "Python, ML Models",
        "lang": "Python",
        "url": f"https://github.com/{USERNAME}/Blockchain_AI_fraud-_detection"
    },
    {
        "name": "nextjs-ai-chatbot",
        "desc": "Next.js-based AI chatbot for conversational interfaces, integrating AI models.",
        "tech": "Next.js, TypeScript, AI APIs",
        "lang": "TypeScript",
        "url": f"https://github.com/{USERNAME}/nextjs-ai-chatbot"
    },
    {
        "name": "musicgen_frontend",
        "desc": "Frontend interface for AI music generation tool (MusicGen).",
        "tech": "TypeScript, Web Frameworks",
        "lang": "TypeScript",
        "url": f"https://github.com/{USERNAME}/musicgen_frontend"
    },
    {
        "name": "healthcare",
        "desc": "Web application for healthcare management with AI-assisted features.",
        "tech": "TypeScript, React/Next.js",
        "lang": "TypeScript",
        "url": f"https://github.com/{USERNAME}/healthcare"
    }
]

# Professional Experience from resume
EXPERIENCE = """
### Tata Group Data Analytics Job Simulation on Forage  
**Machine Learning & Data Analyst Intern** | Remote | July 2025  

- Completed a job simulation involving AI-powered analytics and strategy development for the Financial Services team at Tata iQ.  
- Conducted exploratory data analysis (EDA) with GenAI tools to assess data quality, identify risk factors, and support predictive modeling.  
- Proposed an initial no-code predictive framework to assess customer delinquency risk, leveraging GenAI for structured logic and evaluation.
"""

# Certifications from resume
CERTIFICATIONS = [
    "Cisco Networking Academy – Introduction to Cybersecurity (Dec 2024)",
    "NodeJS with Express & MongoDB – Udemy",
    "Python for Data Science – XIE",
    "Microsoft AI Classroom – Microsoft",
    "C programming & SQL – HackerRank"
]

def generate_readme():
    current_date = datetime.datetime.now().strftime("%Y-%m-%d")
    
    # Header
    readme = f"""# Hi there, I'm {NAME} 👋

![Profile Views](https://komarev.com/ghpvc/?username={USERNAME}&label=Profile%20views&color=0e75b6&style=flat)

{BIO}

**Location:** {LOCATION} | **Email:** {EMAIL} | **Phone:** {PHONE} | **LinkedIn:** [{LINKEDIN.split('/')[-2]}]({LINKEDIN})

## 🚀 About Me
- 🔭 I’m currently working on AI-driven tools for data analysis, finance, and machine learning applications.  
- 🌱 I’m learning advanced ML models, decentralized apps, and full-stack development.  
- 💬 Ask me about Python for data science, web apps with Next.js, or trading algorithms!  
- 📫 How to reach me: {EMAIL}  
- 😄 Pronouns: He/Him  

{EDUCATION}

## 📊 GitHub Stats
<div align="center">

[![{NAME}'s GitHub Stats](https://github-readme-stats.vercel.app/api?username={USERNAME}&show_icons=true&theme=radical&hide_border=true&title_color=6aa6f5&icon_color=79c0ff)](https://github.com/anuraghazra/github-readme-stats)

[![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username={USERNAME}&layout=compact&theme=radical&hide_border=true)](https://github.com/anuraghazra/github-readme-stats)

[![Streak Stats](https://github-readme-streak-stats.herokuapp.com/?user={USERNAME}&theme=radical&hide_border=true)](https://github.com/DenverCoder1/github-readme-streak-stats)

[![Activity Graph](https://activity-graph.herokuapp.com/graph?username={USERNAME}&theme=react-dark&hide_border=true)](https://github.com/Ashutosh00710/github-readme-activity-graph)

</div>

## 🛠️ Technical Skills
<div align="center">

### Core Competencies
{chr(10).join([f"• {skill}" for skill in CORE_SKILLS])}

### Programming & Databases
{chr(10).join([f"• {skill}" for skill in PROGRAMMING])}

### BI & Visualization Tools
{chr(10).join([f"• {skill}" for skill in BI_TOOLS])}

### Developer Tools & Frameworks
{chr(10).join([f"• {skill}" for skill in DEV_TOOLS])}

</div>

## 🔥 Featured Projects
<div align="center">

| Project | Description | Technologies |
|---------|-------------|--------------|
"""
    
    for proj in PROJECTS:
        desc_lines = proj['desc'].split('\n')
        short_desc = desc_lines[0] if len(desc_lines) > 0 else proj['desc']
        readme += f"| [![{proj['name']}]({proj['url']})<br/>[{proj['name']}]({proj['url']}) | {short_desc}<br/><details><summary>More Details</summary>{proj['desc']}</details> | {proj['tech']} |\n"
    
    readme += """</div>

## 💼 Professional Experience
{EXPERIENCE}

## 📜 Certifications
<div align="center">
{chr(10).join([f"• {cert}" for cert in CERTIFICATIONS])}
</div>

## 📈 Contribution Streak
Your current streak is dynamically shown in the badge above! Consistent contributions to AI and data projects will help build an impressive streak (aim for 30+ days for that advanced look).

## 🤝 Let's Connect!
- 📧 **Email:** {EMAIL}  
- 📞 **Phone:** {PHONE}  
- 💼 **LinkedIn:** [{LINKEDIN.split('/')[-2]}]({LINKEDIN})  
- 🐦 **Twitter:** {TWITTER} (Add if available)  
- 🌐 **Portfolio:** {WEBSITE} (Add your site here)

<div align="center">
<a href="{LINKEDIN}"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
<a href="mailto:{EMAIL}"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
</div>

---

⭐ Star this repository if you found it helpful! | Last Updated: {current_date}

<!--- 
This README is auto-generated. For more details, check the script used to create it.
--->
"""
    
    # Format the readme
    readme = readme.format(
        USERNAME=USERNAME,
        NAME=NAME,
        CURRENT_DATE=current_date,
        EDUCATION=EDUCATION,
        EXPERIENCE=EXPERIENCE,
        EMAIL=EMAIL,
        PHONE=PHONE,
        LINKEDIN=LINKEDIN,
        TWITTER=TWITTER,
        WEBSITE=WEBSITE
    )
    
    return readme

if __name__ == "__main__":
    print(generate_readme())
