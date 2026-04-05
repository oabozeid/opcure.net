<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Opcure — Pioneering Non-Invasive Eye Care Solutions</title>
<meta name="description" content="Opcure is developing a patented ophthalmic formulation to transform cataract treatment for 94 million patients worldwide.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,500;0,600;0,700;1,400;1,500&family=Outfit:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<style>
*, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }

:root {
  --bg-deep: #0b1120;
  --bg-primary: #0b1120;
  --bg-card: transparent;
  --bg-card-hover: rgba(255,255,255,0.03);
  --accent: #00c9a7;
  --accent-glow: rgba(0,201,167,0.15);
  --accent-soft: #00e6be;
  --gold: #c4a862;
  --text-primary: #f0f0f0;
  --text-secondary: #c8cdd8;
  --text-muted: #8a90a5;
  --border: rgba(255,255,255,0.08);
  --font-display: 'Playfair Display', Georgia, serif;
  --font-body: 'Outfit', sans-serif;
}

html { scroll-behavior: smooth; }

body {
  font-family: var(--font-body);
  background: var(--bg-deep);
  color: var(--text-primary);
  overflow-x: hidden;
  -webkit-font-smoothing: antialiased;
}

/* ===== CLEAN BACKGROUND ===== */

/* ===== NAVIGATION ===== */
nav {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 1000;
  padding: 0 48px;
  height: 72px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  backdrop-filter: blur(20px);
  -webkit-backdrop-filter: blur(20px);
  background: rgba(11,17,32,0.7);
  border-bottom: 1px solid var(--border);
  transition: all 0.4s ease;
}

nav.scrolled { background: rgba(11,17,32,0.95); }

.nav-logo {
  display: flex;
  align-items: center;
  gap: 12px;
  text-decoration: none;
  color: var(--text-primary);
}

.nav-logo svg { height: 36px; width: auto; }

.nav-logo span {
  font-family: var(--font-display);
  font-size: 22px;
  font-weight: 700;
  letter-spacing: -0.5px;
}

.nav-links {
  display: flex;
  align-items: center;
  gap: 36px;
  list-style: none;
}

.nav-links a {
  font-size: 14px;
  font-weight: 400;
  color: var(--text-secondary);
  text-decoration: none;
  letter-spacing: 0.5px;
  text-transform: uppercase;
  transition: color 0.3s;
  position: relative;
}

.nav-links a::after {
  content: '';
  position: absolute;
  bottom: -4px;
  left: 0;
  width: 0;
  height: 1px;
  background: var(--accent);
  transition: width 0.3s;
}

.nav-links a:hover { color: var(--text-primary); }
.nav-links a:hover::after { width: 100%; }

.nav-cta {
  padding: 10px 24px !important;
  background: var(--accent) !important;
  color: var(--bg-deep) !important;
  border-radius: 6px;
  font-weight: 600 !important;
  text-transform: uppercase !important;
  font-size: 12px !important;
  letter-spacing: 1px !important;
  transition: all 0.3s !important;
}

.nav-cta:hover { background: var(--accent-soft) !important; transform: translateY(-1px); }
.nav-cta::after { display: none !important; }

.menu-toggle {
  display: none;
  background: none;
  border: none;
  cursor: pointer;
  padding: 8px;
}

.menu-toggle span {
  display: block;
  width: 24px;
  height: 2px;
  background: var(--text-primary);
  margin: 5px 0;
  transition: 0.3s;
}

/* ===== HERO ===== */
.hero {
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  overflow: hidden;
  padding: 120px 48px 80px;
}

.hero-bg {
  position: absolute;
  inset: 0;
  z-index: 0;
}

.hero-bg::before {
  content: '';
  position: absolute;
  top: -30%;
  right: -10%;
  width: 800px;
  height: 800px;
  background: radial-gradient(circle, var(--accent-glow) 0%, transparent 70%);
  animation: pulse 8s ease-in-out infinite;
}

.hero-bg::after {
  content: '';
  position: absolute;
  bottom: -20%;
  left: -10%;
  width: 600px;
  height: 600px;
  background: radial-gradient(circle, rgba(196,168,98,0.08) 0%, transparent 70%);
  animation: pulse 10s ease-in-out infinite reverse;
}

@keyframes pulse {
  0%, 100% { transform: scale(1); opacity: 0.5; }
  50% { transform: scale(1.1); opacity: 1; }
}

.hero-content {
  position: relative;
  z-index: 1;
  text-align: center;
  max-width: 900px;
}

.hero-badge {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  padding: 8px 20px;
  border: 1px solid var(--border);
  border-radius: 100px;
  font-size: 12px;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: var(--accent);
  margin-bottom: 40px;
  background: rgba(0,201,167,0.05);
}

.hero-badge::before {
  content: '';
  width: 6px;
  height: 6px;
  background: var(--accent);
  border-radius: 50%;
  animation: blink 2s infinite;
}

@keyframes blink {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.3; }
}

.hero h1 {
  font-family: var(--font-display);
  font-size: clamp(42px, 6vw, 78px);
  font-weight: 600;
  line-height: 1.1;
  letter-spacing: -1.5px;
  margin-bottom: 28px;
  color: var(--text-primary);
}

