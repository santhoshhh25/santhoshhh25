<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>Santhosh | Frontend Developer</title>
  <style>
    :root {
      --primary: #2563eb;
      --primary-light: #3b82f6;
      --secondary: #7c3aed;
      --dark: #0f172a;
      --light: #f8fafc;
      --gray: #94a3b8;
      --card-bg: rgba(255, 255, 255, 0.92);
      --transition: all 0.3s ease;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }

    body {
      background: linear-gradient(135deg, #f0f9ff 0%, #e0f2fe 100%);
      color: var(--dark);
      line-height: 1.6;
      padding: 0;
      overflow-x: hidden;
    }

    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 2rem 1.5rem;
    }

    header {
      text-align: center;
      padding: 4rem 0 2rem;
    }

    .banner-container {
      max-width: 800px;
      margin: 0 auto 2rem;
      border-radius: 16px;
      overflow: hidden;
      box-shadow: 0 10px 30px rgba(0, 0, 100, 0.1);
    }

    .banner-container img {
      width: 100%;
      display: block;
    }

    h1 {
      font-size: 3.5rem;
      margin: 1rem 0 0.5rem;
      background: linear-gradient(90deg, var(--primary), var(--secondary));
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }

    .subtitle {
      font-size: 1.4rem;
      color: var(--gray);
      max-width: 700px;
      margin: 0 auto 1.5rem;
      font-weight: 400;
    }

    .social-links {
      display: flex;
      justify-content: center;
      gap: 1.5rem;
      margin: 2rem 0;
    }

    .social-link {
      display: flex;
      align-items: center;
      gap: 0.5rem;
      padding: 0.8rem 1.8rem;
      border-radius: 50px;
      text-decoration: none;
      font-weight: 600;
      transition: var(--transition);
      background: var(--card-bg);
      box-shadow: 0 4px 15px rgba(0, 0, 0, 0.05);
      color: var(--dark);
      border: 1px solid rgba(37, 99, 235, 0.1);
    }

    .social-link:hover {
      transform: translateY(-3px);
      box-shadow: 0 6px 20px rgba(37, 99, 235, 0.15);
    }

    .social-link svg {
      width: 20px;
      height: 20px;
    }

    .section {
      margin: 3rem 0;
    }

    .section-title {
      font-size: 2rem;
      margin-bottom: 2rem;
      position: relative;
      display: inline-block;
    }

    .section-title::after {
      content: "";
      position: absolute;
      bottom: -8px;
      left: 0;
      width: 60px;
      height: 4px;
      background: var(--primary);
      border-radius: 2px;
    }

    .tech-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(140px, 1fr));
      gap: 1.5rem;
    }

    .tech-card {
      background: var(--card-bg);
      border-radius: 12px;
      padding: 1.5rem 1rem;
      text-align: center;
      transition: var(--transition);
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.05);
      border: 1px solid rgba(37, 99, 235, 0.08);
    }

    .tech-card:hover {
      transform: translateY(-5px);
      box-shadow: 0 8px 20px rgba(37, 99, 235, 0.12);
    }

    .tech-icon {
      width: 50px;
      height: 50px;
      margin: 0 auto 1rem;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
      gap: 2rem;
    }

    .project-card {
      background: var(--card-bg);
      border-radius: 16px;
      overflow: hidden;
      box-shadow: 0 6px 20px rgba(0, 0, 0, 0.08);
      transition: var(--transition);
      border: 1px solid rgba(37, 99, 235, 0.08);
    }

    .project-card:hover {
      transform: translateY(-7px);
      box-shadow: 0 12px 30px rgba(37, 99, 235, 0.15);
    }

    .project-image {
      height: 180px;
      background: linear-gradient(120deg, #e0f2fe, #dbeafe);
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .project-content {
      padding: 1.8rem;
    }

    .project-title {
      font-size: 1.3rem;
      margin-bottom: 0.8rem;
      display: flex;
      align-items: center;
      gap: 0.6rem;
    }

    .project-title a {
      color: var(--dark);
      text-decoration: none;
    }

    .project-title a:hover {
      color: var(--primary);
    }

    .stats-container {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 2rem;
      margin: 3rem 0;
    }

    .stat-card {
      background: var(--card-bg);
      border-radius: 16px;
      padding: 2rem;
      text-align: center;
      box-shadow: 0 6px 20px rgba(0, 0, 0, 0.05);
      border: 1px solid rgba(37, 99, 235, 0.08);
    }

    .stat-title {
      font-size: 1.2rem;
      margin-bottom: 1.5rem;
      color: var(--primary);
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 0.5rem;
    }

    .stat-image {
      max-width: 100%;
      border-radius: 8px;
    }

    .learning-section {
      background: var(--card-bg);
      border-radius: 16px;
      padding: 2.5rem;
      margin: 3rem 0;
      box-shadow: 0 6px 20px rgba(0, 0, 0, 0.05);
      border: 1px solid rgba(37, 99, 235, 0.08);
    }

    .learning-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 1.5rem;
      margin-top: 1.5rem;
    }

    .learning-item {
      display: flex;
      align-items: center;
      gap: 0.8rem;
      padding: 1rem;
      background: rgba(37, 99, 235, 0.05);
      border-radius: 12px;
      transition: var(--transition);
    }

    .learning-item:hover {
      background: rgba(37, 99, 235, 0.1);
      transform: translateX(5px);
    }

    footer {
      text-align: center;
      padding: 2rem 0 3rem;
      color: var(--gray);
      font-size: 0.9rem;
    }

    @media (max-width: 768px) {
      h1 {
        font-size: 2.5rem;
      }
      
      .subtitle {
        font-size: 1.1rem;
      }
      
      .social-links {
        flex-direction: column;
        align-items: center;
        max-width: 300px;
        margin: 2rem auto;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="banner-container">
        <img src="https://i.pinimg.com/originals/90/70/32/9070324cdfc07c68d60eed0c39e77573.gif" alt="Developer Banner">
      </div>
      <h1>Santhosh</h1>
      <p class="subtitle">Frontend Developer | Automation Specialist | Building with React, n8n, Supabase</p>
      
      <div class="social-links">
        <a href="https://santhoshhh25.github.io" class="social-link" target="_blank">
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 12a9 9 0 01-9 9m9-9a9 9 0 00-9-9m9 9H3m9 9a9 9 0 01-9-9m9 9c1.657 0 3-4.03 3-9s-1.343-9-3-9m0 18c-1.657 0-3-4.03-3-9s1.343-9 3-9m-9 9a9 9 0 019-9" />
          </svg>
          Portfolio
        </a>
        <a href="https://linkedin.com/in/YOUR-LINK" class="social-link" target="_blank">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor">
            <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z" />
          </svg>
          LinkedIn
        </a>
        <a href="mailto:youremail@example.com" class="social-link">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor">
            <path d="M24 5.457v13.909c0 .904-.732 1.636-1.636 1.636h-5.318V11.73L12 16.64l-5.045-4.91v9.273H1.636A1.636 1.636 0 0 1 0 19.366V5.457c0-2.023 2.309-3.178 3.927-1.964L5.455 4.64 12 9.548l6.545-4.91 1.528-1.145C21.69 2.28 24 3.434 24 5.457z" />
          </svg>
          Email
        </a>
      </div>
    </header>

    <section class="section">
      <h2 class="section-title">Tech Stack</h2>
      <div class="tech-grid">
        <div class="tech-card">
          <div class="tech-icon">
            <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" viewBox="0 0 48 48">
              <path fill="#E65100" d="M41 5H7l3 34 14 4 14-4 3-34z"></path>
              <path fill="#FF6D00" d="M24 8v31.9l11.2-3.2L37.7 8z"></path>
              <path fill="#FFF" d="M24 25v-4h8.6l-.7 11.5-7.9 2.6v-4.2l4.1-1.4.3-4.5H24zm8.9-8l.3-4H24v4h8.9z"></path>
              <path fill="#EEE" d="M24 30.9v4.2l-7.9-2.6-.4-5.5h4l.2 2.5 4.1 1.4zM19.1 17H24v-4h-9.1l.7 12H24v-4h-4.6l-.3-4z"></path>
            </svg>
          </div>
          <h3>HTML5</h3>
        </div>
        
        <div class="tech-card">
          <div class="tech-icon">
            <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" viewBox="0 0 48 48">
              <path fill="#0277BD" d="M41 5H7l3 34 14 4 14-4 3-34z"></path>
              <path fill="#039BE5" d="M24 8v31.9l11.2-3.2L37.7 8z"></path>
              <path fill="#FFF" d="M33.1 13H24v4h4.9l-.3 4H24v4h4.4l-.3 4.5-4.1 1.4v4.2l7.9-2.6.7-11.5z"></path>
              <path fill="#EEE" d="M24 13v4h-8.9l-.3-4H24zm-4.6 8l.2 4H24v-4h-4.6zm.4 6h-4l.3 5.5 7.9 2.6v-4.2l-4.1-1.4-.1-2.5z"></path>
            </svg>
          </div>
          <h3>CSS3</h3>
        </div>
        
        <div class="tech-card">
          <div class="tech-icon">
            <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" viewBox="0 0 48 48">
              <path fill="#FFD600" d="M6 42V6h36v36H6z"></path>
              <path fill="#000001" d="M29.538 32.947c.692 1.124 1.444 2.201 3.037 2.201 1.338 0 2.04-.665 2.04-1.585 0-1.101-.726-1.492-2.198-2.133l-.807-.344c-2.329-.988-3.878-2.226-3.878-4.841 0-2.41 1.845-4.244 4.728-4.244 2.053 0 3.528.711 4.592 2.573l-2.514 1.607c-.553-.988-1.151-1.377-2.078-1.377-.946 0-1.545.597-1.545 1.377 0 .964.6 1.354 1.985 1.951l.807.344C36.452 29.645 38 30.839 38 33.523 38 36.415 35.716 38 32.65 38c-2.999 0-4.702-1.505-5.65-3.368l2.538-1.685zm-11.586.082c.497.865 1.275 1.603 2.381 1.603 1.058 0 1.667-.418 1.667-2.043V22h3.333v11.101c0 3.367-1.953 4.899-4.805 4.899-2.577 0-4.437-1.746-5.195-3.368l2.619-1.603z"></path>
            </svg>
          </div>
          <h3>JavaScript</h3>
        </div>
        
        <div class="tech-card">
          <div class="tech-icon">
            <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" viewBox="0 0 48 48">
              <path fill="#00BCD4" d="M24 34.5C14.6 34.5 7 29.6 7 24s7.6-10.5 17-10.5S41 18.4 41 24s-7.6 10.5-17 10.5z"></path>
              <path fill="#448AFF" d="M31 24c0 5.2-5.9 9.5-13 9.5S5 29.2 5 24s5.9-9.5 13-9.5 13 4.3 13 9.5z"></path>
              <path fill="#3F51B5" d="M39 24c0 6.1-7.2 11-15 11s-15-4.9-15-11 7.2-11 15-11 15 4.9 15 11z"></path>
            </svg>
          </div>
          <h3>React</h3>
        </div>
        
        <div class="tech-card">
          <div class="tech-icon">
            <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" viewBox="0 0 48 48">
              <path fill="#38BDF8" d="M24 9.604c-6.4 0-10.4 3.403-12 10.203 2.4-3.203 5.2-4.406 8.4-3.604 1.826.456 3.131 1.781 4.576 3.247C27.328 21.236 30.553 24 36 24c6.4 0 10.4-3.403 12-10.203-2.4 3.203-5.2 4.406-8.4 3.604-1.826-.456-3.131-1.781-4.576-3.247C32.672 12.764 29.447 9.604 24 9.604zM12 24c-6.4 0-10.4 3.403-12 10.203 2.4-3.203 5.2-4.406 8.4-3.604 1.826.456 3.131 1.781 4.576 3.247C15.328 35.236 18.553 38.4 24 38.4c6.4 0 10.4-3.403 12-10.203-2.4 3.203-5.2 4.406-8.4 3.604-1.826-.456-3.131-1.781-4.576-3.247C20.672 26.764 17.447 24 12 24z"></path>
            </svg>
          </div>
          <h3>Tailwind</h3>
        </div>
        
        <div class="tech-card">
          <div class="tech-icon">
            <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" viewBox="0 0 48 48">
              <path fill="#AE44FC" d="M24 4C12.95 4 4 12.95 4 24s8.95 20 20 20 20-8.95 20-20S35.05 4 24 4zm-4 30h-4V22h4v12zm8 0h-4V14h4v20zm8 0h-4V18h4v16z"></path>
            </svg>
          </div>
          <h3>n8n</h3>
        </div>
        
        <div class="tech-card">
          <div class="tech-icon">
            <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" viewBox="0 0 48 48">
              <path fill="#3ECF8E" d="M24 4C12.95 4 4 12.95 4 24s8.95 20 20 20 20-8.95 20-20S35.05 4 24 4zm-7.5 30h-3V22h3v12zm7.5 0h-3V14h3v20zm7.5 0h-3V18h3v16z"></path>
            </svg>
          </div>
          <h3>Supabase</h3>
        </div>
      </div>
    </section>

    <section class="section">
      <h2 class="section-title">Featured Projects</h2>
      <div class="projects-grid">
        <div class="project-card">
          <div class="project-image">
            <svg xmlns="http://www.w3.org/2000/svg" width="60" height="60" viewBox="0 0 24 24" fill="none" stroke="#2563eb" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round">
              <path d="M17 3a2.85 2.83 0 1 1 4 4L7.5 20.5 2 22l1.5-5.5Z"/>
            </svg>
          </div>
          <div class="project-content">
            <h3 class="project-title">
              <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="#ef4444" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <circle cx="12" cy="12" r="10"></circle>
                <line x1="12" y1="8" x2="12" y2="12"></line>
                <line x1="12" y1="16" x2="12.01" y2="16"></line>
              </svg>
              <a href="https://santhoshhh25.github.io/marvel-universe/" target="_blank">Marvel Universe App</a>
            </h3>
            <p>Explore Marvel characters, comics, and stories in an interactive experience with rich visuals and detailed information.</p>
          </div>
        </div>
        
        <div class="project-card">
          <div class="project-image">
            <svg xmlns="http://www.w3.org/2000/svg" width="60" height="60" viewBox="0 0 24 24" fill="none" stroke="#2563eb" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round">
              <line x1="3" y1="12" x2="21" y2="12"></line>
              <line x1="3" y1="6" x2="21" y2="6"></line>
              <line x1="3" y1="18" x2="21" y2="18"></line>
            </svg>
          </div>
          <div class="project-content">
            <h3 class="project-title">
              <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="#3b82f6" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <path d="M21 16V8a2 2 0 0 0-1-1.73l-7-4a2 2 0 0 0-2 0l-7 4A2 2 0 0 0 3 8v8a2 2 0 0 0 1 1.73l7 4a2 2 0 0 0 2 0l7-4A2 2 0 0 0 21 16z"></path>
                <polyline points="3.27 6.96 12 12.01 20.73 6.96"></polyline>
                <line x1="12" y1="22.08" x2="12" y2="12"></line>
              </svg>
              <a href="https://santhoshhh25.github.io/Aurora-Dashboard/" target="_blank">Aurora Dashboard</a>
            </h3>
            <p>Modern admin dashboard with analytics, data visualization, and management tools built with React and Tailwind CSS.</p>
          </div>
        </div>
        
        <div class="project-card">
          <div class="project-image">
            <svg xmlns="http://www.w3.org/2000/svg" width="60" height="60" viewBox="0 0 24 24" fill="none" stroke="#2563eb" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round">
              <path d="M22 11.08V12a10 10 0 1 1-5.93-9.14"></path>
              <polyline points="22 4 12 14.01 9 11.01"></polyline>
            </svg>
          </div>
          <div class="project-content">
            <h3 class="project-title">
              <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="#10b981" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"></path>
                <polyline points="14 2 14 8 20 8"></polyline>
                <line x1="16" y1="13" x2="8" y2="13"></line>
                <line x1="16" y1="17" x2="8" y2="17"></line>
                <polyline points="10 9 9 9 8 9"></polyline>
              </svg>
              <a href="https://santhoshhh25.github.io/progress_pal/" target="_blank">Progress Pal</a>
            </h3>
            <p>Goal tracking application that helps users set, monitor, and achieve their personal and professional objectives.</p>
          </div>
        </div>
      </div>
    </section>

    <h2 class="section-title">GitHub Analytics</h2>
    <div class="stats-container">
      <div class="stat-card">
        <h3 class="stat-title">
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="#3b82f6" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <line x1="12" y1="20" x2="12" y2="10"></line>
            <line x1="18" y1="20" x2="18" y2="4"></line>
            <line x1="6" y1="20" x2="6" y2="16"></line>
          </svg>
          Contribution Stats
        </h3>
        <img src="https://github-readme-stats.vercel.app/api?username=santhoshhh25&show_icons=true&theme=default&bg_color=ffffff&hide_border=true&title_color=2563eb&text_color=334155&icon_color=3b82f6" alt="GitHub Stats" class="stat-image">
      </div>
      
      <div class="stat-card">
        <h3 class="stat-title">
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="#3b82f6" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <polyline points="22 12 18 12 15 21 9 3 6 12 2 12"></polyline>
          </svg>
          Streak Stats
        </h3>
        <img src="https://github-readme-streak-stats.herokuapp.com?user=santhoshhh25&theme=default&background=ffffff&hide_border=true&stroke=00000000&ring=3b82f6&fire=3b82f6&currStreakLabel=334155" alt="GitHub Streak" class="stat-image">
      </div>
    </div>

    <div class="learning-section">
      <h2 class="section-title">Currently Learning</h2>
      <p>Expanding my skills in modern web development and automation:</p>
      <div class="learning-grid">
        <div class="learning-item">
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="#3b82f6" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <circle cx="12" cy="12" r="10"></circle>
            <line x1="2" y1="12" x2="22" y2="12"></line>
            <path d="M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"></path>
          </svg>
          <span>Advanced React Patterns</span>
        </div>
        
        <div class="learning-item">
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="#3b82f6" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <polygon points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon>
          </svg>
          <span>GraphQL Implementations</span>
        </div>
        
        <div class="learning-item">
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="#3b82f6" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <path d="M18 3a3 3 0 0 0-3 3v12a3 3 0 0 0 3 3 3 3 0 0 0 3-3 3 3 0 0 0-3-3H6a3 3 0 0 0-3 3 3 3 0 0 0 3 3 3 3 0 0 0 3-3V6a3 3 0 0 0-3-3 3 3 0 0 0-3 3 3 3 0 0 0 3 3h12a3 3 0 0 0 3-3 3 3 0 0 0-3-3z"></path>
          </svg>
          <span>Cloud Automation</span>
        </div>
        
        <div class="learning-item">
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="#3b82f6" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <rect x="2" y="2" width="20" height="20" rx="2" ry="2"></rect>
            <path d="M8 2v20"></path>
            <path d="M17 2v20"></path>
            <path d="M2 12h20"></path>
            <path d="M2 8h4"></path>
            <path d="M2 16h4"></path>
            <path d="M18 16h4"></path>
            <path d="M18 8h4"></path>
          </svg>
          <span>UI/UX Design Principles</span>
        </div>
      </div>
    </div>

    <footer>
      <p>💡 Learning in public • Building projects daily • Making automation accessible</p>
      <p>© 2023 Santhosh | Crafted with passion</p>
    </footer>
  </div>
</body>
</html>
