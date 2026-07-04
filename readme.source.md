<!-- ═══════════════════════════════════════════════════════════════════ -->
<!-- HERO SECTION — Animated banner with name, subtitle, floating orbs -->
<!-- ═══════════════════════════════════════════════════════════════════ -->

```aura width=860 height=320
<div style={{
  width: '100%', height: '100%', background: '#06060a',
  display: 'flex', flexDirection: 'column', alignItems: 'center', justifyContent: 'center',
  fontFamily: 'Inter, sans-serif', position: 'relative', overflow: 'hidden',
  borderRadius: 20, border: '1px solid rgba(0,229,255,0.08)'
}}>

  <style>{`
    @keyframes hero-orb-a { 0%, 100% { transform: translate(0,0); opacity: 0.55; } 50% { transform: translate(40px,-30px); opacity: 0.85; } }
    @keyframes hero-orb-b { 0%, 100% { transform: translate(0,0); opacity: 0.45; } 50% { transform: translate(-35px,25px); opacity: 0.75; } }
    @keyframes hero-orb-c { 0%, 100% { transform: translate(0,0); opacity: 0.35; } 50% { transform: translate(25px,-40px); opacity: 0.65; } }
    @keyframes hero-orb-d { 0%, 100% { transform: translate(0,0); opacity: 0.40; } 50% { transform: translate(-20px,-15px); opacity: 0.70; } }
    @keyframes hero-ring { 0%, 100% { opacity: 0.04; } 50% { opacity: 0.14; } }
    @keyframes hero-ring-b { 0%, 100% { opacity: 0.03; } 50% { opacity: 0.10; } }
    @keyframes hero-dot-spin { 0% { transform: rotate(0deg); } 100% { transform: rotate(360deg); } }
    @keyframes hero-line-scan { 0% { transform: translateY(-320px); } 100% { transform: translateY(320px); } }
    @keyframes hero-cursor { 0%, 100% { opacity: 1; } 49% { opacity: 1; } 50% { opacity: 0; } 99% { opacity: 0; } }
    #ho1 { animation: hero-orb-a 9s ease-in-out infinite; }
    #ho2 { animation: hero-orb-b 12s ease-in-out infinite 0.6s; }
    #ho3 { animation: hero-orb-c 8s ease-in-out infinite 1.5s; }
    #ho4 { animation: hero-orb-d 11s ease-in-out infinite 0.3s; }
    #ho5 { animation: hero-orb-a 10s ease-in-out infinite 2s; }
    #ho6 { animation: hero-orb-b 14s ease-in-out infinite 1s; }
    #hr1 { animation: hero-ring 9s ease-in-out infinite; }
    #hr2 { animation: hero-ring 9s ease-in-out infinite 1.5s; }
    #hr3 { animation: hero-ring-b 9s ease-in-out infinite 3s; }
    #hr4 { animation: hero-ring-b 10s ease-in-out infinite 4.5s; }
    #hdot { animation: hero-dot-spin 24s linear infinite; }
    #hscan { animation: hero-line-scan 6s linear infinite; }
    #hcur { animation: hero-cursor 1.1s step-end infinite; }
  `}</style>

  <svg width="860" height="320" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="hg1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(0,229,255,0.50)" />
        <stop offset="60%" stopColor="rgba(0,229,255,0.12)" />
        <stop offset="100%" stopColor="rgba(0,229,255,0)" />
      </radialGradient>
      <radialGradient id="hg2" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(139,92,246,0.55)" />
        <stop offset="55%" stopColor="rgba(139,92,246,0.15)" />
        <stop offset="100%" stopColor="rgba(139,92,246,0)" />
      </radialGradient>
      <radialGradient id="hg3" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(51,102,255,0.45)" />
        <stop offset="60%" stopColor="rgba(51,102,255,0.10)" />
        <stop offset="100%" stopColor="rgba(51,102,255,0)" />
      </radialGradient>
      <radialGradient id="hg4" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(236,72,153,0.30)" />
        <stop offset="70%" stopColor="rgba(236,72,153,0)" />
      </radialGradient>
      <radialGradient id="hg5" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(0,180,255,0.35)" />
        <stop offset="100%" stopColor="rgba(0,180,255,0)" />
      </radialGradient>
      <radialGradient id="hg6" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(168,85,247,0.40)" />
        <stop offset="100%" stopColor="rgba(168,85,247,0)" />
      </radialGradient>
      <linearGradient id="hscan-g" x1="0" y1="0" x2="0" y2="1">
        <stop offset="0%" stopColor="rgba(0,229,255,0)" />
        <stop offset="45%" stopColor="rgba(0,229,255,0.04)" />
        <stop offset="50%" stopColor="rgba(0,229,255,0.12)" />
        <stop offset="55%" stopColor="rgba(0,229,255,0.04)" />
        <stop offset="100%" stopColor="rgba(0,229,255,0)" />
      </linearGradient>
    </defs>

    <ellipse id="ho1" cx="120" cy="280" rx="280" ry="200" fill="url(#hg1)" />
    <ellipse id="ho2" cx="740" cy="60"  rx="250" ry="190" fill="url(#hg2)" />
    <ellipse id="ho3" cx="430" cy="310" rx="200" ry="160" fill="url(#hg3)" />
    <ellipse id="ho4" cx="680" cy="290" rx="180" ry="140" fill="url(#hg4)" />
    <ellipse id="ho5" cx="250" cy="40"  rx="220" ry="160" fill="url(#hg5)" />
    <ellipse id="ho6" cx="500" cy="60"  rx="160" ry="130" fill="url(#hg6)" />

    <circle id="hr1" cx="430" cy="160" r="55"  fill="none" stroke="rgba(0,229,255,0.7)" strokeWidth="0.5" />
    <circle id="hr2" cx="430" cy="160" r="100" fill="none" stroke="rgba(139,92,246,0.6)" strokeWidth="0.5" />
    <circle id="hr3" cx="430" cy="160" r="155" fill="none" stroke="rgba(51,102,255,0.5)" strokeWidth="0.4" />
    <circle id="hr4" cx="430" cy="160" r="220" fill="none" stroke="rgba(0,229,255,0.3)" strokeWidth="0.3" />

    <g id="hdot">
      <circle cx="430" cy="105" r="2" fill="rgba(0,229,255,0.6)" />
    </g>

    <rect id="hscan" x="0" y="0" width="860" height="320" fill="url(#hscan-g)" />
  </svg>

  <div style={{ position: 'relative', display: 'flex', flexDirection: 'column', alignItems: 'center', zIndex: 10 }}>
    <span style={{
      fontSize: 11, letterSpacing: 6, textTransform: 'uppercase',
      color: 'rgba(0,229,255,0.50)', fontWeight: 300, marginBottom: 14
    }}>AI Engineer &amp; Quantitative Developer</span>

    <span style={{
      fontSize: 52, fontWeight: 800, letterSpacing: -2, lineHeight: 1,
      color: '#ffffff',
      textShadow: '0 0 60px rgba(0,229,255,0.25), 0 0 120px rgba(139,92,246,0.15)'
    }}>gaurav kumar pandey</span>

    <div style={{ display: 'flex', alignItems: 'center', marginTop: 16, gap: 6 }}>
      <span style={{
        fontSize: 15, color: 'rgba(180,190,255,0.70)', fontWeight: 400,
        letterSpacing: 0.5, fontFamily: 'monospace'
      }}>> Spring Boot · MLOps · Graph Neural Networks · Systems Security</span>
      <span id="hcur" style={{ fontSize: 15, color: 'rgba(0,229,255,0.7)', fontFamily: 'monospace' }}>_</span>
    </div>

    <div style={{ display: 'flex', gap: 8, marginTop: 24, flexWrap: 'wrap', justifyContent: 'center' }}>
      {['Quant Systems', 'Graph ML', 'Systems Security', 'Kotlin / Java'].map(function(tag, i) {
        return (
          <span key={i} style={{
            padding: '5px 14px', borderRadius: 100,
            background: 'rgba(0,229,255,0.04)',
            border: '1px solid rgba(0,229,255,0.12)',
            color: 'rgba(0,229,255,0.65)', fontSize: 11, fontWeight: 500, letterSpacing: 0.8
          }}>{tag}</span>
        );
      })}
    </div>
  </div>
</div>
```