.hero h1 em {
  font-style: italic;
  color: var(--accent);
}

.hero-sub {
  font-size: clamp(16px, 2vw, 20px);
  color: var(--text-secondary);
  line-height: 1.7;
  max-width: 640px;
  margin: 0 auto 48px;
  font-weight: 300;
}

.hero-actions {
  display: flex;
  gap: 16px;
  justify-content: center;
  flex-wrap: wrap;
}

.btn-primary {
  padding: 16px 36px;
  background: var(--accent);
  color: var(--bg-deep);
  border: none;
  border-radius: 8px;
  font-family: var(--font-body);
  font-size: 14px;
  font-weight: 600;
  letter-spacing: 1px;
  text-transform: uppercase;
  cursor: pointer;
  transition: all 0.3s;
  text-decoration: none;
}

.btn-primary:hover { background: var(--accent-soft); transform: translateY(-2px); box-shadow: 0 8px 30px var(--accent-glow); }

.btn-secondary {
  padding: 16px 36px;
  background: transparent;
  color: var(--text-primary);
  border: 1px solid var(--border);
  border-radius: 8px;
  font-family: var(--font-body);
  font-size: 14px;
  font-weight: 500;
  letter-spacing: 1px;
  text-transform: uppercase;
  cursor: pointer;
  transition: all 0.3s;
  text-decoration: none;
}

.btn-secondary:hover { border-color: var(--text-secondary); background: rgba(255,255,255,0.05); }

.hero-scroll {
  position: absolute;
  bottom: 32px;
  left: 50%;
  transform: translateX(-50%);
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 8px;
  color: var(--text-muted);
  font-size: 11px;
  letter-spacing: 2px;
  text-transform: uppercase;
  z-index: 1;
}

.hero-scroll-line {
  width: 1px;
  height: 40px;
  background: linear-gradient(to bottom, var(--accent), transparent);
  animation: scrollDown 2s infinite;
}

@keyframes scrollDown {
  0% { transform: scaleY(0); transform-origin: top; }
  50% { transform: scaleY(1); transform-origin: top; }
  51% { transform: scaleY(1); transform-origin: bottom; }
  100% { transform: scaleY(0); transform-origin: bottom; }
}

/* ===== SECTIONS ===== */
section { padding: 120px 48px; position: relative; }

.section-label {
  font-size: 12px;
  letter-spacing: 3px;
  text-transform: uppercase;
  color: var(--accent);
  margin-bottom: 16px;
  font-weight: 500;
}

.section-title {
  font-family: var(--font-display);
  font-size: clamp(32px, 4vw, 54px);
  font-weight: 600;
  line-height: 1.15;
  letter-spacing: -1px;
  margin-bottom: 24px;
}

.section-desc {
  font-size: 18px;
  color: var(--text-secondary);
  line-height: 1.8;
  max-width: 680px;
  font-weight: 300;
}

.container { max-width: 1200px; margin: 0 auto; }

/* ===== PROBLEM ===== */
.problem { background: var(--bg-primary); }

.problem-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 80px;
  align-items: center;
  margin-top: 64px;
}

.problem-stats {
  display: flex;
  flex-direction: column;
  gap: 40px;
}

.stat-item {
  padding: 32px;
  border-left: 2px solid var(--accent);
  background: var(--bg-card);
  border-radius: 0 12px 12px 0;
  transition: all 0.3s;
}

.stat-item:hover { background: var(--bg-card-hover); transform: translateX(4px); }

.stat-number {
  font-family: var(--font-display);
  font-size: 42px;
  font-weight: 700;
  color: var(--accent);
  margin-bottom: 8px;
}

.stat-label {
  font-size: 15px;
  color: var(--text-secondary);
  line-height: 1.6;
  font-weight: 300;
}

.problem-text { padding-right: 40px; }

.problem-quote {
  margin-top: 40px;
  padding: 28px 32px;
  border-radius: 12px;
  background: transparent;
  border: 1px solid rgba(0,201,167,0.12);
  position: relative;
}

.problem-quote p {
  font-family: var(--font-display);
  font-size: 17px;
  font-style: italic;
  color: var(--text-secondary);
  line-height: 1.7;
}

.problem-quote cite {
  display: block;
  margin-top: 12px;
  font-size: 13px;
  font-style: normal;
  color: var(--text-muted);
}

/* ===== CURRENT SOLUTION ===== */
.current-solution {
  background: var(--bg-deep);
  text-align: center;
}

.current-solution .section-desc { margin: 0 auto 48px; }

.gap-cards {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
  max-width: 960px;
  margin: 0 auto;
}

.gap-card {
  padding: 36px 28px;
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: 16px;
  text-align: center;
  transition: all 0.4s;
}

.gap-card:hover { border-color: rgba(0,201,167,0.2); background: var(--bg-card-hover); transform: translateY(-4px); }

.gap-card-icon {
  width: 48px;
  height: 48px;
  margin: 0 auto 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: var(--accent-glow);
  border-radius: 12px;
}

.gap-card-icon svg { width: 24px; height: 24px; stroke: var(--accent); fill: none; stroke-width: 1.5; }

.gap-card h4 {
  font-family: var(--font-display);
  font-size: 18px;
  margin-bottom: 10px;
  color: var(--text-primary);
}

.gap-card p {
  font-size: 14px;
  color: var(--text-secondary);
  line-height: 1.7;
  font-weight: 300;
}

/* ===== SOLUTION ===== */
.solution { background: var(--bg-primary); }

.solution-header { text-align: center; margin-bottom: 72px; }
.solution-header .section-desc { margin: 0 auto; }

.solution-desc-block {
  text-align: center;
  max-width: 800px;
  margin: 0 auto 72px;
  padding: 40px;
  border: 1px solid var(--border);
  border-radius: 20px;
  background: transparent;
}

.solution-desc-block p {
  font-size: 18px;
  color: var(--text-secondary);
  line-height: 1.8;
  font-weight: 300;
}

.solution-desc-block strong { color: var(--text-primary); font-weight: 500; }

.benefits-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 24px;
}

.benefit-card {
  padding: 40px 28px;
  border-radius: 20px;
  background: var(--bg-card);
  border: 1px solid var(--border);
  text-align: center;
  transition: all 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
  position: relative;
  overflow: hidden;
}

.benefit-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 2px;
  background: linear-gradient(90deg, transparent, var(--accent), transparent);
  opacity: 0;
  transition: opacity 0.4s;
}

.benefit-card:hover { transform: translateY(-8px); border-color: rgba(0,201,167,0.15); }
.benefit-card:hover::before { opacity: 1; }

.benefit-icon {
  font-size: 36px;
  margin-bottom: 20px;
  display: block;
}

.benefit-card h4 {
  font-family: var(--font-display);
  font-size: 20px;
  margin-bottom: 12px;
  color: var(--text-primary);
}

.benefit-card p {
  font-size: 14px;
  color: var(--text-secondary);
  line-height: 1.7;
  font-weight: 300;
}

.benefit-highlight {
  margin-top: 16px;
  display: inline-block;
  padding: 6px 14px;
  background: var(--accent-glow);
  border-radius: 100px;
  font-size: 13px;
  font-weight: 600;
  color: var(--accent);
}

/* ===== MARKET ===== */
.market { background: var(--bg-deep); position: relative; }

.market-header { text-align: center; margin-bottom: 72px; }
.market-header .section-desc { margin: 0 auto; }

.market-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
  margin-bottom: 32px;
}

.market-card {
  padding: 44px 32px;
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: 20px;
  text-align: center;
  transition: all 0.4s;
}

.market-card:hover { border-color: rgba(0,201,167,0.15); transform: translateY(-4px); }

.market-card .number {
  font-family: var(--font-display);
  font-size: clamp(36px, 4vw, 52px);
  font-weight: 700;
  color: var(--accent);
  margin-bottom: 4px;
  line-height: 1;
}

.market-card .number-suffix {
  font-family: var(--font-display);
  font-size: clamp(20px, 2vw, 28px);
  font-weight: 400;
  color: var(--accent);
}

.market-card .label {
  font-size: 15px;
  color: var(--text-secondary);
  line-height: 1.6;
  font-weight: 300;
  margin-top: 12px;
}

.market-row-2 {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 24px;
}

.patent-badge {
  margin-top: 48px;
  text-align: center;
  padding: 32px;
  border-radius: 16px;
  background: transparent;
  border: 1px solid rgba(0,201,167,0.12);
}

.patent-badge .number {
  font-family: var(--font-display);
  font-size: 64px;
  font-weight: 700;
  background: linear-gradient(135deg, var(--accent), var(--gold));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.patent-badge .label {
  font-size: 16px;
  color: var(--text-secondary);
  margin-top: 8px;
}

/* ===== WHY OPCURE ===== */
.why-opcure { background: var(--bg-primary); }

.why-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 24px;
  margin-top: 64px;
}

.why-card {
  padding: 40px;
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: 20px;
  transition: all 0.4s;
  position: relative;
}

.why-card:hover { border-color: rgba(0,201,167,0.15); transform: translateY(-4px); }

.why-card-number {
  font-family: var(--font-display);
  font-size: 48px;
  font-weight: 700;
  color: rgba(0,201,167,0.1);
  position: absolute;
  top: 20px;
  right: 28px;
}

.why-card h4 {
  font-family: var(--font-display);
  font-size: 22px;
  color: var(--accent);
  margin-bottom: 14px;
}

.why-card p {
  font-size: 15px;
  color: var(--text-secondary);
  line-height: 1.8;
  font-weight: 300;
}

/* ===== TEAM ===== */
.team {
  background: var(--bg-deep);
  text-align: center;
}

.team-header { margin-bottom: 64px; }
.team-header .section-desc { margin: 0 auto; }

.team-stats {
  display: flex;
  justify-content: center;
  gap: 72px;
  margin-bottom: 56px;
}

.team-stat { text-align: center; }

.team-stat .number {
  font-family: var(--font-display);
  font-size: 48px;
  font-weight: 700;
  color: var(--accent);
}

.team-stat .label {
  font-size: 14px;
  color: var(--text-secondary);
  margin-top: 4px;
  font-weight: 300;
}

.expertise-tags {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 12px;
  max-width: 800px;
  margin: 0 auto;
}