<!-- ═══════════════════════════════════════════════════════════════ -->
<!-- TECH STACK SECTION — Animated glowing technology cards         -->
<!-- ═══════════════════════════════════════════════════════════════ -->

```aura width=860 height=300
<div style={{
  width: '100%', height: '100%', background: '#06060a',
  display: 'flex', flexDirection: 'column', alignItems: 'center', justifyContent: 'center',
  fontFamily: 'Inter, sans-serif', position: 'relative', overflow: 'hidden',
  borderRadius: 20, border: '1px solid rgba(139,92,246,0.08)'
}}>

  <style>{`
    @keyframes ts-orb1 { 0%, 100% { transform: translate(0,0); opacity: 0.4; } 50% { transform: translate(30px,-20px); opacity: 0.7; } }
    @keyframes ts-orb2 { 0%, 100% { transform: translate(0,0); opacity: 0.35; } 50% { transform: translate(-25px,15px); opacity: 0.6; } }
    @keyframes ts-pulse { 0%, 100% { opacity: 0.7; } 50% { opacity: 1; } }
    #tso1 { animation: ts-orb1 10s ease-in-out infinite; }
    #tso2 { animation: ts-orb2 13s ease-in-out infinite 1s; }
    #tso3 { animation: ts-orb1 9s ease-in-out infinite 2s; }
    #tsp1 { animation: ts-pulse 3s ease-in-out infinite; }
    #tsp2 { animation: ts-pulse 3s ease-in-out infinite 0.5s; }
    #tsp3 { animation: ts-pulse 3s ease-in-out infinite 1s; }
    #tsp4 { animation: ts-pulse 3s ease-in-out infinite 1.5s; }
    #tsp5 { animation: ts-pulse 3s ease-in-out infinite 2s; }
    #tsp6 { animation: ts-pulse 3s ease-in-out infinite 0.3s; }
    #tsp7 { animation: ts-pulse 3s ease-in-out infinite 0.8s; }
    #tsp8 { animation: ts-pulse 3s ease-in-out infinite 1.3s; }
    #tsp9 { animation: ts-pulse 3s ease-in-out infinite 1.8s; }
    #tsp10 { animation: ts-pulse 3s ease-in-out infinite 0.2s; }
  `}</style>

  <svg width="860" height="300" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="tsg1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(139,92,246,0.35)" />
        <stop offset="100%" stopColor="rgba(139,92,246,0)" />
      </radialGradient>
      <radialGradient id="tsg2" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(0,229,255,0.30)" />
        <stop offset="100%" stopColor="rgba(0,229,255,0)" />
      </radialGradient>
      <radialGradient id="tsg3" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(51,102,255,0.30)" />
        <stop offset="100%" stopColor="rgba(51,102,255,0)" />
      </radialGradient>
    </defs>
    <ellipse id="tso1" cx="150" cy="220" rx="200" ry="160" fill="url(#tsg1)" />
    <ellipse id="tso2" cx="700" cy="50"  rx="180" ry="140" fill="url(#tsg2)" />
    <ellipse id="tso3" cx="430" cy="240" rx="160" ry="120" fill="url(#tsg3)" />
  </svg>

  <span style={{
    fontSize: 11, letterSpacing: 5, textTransform: 'uppercase',
    color: 'rgba(139,92,246,0.50)', fontWeight: 300, marginBottom: 20, zIndex: 10
  }}>tech stack</span>

  <div style={{ display: 'flex', flexWrap: 'wrap', gap: 12, justifyContent: 'center', zIndex: 10, maxWidth: 760, padding: '0 20px' }}>
    {[
      { name: 'Kotlin', color: '127,122,255' },
      { name: 'Java', color: '224,119,38' },
      { name: 'Python', color: '55,118,171' },
      { name: 'Spring Boot', color: '109,179,63' },
      { name: 'PyTorch', color: '238,76,44' },
      { name: 'Neo4j', color: '0,143,188' },
      { name: 'PostgreSQL', color: '51,103,145' },
      { name: 'Kafka', color: '255,255,255' },
      { name: 'Docker', color: '13,183,237' },
      { name: 'AWS', color: '255,153,0' }
    ].map(function(tech, i) {
      return (
        <div key={i} id={'tsp' + (i + 1)} style={{
          display: 'flex', alignItems: 'center', gap: 8,
          padding: '10px 20px', borderRadius: 12,
          background: 'rgba(' + tech.color + ',0.06)',
          border: '1px solid rgba(' + tech.color + ',0.18)',
        }}>
          <div style={{
            width: 8, height: 8, borderRadius: 4,
            background: 'rgba(' + tech.color + ',0.8)',
            boxShadow: '0 0 8px rgba(' + tech.color + ',0.5)'
          }} />
          <span style={{
            fontSize: 13, fontWeight: 500,
            color: 'rgba(255,255,255,0.75)', letterSpacing: 0.3
          }}>{tech.name}</span>
        </div>
      );
    })}
  </div>
</div>
```