.expertise-tag {
  padding: 12px 24px;
  border: 1px solid var(--border);
  border-radius: 100px;
  font-size: 14px;
  color: var(--text-secondary);
  font-weight: 400;
  transition: all 0.3s;
}

.expertise-tag:hover { border-color: var(--accent); color: var(--accent); background: var(--accent-glow); }

/* ===== ROADMAP ===== */
.roadmap { background: var(--bg-primary); }

.roadmap-header { text-align: center; margin-bottom: 80px; }
.roadmap-header .section-desc { margin: 0 auto; }

.timeline { position: relative; max-width: 800px; margin: 0 auto; }

.timeline::before {
  content: '';
  position: absolute;
  top: 0;
  left: 24px;
  width: 2px;
  height: 100%;
  background: linear-gradient(to bottom, var(--accent), var(--border));
}

.timeline-item {
  position: relative;
  padding-left: 72px;
  padding-bottom: 56px;
}

.timeline-item:last-child { padding-bottom: 0; }

.timeline-dot {
  position: absolute;
  left: 14px;
  top: 6px;
  width: 22px;
  height: 22px;
  border-radius: 50%;
  background: var(--bg-deep);
  border: 2px solid var(--accent);
  z-index: 1;
}

.timeline-dot::after {
  content: '';
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 8px;
  height: 8px;
  border-radius: 50%;
  background: var(--accent);
}

.timeline-date {
  font-size: 13px;
  font-weight: 600;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: var(--accent);
  margin-bottom: 8px;
}

.timeline-title {
  font-family: var(--font-display);
  font-size: 22px;
  font-weight: 600;
  margin-bottom: 10px;
  color: var(--text-primary);
}

.timeline-desc {
  font-size: 15px;
  color: var(--text-secondary);
  line-height: 1.7;
  font-weight: 300;
}

/* ===== CONTACT / CTA ===== */
.contact {
  background: var(--bg-deep);
  text-align: center;
  padding: 140px 48px;
  position: relative;
  overflow: hidden;
}

.contact::before {
  content: '';
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 600px;
  height: 600px;
  background: radial-gradient(circle, var(--accent-glow) 0%, transparent 70%);
  opacity: 0.4;
}

.contact-content { position: relative; z-index: 1; }

.contact-logo {
  margin-bottom: 40px;
}

.contact-logo svg { height: 56px; width: auto; }

.contact h2 {
  font-family: var(--font-display);
  font-size: clamp(32px, 4vw, 52px);
  font-weight: 600;
  line-height: 1.15;
  margin-bottom: 20px;
  letter-spacing: -1px;
}

.contact h2 em { font-style: italic; color: var(--accent); }

.contact-sub {
  font-size: 18px;
  color: var(--text-secondary);
  margin-bottom: 48px;
  font-weight: 300;
}

.contact-email {
  display: inline-flex;
  align-items: center;
  gap: 12px;
  padding: 18px 40px;
  background: transparent;
  border: 1px solid var(--border);
  border-radius: 12px;
  font-size: 18px;
  color: var(--accent);
  text-decoration: none;
  font-weight: 500;
  transition: all 0.3s;
  letter-spacing: 0.5px;
}

.contact-email:hover { border-color: var(--accent); background: var(--accent-glow); transform: translateY(-2px); }

.contact-email svg { width: 20px; height: 20px; stroke: var(--accent); fill: none; stroke-width: 1.5; }

/* ===== FOOTER ===== */
footer {
  padding: 32px 48px;
  border-top: 1px solid var(--border);
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: var(--bg-deep);
}

footer p {
  font-size: 13px;
  color: var(--text-muted);
  font-weight: 300;
}

.footer-links {
  display: flex;
  gap: 24px;
}

.footer-links a {
  font-size: 13px;
  color: var(--text-muted);
  text-decoration: none;
  transition: color 0.3s;
}

.footer-links a:hover { color: var(--accent); }

/* ===== DIVIDER ===== */
.section-divider {
  width: 100%;
  height: 1px;
  background: linear-gradient(90deg, transparent, var(--border), transparent);
}

/* ===== SCROLL ANIMATIONS ===== */
.reveal {
  opacity: 0;
  transform: translateY(40px);
  transition: opacity 0.8s cubic-bezier(0.25, 0.46, 0.45, 0.94), transform 0.8s cubic-bezier(0.25, 0.46, 0.45, 0.94);
}

.reveal.visible { opacity: 1; transform: translateY(0); }

.reveal-delay-1 { transition-delay: 0.1s; }
.reveal-delay-2 { transition-delay: 0.2s; }
.reveal-delay-3 { transition-delay: 0.3s; }
.reveal-delay-4 { transition-delay: 0.4s; }
.reveal-delay-5 { transition-delay: 0.5s; }

/* ===== RESPONSIVE ===== */
@media (max-width: 1024px) {
  section { padding: 80px 32px; }
  .problem-grid { grid-template-columns: 1fr; gap: 48px; }
  .problem-text { padding-right: 0; }
  .benefits-grid { grid-template-columns: 1fr 1fr; }
  .market-grid { grid-template-columns: 1fr 1fr; }
  .why-grid { grid-template-columns: 1fr; }
  .team-stats { gap: 48px; }
}

@media (max-width: 768px) {
  nav { padding: 0 20px; height: 64px; }
  .nav-links { display: none; }
  .menu-toggle { display: block; }
  .nav-links.open {
    display: flex;
    flex-direction: column;
    position: absolute;
    top: 64px;
    left: 0;
    right: 0;
    background: rgba(11,17,32,0.97);
    padding: 24px 20px;
    gap: 20px;
    border-bottom: 1px solid var(--border);
    backdrop-filter: blur(20px);
  }
  section { padding: 56px 20px; }
  .hero { padding: 100px 20px 60px; min-height: auto; min-height: 100svh; }
  .hero h1 { font-size: 32px; letter-spacing: -0.5px; line-height: 1.15; }
  .hero-sub { font-size: 16px; margin-bottom: 32px; }
  .hero-badge { font-size: 10px; padding: 6px 14px; margin-bottom: 28px; }
  .hero-actions { flex-direction: column; align-items: stretch; }
  .btn-primary, .btn-secondary { text-align: center; padding: 14px 24px; font-size: 13px; }
  .hero-scroll { display: none; }
  .section-title { font-size: 28px; letter-spacing: -0.5px; }
  .section-desc { font-size: 16px; }
  .section-label { font-size: 11px; letter-spacing: 2px; }
  .problem-grid { gap: 36px; }
  .stat-item { padding: 20px 24px; }
  .stat-number { font-size: 32px; }
  .stat-label { font-size: 14px; }
  .problem-quote { padding: 20px; }
  .problem-quote p { font-size: 15px; }
  .gap-cards { grid-template-columns: 1fr; max-width: 100%; }
  .gap-card { padding: 28px 24px; }
  .solution-desc-block { padding: 28px 20px; margin-bottom: 48px; }
  .solution-desc-block p { font-size: 16px; }
  .benefits-grid { grid-template-columns: 1fr; gap: 16px; }
  .benefit-card { padding: 28px 24px; display: flex; flex-direction: column; align-items: center; }
  .benefit-icon { font-size: 28px; margin-bottom: 12px; }
  .benefit-card h4 { font-size: 18px; }
  .market-grid { grid-template-columns: 1fr; gap: 16px; }
  .market-row-2 { grid-template-columns: 1fr; gap: 16px; }
  .market-card { padding: 32px 24px; }
  .market-card .number { font-size: 36px; }
  .why-grid { gap: 16px; }
  .why-card { padding: 28px 24px; }
  .why-card h4 { font-size: 18px; }
  .why-card p { font-size: 14px; }
  .why-card-number { font-size: 36px; top: 16px; right: 20px; }
  .team-stats { flex-direction: column; gap: 24px; }
  .team-stat .number { font-size: 36px; }
  .expertise-tags { gap: 8px; }
  .expertise-tag { padding: 8px 16px; font-size: 13px; }
  .timeline { padding-left: 0; }
  .timeline::before { left: 16px; }
  .timeline-item { padding-left: 52px; padding-bottom: 40px; }
  .timeline-dot { left: 6px; width: 22px; height: 22px; }
  .timeline-title { font-size: 18px; }
  .timeline-desc { font-size: 14px; }
  .contact { padding: 64px 20px; }
  .contact h2 { font-size: 28px; }
  .contact-sub { font-size: 16px; margin-bottom: 32px; }
  .contact-email { font-size: 15px; padding: 14px 24px; }
  .contact-logo svg { height: 44px; }
  footer { flex-direction: column; gap: 12px; text-align: center; padding: 24px 20px; }
  .container { max-width: 100%; }
  .patent-badge .number { font-size: 48px; }
}
</style>
</head>
<body>

<!-- ===== NAVIGATION ===== -->
<nav id="navbar">
  <a href="#" class="nav-logo">
    <svg viewBox="0 0 40 40" xmlns="http://www.w3.org/2000/svg">
      <circle cx="20" cy="18" r="16" fill="white"/>
      <circle cx="14" cy="16" r="10" fill="#0b1120"/>
    </svg>
    <span>Opcure</span>
  </a>
  <ul class="nav-links" id="navLinks">
    <li><a href="#problem">Problem</a></li>
    <li><a href="#solution">Solution</a></li>
    <li><a href="#market">Market</a></li>
    <li><a href="#why">Why Opcure</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contact" class="nav-cta">Contact</a></li>
  </ul>
  <button class="menu-toggle" id="menuToggle" onclick="document.getElementById('navLinks').classList.toggle('open')">
    <span></span><span></span><span></span>
  </button>
</nav>

<!-- ===== HERO ===== -->
<section class="hero" id="hero">
  <div class="hero-bg"></div>
  <div class="hero-content">
    <div class="hero-badge">
      Patented in the US &amp; China
    </div>
    <h1>Pioneering <em>Non-Invasive</em> Eye Care Solutions</h1>
    <p class="hero-sub">A patented ophthalmic formulation poised to transform cataract treatment for 94 million patients worldwide — where no FDA-approved pharmacological alternative exists today.</p>
    <div class="hero-actions">
      <a href="#solution" class="btn-primary">Discover Opcure</a>
      <a href="#contact" class="btn-secondary">Get in Touch</a>
    </div>
  </div>
  <div class="hero-scroll">
    <div class="hero-scroll-line"></div>
    Scroll
  </div>