<!-- ═══════════════════════════════════════════════════════════════ -->
<!-- ABOUT ME SECTION — Terminal-style glassmorphism panel          -->
<!-- ═══════════════════════════════════════════════════════════════ -->

```aura width=860 height=240
<div style={{
  width: '100%', height: '100%', background: '#06060a',
  display: 'flex', fontFamily: 'Inter, sans-serif',
  position: 'relative', overflow: 'hidden',
  borderRadius: 20, border: '1px solid rgba(51,102,255,0.08)'
}}>

  <style>{`
    @keyframes ab-orb1 { 0%, 100% { transform: translate(0,0); opacity: 0.5; } 50% { transform: translate(25px,-18px); opacity: 0.8; } }
    @keyframes ab-orb2 { 0%, 100% { transform: translate(0,0); opacity: 0.4; } 50% { transform: translate(-20px,14px); opacity: 0.65; } }
    @keyframes ab-cursor { 0%, 100% { opacity: 1; } 49% { opacity: 1; } 50% { opacity: 0; } 99% { opacity: 0; } }
    @keyframes ab-line-glow { 0%, 100% { opacity: 0.15; } 50% { opacity: 0.35; } }
    #abo1 { animation: ab-orb1 9s ease-in-out infinite; }
    #abo2 { animation: ab-orb2 11s ease-in-out infinite 1.5s; }
    #abcur { animation: ab-cursor 1.1s step-end infinite; }
    #abline { animation: ab-line-glow 4s ease-in-out infinite; }
  `}</style>

  <svg width="860" height="240" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="abg1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(0,229,255,0.35)" />
        <stop offset="100%" stopColor="rgba(0,229,255,0)" />
      </radialGradient>
      <radialGradient id="abg2" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(139,92,246,0.30)" />
        <stop offset="100%" stopColor="rgba(139,92,246,0)" />
      </radialGradient>
    </defs>
    <ellipse id="abo1" cx="80"  cy="200" rx="200" ry="150" fill="url(#abg1)" />
    <ellipse id="abo2" cx="780" cy="60"  rx="180" ry="140" fill="url(#abg2)" />
    <line id="abline" x1="44" y1="70" x2="44" y2="200" stroke="rgba(0,229,255,0.25)" strokeWidth="1" />
  </svg>

  <div style={{
    position: 'relative', display: 'flex', flexDirection: 'column',
    justifyContent: 'center', padding: '0 56px', zIndex: 10, gap: 10, flex: 1
  }}>
    <span style={{
      fontSize: 11, letterSpacing: 5, textTransform: 'uppercase',
      color: 'rgba(51,102,255,0.50)', fontWeight: 300, marginBottom: 6
    }}>about</span>

    <span style={{ fontSize: 22, fontWeight: 700, color: '#ffffff', lineHeight: 1.3 }}>
      Building concurrent backend systems and machine learning models at scale
    </span>

    <span style={{
      fontSize: 14, color: 'rgba(255,255,255,0.50)', lineHeight: 1.7,
      maxWidth: 680
    }}>
      I am a Software Engineer and Quantitative Developer. I specialize in building mission-critical concurrent backend systems (Kotlin/Java &amp; Spring Boot), developing production-grade machine learning applications (Graph Neural Networks with PyTorch, autonomous agents, and RAG architectures), and writing highly performant mathematical/financial modeling systems.
    </span>

    <div style={{ display: 'flex', alignItems: 'center', marginTop: 8 }}>
      <span style={{ fontSize: 13, color: 'rgba(0,229,255,0.45)', fontFamily: 'monospace' }}>
        {'>'} AI/ML · quantitative systems · systems security · mobile reversing
      </span>
      <span id="abcur" style={{ fontSize: 13, color: 'rgba(0,229,255,0.6)', fontFamily: 'monospace', marginLeft: 1 }}>_</span>
    </div>
  </div>
</div>
```