</section>

<!-- ===== THE PROBLEM ===== -->
<section class="problem" id="problem">
  <div class="container">
    <div class="problem-grid">
      <div class="problem-text">
        <div class="section-label reveal">The Problem</div>
        <h2 class="section-title reveal reveal-delay-1">Cataract — <br>The Silent Epidemic</h2>
        <p class="section-desc reveal reveal-delay-2">Cataracts remain the leading cause of blindness worldwide. An estimated 17 million people were bilaterally blind from cataracts in 2020, representing about 35% of all global cases of blindness.</p>
        <div class="problem-quote reveal reveal-delay-3">
          <p>So far, the only effective treatment for cataracts is surgery. However, accessibility and cost remain significant barriers. The FDA has not yet approved any non-surgical pharmacological drug to prevent, delay, or cure cataracts.</p>
        </div>
      </div>
      <div class="problem-stats">
        <div class="stat-item reveal reveal-delay-1">
          <div class="stat-number" data-target="1" data-suffix="B">0</div>
          <div class="stat-label">People globally have a vision impairment that could have been prevented or has yet to be addressed</div>
        </div>
        <div class="stat-item reveal reveal-delay-2">
          <div class="stat-number" data-target="94" data-suffix="M">0</div>
          <div class="stat-label">Suffer from cataracts worldwide</div>
        </div>
        <div class="stat-item reveal reveal-delay-3">
          <div class="stat-number" data-target="17" data-suffix="M">0</div>
          <div class="stat-label">Bilaterally blind from cataracts — about 35% of all global blindness</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ===== CURRENT SOLUTION GAP ===== -->
<section class="current-solution">
  <div class="container">
    <div class="section-label reveal">The Gap</div>
    <h2 class="section-title reveal reveal-delay-1">No Approved Alternative to Surgery</h2>
    <p class="section-desc reveal reveal-delay-2">Despite the enormous global burden, cataract patients today face a stark reality.</p>
    <div class="gap-cards">
      <div class="gap-card reveal reveal-delay-2">
        <div class="gap-card-icon">
          <svg viewBox="0 0 24 24"><path d="M12 22c5.523 0 10-4.477 10-10S17.523 2 12 2 2 6.477 2 12s4.477 10 10 10z"/><path d="M15 9l-6 6M9 9l6 6"/></svg>
        </div>
        <h4>Surgery Only</h4>
        <p>Invasive surgery remains the sole effective treatment — a significant barrier for millions.</p>
      </div>
      <div class="gap-card reveal reveal-delay-3">
        <div class="gap-card-icon">
          <svg viewBox="0 0 24 24"><path d="M12 2v20M2 12h20"/><circle cx="12" cy="12" r="10"/></svg>
        </div>
        <h4>Accessibility Crisis</h4>
        <p>Cost and limited access to surgical facilities leave countless patients untreated globally.</p>
      </div>
      <div class="gap-card reveal reveal-delay-4">
        <div class="gap-card-icon">
          <svg viewBox="0 0 24 24"><path d="M9 12l2 2 4-4"/><path d="M21 12a9 9 0 11-18 0 9 9 0 0118 0z"/></svg>
        </div>
        <h4>No FDA Drug</h4>
        <p>The FDA has not yet approved any pharmacological drug to prevent, delay, or cure cataracts.</p>
      </div>
    </div>
  </div>
</section>

<div class="section-divider"></div>

<!-- ===== OUR SOLUTION ===== -->
<section class="solution" id="solution">
  <div class="container">
    <div class="solution-header">
      <div class="section-label reveal">Our Solution</div>
      <h2 class="section-title reveal reveal-delay-1">A New Dawn in<br>Cataract Treatment</h2>
    </div>

    <div class="solution-desc-block reveal reveal-delay-2">
      <p><strong>Opcure</strong> is an ophthalmic formulation — <strong>eye drops</strong> with therapeutically effective concentrations of a zinc compound and an antihistamine — <strong>patented in the US and China</strong>, with pending patents in Canada, Europe, and India.</p>
    </div>

    <div class="benefits-grid">
      <div class="benefit-card reveal reveal-delay-1">
        <span class="benefit-icon">🎯</span>
        <h4>Effective</h4>
        <p>Out of 230 volunteers, 90% demonstrated positive results in our observational study.</p>
        <span class="benefit-highlight">90% positive results</span>
      </div>
      <div class="benefit-card reveal reveal-delay-2">
        <span class="benefit-icon">🛡️</span>
        <h4>Safe</h4>
        <p>The active ingredients have a well-established safety profile backed by years of clinical use.</p>
        <span class="benefit-highlight">Clinically proven ingredients</span>
      </div>
      <div class="benefit-card reveal reveal-delay-3">
        <span class="benefit-icon">💧</span>
        <h4>Easy to Use</h4>
        <p>Self-administered eye drops, applied four times daily. No surgical intervention required.</p>
        <span class="benefit-highlight">Self-administered</span>
      </div>
      <div class="benefit-card reveal reveal-delay-4">
        <span class="benefit-icon">✦</span>
        <h4>Affordable</h4>
        <p>A highly cost-effective alternative to cataract surgery for eligible patients worldwide.</p>
        <span class="benefit-highlight">Cost-effective</span>
      </div>
    </div>
  </div>
</section>

<!-- ===== MARKET ===== -->
<section class="market" id="market">
  <div class="container">
    <div class="market-header">
      <div class="section-label reveal">Market Opportunity</div>
      <h2 class="section-title reveal reveal-delay-1">A Multi-Billion Dollar<br>Global Market</h2>
      <p class="section-desc reveal reveal-delay-2">The cataract treatment market represents one of the largest opportunities in ophthalmology — and Opcure's patent portfolio covers the majority of it.</p>
    </div>

    <div class="market-grid reveal reveal-delay-2">
      <div class="market-card">
        <div class="number">$11.6<span class="number-suffix">B</span></div>
        <div class="label">Current estimated global market for cataract treatments</div>
      </div>
      <div class="market-card">
        <div class="number">$9.6<span class="number-suffix">B</span></div>
        <div class="label">Current global market for cataract surgeries</div>
      </div>
      <div class="market-card">
        <div class="number">$2<span class="number-suffix">B</span></div>
        <div class="label">Estimated global market for non-invasive cataract treatments</div>
      </div>
    </div>

    <div class="market-row-2 reveal reveal-delay-3">
      <div class="market-card">
        <div class="number">94<span class="number-suffix">M</span></div>
        <div class="label">Cataract patients globally</div>
      </div>
      <div class="market-card">
        <div class="number">75<span class="number-suffix">%</span></div>
        <div class="label">Opcure's patent portfolio provides legal protection for the majority of the global market</div>
      </div>
    </div>
  </div>
</section>

<!-- ===== WHY OPCURE ===== -->
<section class="why-opcure" id="why">
  <div class="container">
    <div class="section-label reveal">Investment Highlights</div>
    <h2 class="section-title reveal reveal-delay-1">Why Opcure</h2>
    <p class="section-desc reveal reveal-delay-2">A compelling opportunity at the intersection of innovation, impact, and returns.</p>

    <div class="why-grid">
      <div class="why-card reveal reveal-delay-1">
        <div class="why-card-number">01</div>
        <h4>Global Interest</h4>
        <p>Two global leaders in ophthalmology have expressed interest through their external innovation units in the U.S. and Europe, contingent on receiving additional clinical study results.</p>
      </div>
      <div class="why-card reveal reveal-delay-2">
        <div class="why-card-number">02</div>
        <h4>Business Partnership</h4>
        <p>The primary goal is to secure a licensing partnership with a multinational pharmaceutical company in exchange for royalty revenues.</p>
      </div>
      <div class="why-card reveal reveal-delay-3">
        <div class="why-card-number">03</div>
        <h4>Return on Investment</h4>
        <p>ROI is expected in three stages: an upfront lump sum payment from the licensing agreement (anticipated 2027), followed by milestone-based payments, then ongoing royalties from product sales starting 2033–2034 after FDA approval.</p>
      </div>
      <div class="why-card reveal reveal-delay-4">
        <div class="why-card-number">04</div>
        <h4>Early Investment Advantage</h4>
        <p>By investing in Opcure, you invest in a company that owns the patent rights and its future revenue streams — at the earliest and most advantageous stage.</p>
      </div>
      <div class="why-card reveal reveal-delay-5" style="grid-column: 1 / -1;">
        <div class="why-card-number">05</div>
        <h4>Social Impact</h4>
        <p>This investment opportunity offers the potential for remarkable financial returns by pioneering a new treatment class globally, while also making a significant positive impact on the lives of millions worldwide.</p>
      </div>
    </div>
  </div>
</section>

<!-- ===== TEAM ===== -->
<section class="team" id="team">
  <div class="container">
    <div class="team-header">
      <div class="section-label reveal">Our Team</div>
      <h2 class="section-title reveal reveal-delay-1">Global Expertise,<br>Unified Vision</h2>
    </div>

    <div class="team-stats reveal reveal-delay-2">
      <div class="team-stat">
        <div class="number">12</div>
        <div class="label">Team Members</div>
      </div>
      <div class="team-stat">
        <div class="number">3</div>
        <div class="label">Continents</div>
      </div>
      <div class="team-stat">
        <div class="number">5</div>
        <div class="label">At Top Global Firms</div>
      </div>
    </div>

    <div class="expertise-tags reveal reveal-delay-3">
      <span class="expertise-tag">Pharmaceutical Sciences</span>
      <span class="expertise-tag">Ophthalmology</span>
      <span class="expertise-tag">Management Consulting</span>
      <span class="expertise-tag">Entrepreneurship</span>
      <span class="expertise-tag">Business Management</span>
      <span class="expertise-tag">Medical Affairs</span>
      <span class="expertise-tag">Clinical Research</span>
      <span class="expertise-tag">Business Analytics</span>
      <span class="expertise-tag">Sales &amp; Business Development</span>
    </div>
  </div>
</section>

<div class="section-divider"></div>