<!-- ═══════════════════════════════════════════════════════════════════ -->
<!-- FEATURED PROJECTS — Rich project cards with animated glow borders -->
<!-- ═══════════════════════════════════════════════════════════════════ -->

```aura width=860 height=566
<div style={{
  width: '100%', height: '100%', background: '#06060a',
  display: 'flex', flexDirection: 'column', alignItems: 'center',
  fontFamily: 'Inter, sans-serif', position: 'relative', overflow: 'hidden',
  borderRadius: 20, border: '1px solid rgba(0,229,255,0.06)', padding: '28px 0'
}}>

  <style>{`
    @keyframes pj-orb1 { 0%, 100% { transform: translate(0,0); opacity: 0.3; } 50% { transform: translate(35px,-25px); opacity: 0.55; } }
    @keyframes pj-orb2 { 0%, 100% { transform: translate(0,0); opacity: 0.25; } 50% { transform: translate(-30px,20px); opacity: 0.5; } }
    @keyframes pj-orb3 { 0%, 100% { transform: translate(0,0); opacity: 0.3; } 50% { transform: translate(20px,15px); opacity: 0.5; } }
    @keyframes pj-status { 0%, 100% { opacity: 0.5; } 50% { opacity: 1; } }
    #pjo1 { animation: pj-orb1 10s ease-in-out infinite; }
    #pjo2 { animation: pj-orb2 13s ease-in-out infinite 1s; }
    #pjo3 { animation: pj-orb3 11s ease-in-out infinite 2s; }
    #pjs1 { animation: pj-status 2s ease-in-out infinite; }
    #pjs2 { animation: pj-status 2s ease-in-out infinite 0.4s; }
    #pjs3 { animation: pj-status 2s ease-in-out infinite 0.8s; }
    #pjs4 { animation: pj-status 2s ease-in-out infinite 1.2s; }
    #pjs5 { animation: pj-status 2s ease-in-out infinite 1.6s; }
    #pjs6 { animation: pj-status 2s ease-in-out infinite 2.0s; }
  `}</style>

  <svg width="860" height="566" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="pjg1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(0,229,255,0.20)" />
        <stop offset="100%" stopColor="rgba(0,229,255,0)" />
      </radialGradient>
      <radialGradient id="pjg2" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(139,92,246,0.22)" />
        <stop offset="100%" stopColor="rgba(139,92,246,0)" />
      </radialGradient>
      <radialGradient id="pjg3" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(236,72,153,0.18)" />
        <stop offset="100%" stopColor="rgba(236,72,153,0)" />
      </radialGradient>
    </defs>
    <ellipse id="pjo1" cx="100" cy="470" rx="220" ry="180" fill="url(#pjg1)" />
    <ellipse id="pjo2" cx="760" cy="100" rx="200" ry="160" fill="url(#pjg2)" />
    <ellipse id="pjo3" cx="430" cy="520" rx="180" ry="140" fill="url(#pjg3)" />
  </svg>

  <span style={{
    fontSize: 11, letterSpacing: 5, textTransform: 'uppercase',
    color: 'rgba(0,229,255,0.45)', fontWeight: 300, marginBottom: 20, zIndex: 10
  }}>featured projects</span>

  <div style={{ display: 'flex', flexDirection: 'column', gap: 10, zIndex: 10, width: '100%', padding: '0 28px' }}>
    {[
      {
        title: 'Financial Fraud Graph Neural Network',
        desc: 'Heterogeneous GNN fraud detection modeling customer networks, Neo4j graph data, and low-latency Kafka predictions.',
        tech: 'PyTorch Geometric · Neo4j · Kafka · FastAPI',
        color: '0,229,255',
        statusId: 'pjs1'
      },
      {
        title: 'MCMC Options Trading &amp; Risk System',
        desc: 'Quantitative Bayesian parameter inference and Metropolis-Hastings options simulation hedged daily.',
        tech: 'Python · NumPy/SciPy · Pandas · FastAPI',
        color: '139,92,246',
        statusId: 'pjs2'
      },
      {
        title: 'AgentForge — AI Agent Framework',
        desc: 'Modular AI agent framework supporting tool execution loops, Websockets, and pgvector RAG.',
        tech: 'Kotlin · Spring Boot 3.x · pgvector · WebFlux',
        color: '51,102,255',
        statusId: 'pjs3'
      },
      {
        title: 'High-Concurrency Wallet Ledger',
        desc: 'ACID-compliant double-entry ledger with database pessimistic locking and API idempotency.',
        tech: 'Kotlin · Spring Boot 3.x · PostgreSQL · Gradle',
        color: '236,72,153',
        statusId: 'pjs4'
      },
      {
        title: 'CovertChat — Disguised Messenger',
        desc: 'Zero-knowledge disguised messenger with client-side Web Crypto AES-GCM-256 encryption.',
        tech: 'Python · Web Crypto API · JavaScript',
        color: '168,85,247',
        statusId: 'pjs5'
      },
      {
        title: 'APK Clone &amp; Repackage Engine',
        desc: 'Automated toolkit to decompile, patch, and repackage secure Android APKs for multi-app cloning.',
        tech: 'Python · Apktool · Smali · Apksigner',
        color: '0,180,255',
        statusId: 'pjs6'
      }
    ].map(function(project, i) {
      return (
        <div key={i} style={{
          display: 'flex', alignItems: 'center', padding: '14px 20px',
          background: 'rgba(255,255,255,0.02)',
          border: '1px solid rgba(' + project.color + ',0.12)',
          borderRadius: 12, gap: 14
        }}>
          <div id={project.statusId} style={{
            width: 8, height: 8, borderRadius: 4, flexShrink: 0,
            background: 'rgba(' + project.color + ',0.8)',
            boxShadow: '0 0 10px rgba(' + project.color + ',0.4)'
          }} />
          <div style={{ display: 'flex', flexDirection: 'column', gap: 3, flex: 1 }}>
            <span style={{ fontSize: 14, fontWeight: 600, color: '#ffffff', letterSpacing: 0.2 }}>
              {project.title}
            </span>
            <span style={{ fontSize: 11, color: 'rgba(255,255,255,0.40)', lineHeight: 1.4 }}>
              {project.desc}
            </span>
          </div>
          <span style={{
            fontSize: 10, color: 'rgba(' + project.color + ',0.55)',
            fontFamily: 'monospace', letterSpacing: 0.3, textAlign: 'right',
            flexShrink: 0, maxWidth: 200
          }}>{project.tech}</span>
        </div>
      );
    })}
  </div>
</div>
```