<!-- ===== ROADMAP ===== -->
<section class="roadmap" id="roadmap">
  <div class="container">
    <div class="roadmap-header">
      <div class="section-label reveal">Our Future Path</div>
      <h2 class="section-title reveal reveal-delay-1">Roadmap to Market</h2>
      <p class="section-desc reveal reveal-delay-2">A clear, milestone-driven path from clinical validation to global licensing.</p>
    </div>

    <div class="timeline">
      <div class="timeline-item reveal">
        <div class="timeline-dot"></div>
        <div class="timeline-date">Q2 2026</div>
        <div class="timeline-title">1st Investment Round</div>
        <div class="timeline-desc">Completing an investment round to fund the extension of global patent protection and the implementation of a clinical study (RCT).</div>
      </div>
      <div class="timeline-item reveal reveal-delay-1">
        <div class="timeline-dot"></div>
        <div class="timeline-date">Q2 2026</div>
        <div class="timeline-title">Opcure, LLC</div>
        <div class="timeline-desc">An LLC will be established, with the patent assigned to it, which will be the recipient of future revenue rights.</div>
      </div>
      <div class="timeline-item reveal reveal-delay-2">
        <div class="timeline-dot"></div>
        <div class="timeline-date">Q3–Q4 2026</div>
        <div class="timeline-title">Randomized Clinical Trial</div>
        <div class="timeline-desc">Conducting a double-blinded, randomized clinical trial (RCT). The study follows a protocol developed with a leading London-based clinical research firm.</div>
      </div>
      <div class="timeline-item reveal reveal-delay-3">
        <div class="timeline-dot"></div>
        <div class="timeline-date">Q4 2026</div>
        <div class="timeline-title">Preliminary Results</div>
        <div class="timeline-desc">Analyzing, assessing, and documenting the study results, which will then be shared with interested multinational pharmaceutical companies.</div>
      </div>
      <div class="timeline-item reveal reveal-delay-4">
        <div class="timeline-dot"></div>
        <div class="timeline-date">Q1 2027</div>
        <div class="timeline-title">Securing a Deal</div>
        <div class="timeline-desc">Securing a patent licensing agreement with a leading multinational pharmaceutical company, which will conduct the necessary studies and bring the product to global markets.</div>
      </div>
    </div>
  </div>
</section>

<!-- ===== CONTACT ===== -->
<section class="contact" id="contact">
  <div class="contact-content">
    <div class="contact-logo reveal">
      <svg viewBox="0 0 50 50" xmlns="http://www.w3.org/2000/svg">
        <circle cx="25" cy="22" r="20" fill="white"/>
        <circle cx="17" cy="20" r="12.5" fill="#0b1120"/>
      </svg>
    </div>
    <h2 class="reveal reveal-delay-1">Let's Shape the Future<br>of <em>Eye Care</em> Together</h2>
    <p class="contact-sub reveal reveal-delay-2">For inquiries, investment opportunities, or partnerships</p>
    <a href="mailto:team@opcure.net" class="contact-email reveal reveal-delay-3">
      <svg viewBox="0 0 24 24"><rect x="2" y="4" width="20" height="16" rx="2"/><path d="M22 4L12 13 2 4"/></svg>
      team@opcure.net
    </a>
  </div>
</section>

<!-- ===== FOOTER ===== -->
<footer>
  <p>&copy; 2026 Opcure. All rights reserved.</p>
  <div class="footer-links">
    <a href="mailto:team@opcure.net">Contact</a>
  </div>
</footer>

<script>
// Scroll-reveal animations
const observerOptions = { threshold: 0.1, rootMargin: '0px 0px -60px 0px' };
const observer = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.classList.add('visible');
      observer.unobserve(entry.target);
    }
  });
}, observerOptions);

document.querySelectorAll('.reveal').forEach(el => observer.observe(el));

// Navbar scroll effect
window.addEventListener('scroll', () => {
  document.getElementById('navbar').classList.toggle('scrolled', window.scrollY > 50);
});

// Animated counters
const counterObserver = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      const el = entry.target;
      const target = parseFloat(el.dataset.target);
      const suffix = el.dataset.suffix || '';
      const duration = 2000;
      const start = performance.now();

      function update(now) {
        const progress = Math.min((now - start) / duration, 1);
        const eased = 1 - Math.pow(1 - progress, 3);
        const current = target * eased;
        el.textContent = (target < 10 ? current.toFixed(target % 1 === 0 ? 0 : 1) : Math.floor(current)) + suffix;
        if (progress < 1) requestAnimationFrame(update);
      }
      requestAnimationFrame(update);
      counterObserver.unobserve(el);
    }
  });
}, { threshold: 0.5 });

document.querySelectorAll('[data-target]').forEach(el => counterObserver.observe(el));

// Smooth scroll for anchor links
document.querySelectorAll('a[href^="#"]').forEach(anchor => {
  anchor.addEventListener('click', function(e) {
    e.preventDefault();
    const target = document.querySelector(this.getAttribute('href'));
    if (target) {
      target.scrollIntoView({ behavior: 'smooth', block: 'start' });
      document.getElementById('navLinks').classList.remove('open');
    }
  });
});
</script>
</body>
</html>