<!-- ═══════════════════════════════════════════════════════════════ -->
<!-- GITHUB STATS — Cohesive themed statistics                      -->
<!-- ═══════════════════════════════════════════════════════════════ -->

<p align="center">

![](https://github-readme-stats.vercel.app/api?username=Alwaysgaurav1&show_icons=true&theme=transparent&hide_border=true&title_color=00e5ff&text_color=8b9dc3&icon_color=8b5cf6&bg_color=00000000&ring_color=00e5ff)
![](https://github-readme-stats.vercel.app/api/top-langs/?username=Alwaysgaurav1&layout=compact&theme=transparent&hide_border=true&title_color=00e5ff&text_color=8b9dc3&bg_color=00000000)

</p>

<p align="center">

![](https://github-readme-streak-stats.herokuapp.com/?user=Alwaysgaurav1&theme=transparent&hide_border=true&ring=00e5ff&fire=8b5cf6&currStreakLabel=00e5ff&sideLabels=8b9dc3&currStreakNum=ffffff&sideNums=ffffff&dates=555555&stroke=1a1a2e)

</p>

<!-- ═══════════════════════════════════════════════════════════════ -->
<!-- CURRENT FOCUS — What I'm building and exploring                -->
<!-- ═══════════════════════════════════════════════════════════════ -->

```aura width=860 height=220
<div style={{
  width: '100%', height: '100%', background: '#06060a',
  display: 'flex', fontFamily: 'Inter, sans-serif',
  position: 'relative', overflow: 'hidden',
  borderRadius: 20, border: '1px solid rgba(139,92,246,0.08)'
}}>

  <style>{`
    @keyframes cf-orb1 { 0%, 100% { transform: translate(0,0); opacity: 0.35; } 50% { transform: translate(25px,-18px); opacity: 0.6; } }
    @keyframes cf-orb2 { 0%, 100% { transform: translate(0,0); opacity: 0.3; } 50% { transform: translate(-20px,14px); opacity: 0.55; } }
    @keyframes cf-dot { 0%, 100% { opacity: 0.4; } 50% { opacity: 1; } }
    #cfo1 { animation: cf-orb1 10s ease-in-out infinite; }
    #cfo2 { animation: cf-orb2 12s ease-in-out infinite 1s; }
    #cfd1 { animation: cf-dot 2.5s ease-in-out infinite; }
    #cfd2 { animation: cf-dot 2.5s ease-in-out infinite 0.4s; }
    #cfd3 { animation: cf-dot 2.5s ease-in-out infinite 0.8s; }
    #cfd4 { animation: cf-dot 2.5s ease-in-out infinite 1.2s; }
    #cfd5 { animation: cf-dot 2.5s ease-in-out infinite 1.6s; }
    #cfd6 { animation: cf-dot 2.5s ease-in-out infinite 2.0s; }
  `}</style>

  <svg width="860" height="220" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="cfg1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(139,92,246,0.30)" />
        <stop offset="100%" stopColor="rgba(139,92,246,0)" />
      </radialGradient>
      <radialGradient id="cfg2" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(0,229,255,0.25)" />
        <stop offset="100%" stopColor="rgba(0,229,255,0)" />
      </radialGradient>
    </defs>
    <ellipse id="cfo1" cx="120" cy="190" rx="200" ry="150" fill="url(#cfg1)" />
    <ellipse id="cfo2" cx="740" cy="50"  rx="180" ry="140" fill="url(#cfg2)" />
  </svg>

  <div style={{
    position: 'relative', display: 'flex', flexDirection: 'column',
    padding: '24px 40px', zIndex: 10, flex: 1, justifyContent: 'center'
  }}>
    <span style={{
      fontSize: 11, letterSpacing: 5, textTransform: 'uppercase',
      color: 'rgba(139,92,246,0.50)', fontWeight: 300, marginBottom: 16
    }}>currently exploring</span>

    <div style={{ display: 'flex', flexWrap: 'wrap', gap: 10 }}>
      {[
        { label: 'Graph Neural Networks', color: '0,229,255', id: 'cfd1' },
        { label: 'Quantitative Trading', color: '139,92,246', id: 'cfd2' },
        { label: 'Multi-Agent Frameworks', color: '51,102,255', id: 'cfd3' },
        { label: 'Spring Boot Microservices', color: '236,72,153', id: 'cfd4' },
        { label: 'Explainable AI (XAI)', color: '168,85,247', id: 'cfd5' },
        { label: 'Systems Security &amp; E2EE', color: '0,180,255', id: 'cfd6' },
      ].map(function(item, i) {
        return (
          <div key={i} style={{
            display: 'flex', alignItems: 'center', gap: 8,
            padding: '8px 16px', borderRadius: 10,
            background: 'rgba(' + item.color + ',0.04)',
            border: '1px solid rgba(' + item.color + ',0.12)'
          }}>
            <div id={item.id} style={{
              width: 6, height: 6, borderRadius: 3,
              background: 'rgba(' + item.color + ',0.9)',
              boxShadow: '0 0 8px rgba(' + item.color + ',0.5)'
            }} />
            <span style={{
              fontSize: 12, color: 'rgba(255,255,255,0.60)',
              fontWeight: 500, letterSpacing: 0.3
            }}>{item.label}</span>
          </div>
        );
      })}
    </div>
  </div>
</div>
```

<!-- ═══════════════════════════════════════════════════════════════ -->
<!-- SOCIAL LINKS — Custom SocialMediaButton components             -->
<!-- ═══════════════════════════════════════════════════════════════ -->

```aura width=130 height=44 link="https://github.com/Alwaysgaurav1" inline align=center
<div style={{
  width: 130, height: 44, background: '#0a0a12',
  display: 'flex', alignItems: 'center', justifyContent: 'center', gap: 8,
  borderRadius: 12, border: '1px solid rgba(0,229,255,0.2)',
  fontFamily: 'Inter, sans-serif'
}}>
  <svg width="18" height="18" viewBox="0 0 24 24" style={{ display: 'flex' }}>
    <path fill="#e8eef8" d="M12 .5C5.86.5.5 5.86.5 12c0 5.25 3.4 9.7 8.12 11.28.6.11.82-.26.82-.58 0-.28-.02-1.23-.02-2.23-3.02.56-3.83-.74-4.08-1.4-.14-.35-.73-1.41-1.25-1.69-.43-.23-1.04-.8-.01-.81.96-.02 1.65.88 1.88 1.26 1.1 1.85 2.85 1.33 3.54 1.01.11-.79.42-1.34.76-1.64-2.66-.31-5.45-1.33-5.45-5.92 0-1.31.47-2.38 1.24-3.22-.12-.31-.54-1.54.12-3.2 0 0 1.01-.32 3.3 1.23.96-.27 1.99-.4 3.01-.4s2.05.14 3.02.4c2.28-1.55 3.29-1.23 3.29-1.23.66 1.66.24 2.89.12 3.2.77.84 1.23 1.91 1.23 3.22 0 4.61-2.8 5.62-5.49 5.92.43.37.81 1.1.81 2.22 0 1.6-.02 2.89-.02 3.29 0 .32.22.69.83.57A11.5 11.5 0 0 0 23.5 12C23.5 5.86 18.14.5 12 .5Z"/>
  </svg>
  <span style={{ fontSize: 14, color: '#c0c8e0', fontWeight: 500 }}>GitHub</span>
</div>
```

```aura width=140 height=44 link="https://www.linkedin.com/in/gauravkumarpandey/" inline align=center
<div style={{
  width: 140, height: 44, background: '#0a0a12',
  display: 'flex', alignItems: 'center', justifyContent: 'center', gap: 8,
  borderRadius: 12, border: '1px solid rgba(139,92,246,0.2)',
  fontFamily: 'Inter, sans-serif'
}}>
  <svg width="18" height="18" viewBox="0 0 24 24" style={{ display: 'flex' }}>
    <path fill="#b8d4f0" d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 0 1-2.063-2.065 2.064 2.064 0 1 1 4.126 0 2.062 2.062 0 0 1-2.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
  </svg>
  <span style={{ fontSize: 14, color: '#c0c8e0', fontWeight: 500 }}>LinkedIn</span>
</div>
```

```aura width=120 height=44 link="mailto:gauravkumarpandey@example.com" inline align=center
<div style={{
  width: 120, height: 44, background: '#0a0a12',
  display: 'flex', alignItems: 'center', justifyContent: 'center', gap: 8,
  borderRadius: 12, border: '1px solid rgba(234,67,53,0.2)',
  fontFamily: 'Inter, sans-serif'
}}>
  <svg width="18" height="18" viewBox="0 0 24 24" style={{ display: 'flex' }}>
    <path fill="#fecaca" d="M2 7h20L12 13.5 2 7Z"/>
    <path fill="#fb7185" d="M2 9l10 6 10-6v9a2 2 0 0 1-2 2H4a2 2 0 0 1-2-2V9Z"/>
  </svg>
  <span style={{ fontSize: 14, color: '#c0c8e0', fontWeight: 500 }}>Email</span>
</div>
```

<!-- ═══════════════════════════════════════════════════════════════════ -->
<!-- FOOTER — Animated scanline + terminal aesthetic                    -->
<!-- ═══════════════════════════════════════════════════════════════════ -->

```aura width=860 height=80
<div style={{
  width: '100%', height: '100%', background: '#fff5f6',
  display: 'flex', flexDirection: 'column', alignItems: 'center', justifyContent: 'center',
  fontFamily: 'Inter, sans-serif', position: 'relative', overflow: 'hidden',
  borderRadius: 16, border: '1px solid rgba(236,72,153,0.16)'
}}>

  <style>{`
    @keyframes ft-scan { 0% { transform: translateY(-80px); } 100% { transform: translateY(80px); } }
    @keyframes ft-pulse { 0%, 100% { opacity: 0.4; } 50% { opacity: 0.8; } }
    @keyframes ft-orb { 0%, 100% { transform: translate(0,0); opacity: 0.3; } 50% { transform: translate(30px,-10px); opacity: 0.5; } }
    #ftscan { animation: ft-scan 4s linear infinite; }
    #ftd1 { animation: ft-pulse 3s ease-in-out infinite; }
    #ftd2 { animation: ft-pulse 3s ease-in-out infinite 1s; }
    #ftd3 { animation: ft-pulse 3s ease-in-out infinite 2s; }
    #ftorb1 { animation: ft-orb 8s ease-in-out infinite; }
  `}</style>

  <svg width="860" height="80" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <linearGradient id="fsg" x1="0" y1="0" x2="0" y2="1">
        <stop offset="0%" stopColor="rgba(236,72,153,0)" />
        <stop offset="45%" stopColor="rgba(236,72,153,0.02)" />
        <stop offset="50%" stopColor="rgba(236,72,153,0.06)" />
        <stop offset="55%" stopColor="rgba(236,72,153,0.02)" />
        <stop offset="100%" stopColor="rgba(236,72,153,0)" />
      </linearGradient>
      <radialGradient id="ftg1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(236,72,153,0.20)" />
        <stop offset="100%" stopColor="rgba(236,72,153,0)" />
      </radialGradient>
    </defs>

    <line x1="0" y1="1" x2="860" y2="1" stroke="rgba(236,72,153,0.12)" strokeWidth="1" />

    <ellipse id="ftorb1" cx="430" cy="40" rx="300" ry="60" fill="url(#ftg1)" />
    <rect id="ftscan" x="0" y="0" width="860" height="80" fill="url(#fsg)" />
  </svg>

  <div style={{ display: 'flex', alignItems: 'center', gap: 6, zIndex: 10 }}>
    <div id="ftd1" style={{ width: 4, height: 4, borderRadius: 2, background: 'rgba(236,72,153,0.7)' }} />
    <div id="ftd2" style={{ width: 4, height: 4, borderRadius: 2, background: 'rgba(139,92,246,0.7)' }} />
    <div id="ftd3" style={{ width: 4, height: 4, borderRadius: 2, background: 'rgba(244,63,94,0.7)' }} />
  </div>

  <span style={{
    fontSize: 11, color: 'rgba(190,24,93,0.60)', letterSpacing: 3,
    fontWeight: 500, marginTop: 8, zIndex: 10
  }}>gaurav kumar pandey · one quiet credit: akuuu.</span>
</div>
```
