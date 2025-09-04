<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>The Execution Discipline Method™ – Leadership Style Quiz</title>
<meta name="description" content="Discover your execution leadership archetype: Visionary, Operator, Architect, or Steward." />
<style>
  :root{
    --brand:#0B3D91;      /* primary brand color */
    --brand-2:#14213d;    /* deep accent */
    --ink:#1b1f23;        /* body text */
    --muted:#6b7280;      /* secondary text */
    --bg:#f7f7fa;         /* page bg */
    --card:#ffffff;       /* card bg */
    --ok:#0a7d2f;
    --warn:#b45309;
  }
  *{box-sizing:border-box}
  body{
    margin:0; font-family:system-ui, -apple-system, Segoe UI, Roboto, Inter, Arial, sans-serif;
    color:var(--ink); background:var(--bg); line-height:1.5;
  }
  .wrap{max-width:880px; margin:32px auto; padding:0 16px}
  header{
    background:linear-gradient(140deg,var(--brand),var(--brand-2));
    color:#fff; border-radius:16px; padding:24px;
    box-shadow:0 10px 24px rgba(0,0,0,.06);
  }
  header h1{margin:0 0 6px; font-size:28px; letter-spacing:.2px}
  header p{margin:0; opacity:.9}
  .card{
    background:var(--card); border-radius:14px; padding:20px; margin:16px 0;
    box-shadow:0 8px 18px rgba(0,0,0,.05); border:1px solid #ececf1;
  }
  .muted{color:var(--muted)}
  .row{display:flex; gap:16px; flex-wrap:wrap}
  .q{
    padding:14px 14px 8px; border:1px solid #e7e7ee; border-radius:12px; margin:10px 0;
  }
  .q h4{margin:0 0 10px; font-size:16px}
  .scale{display:flex; align-items:center; gap:12px; flex-wrap:wrap}
  .scale label{
    display:flex; align-items:center; gap:8px; padding:8px 10px; border:1px solid #e5e7eb;
    border-radius:10px; cursor:pointer; user-select:none; background:#fff;
  }
  input[type="radio"]{accent-color:var(--brand)}
  .pill{display:inline-block; padding:6px 10px; border-radius:999px; background:#eef2ff; color:#1f2a69; font-weight:600; font-size:12px}
  .progress{height:10px; background:#ececf1; border-radius:999px; overflow:hidden}
  .bar{height:100%; width:0; background:linear-gradient(90deg,#2563eb,#0ea5e9)}
  button{
    appearance:none; border:0; background:var(--brand); color:#fff;
    padding:12px 16px; border-radius:12px; font-weight:700; cursor:pointer;
    box-shadow:0 8px 18px rgba(11,61,145,.25);
  }
  button.secondary{
    background:#fff; color:var(--brand); border:1px solid #d1d5db; box-shadow:none;
  }
  .grid{display:grid; grid-template-columns:1fr 1fr; gap:16px}
  @media (max-width:720px){ .grid{grid-template-columns:1fr} }
  .result{
    border-left:4px solid var(--brand); padding-left:12px; margin:8px 0 0;
  }
  .tag{display:inline-block; padding:6px 8px; border-radius:8px; background:#f0fdf4; color:var(--ok); font-weight:600; font-size:12px}
  .warn{background:#fff7ed; color:var(--warn)}
  .footer-note{font-size:12px; color:var(--muted); margin-top:8px}
</style>
</head>
<body>
<div class="wrap">
  <header>
    <h1>The Execution Discipline Method™</h1>
    <p>Leadership Style Quiz — discover your execution archetype and get a tailored next step.</p>
  </header>

  <div class="card">
    <div class="row" style="align-items:center; justify-content:space-between">
      <div><span class="pill" id="progress-label">Progress: 0%</span></div>
      <div style="flex:1; min-width:220px">
        <div class="progress"><div class="bar" id="bar"></div></div>
      </div>
    </div>
  </div>

  <!-- INSTRUCTIONS -->
  <div class="card">
    <strong>Instructions</strong>
    <p class="muted">Rate each statement from 1 to 5. 1 = Strongly Disagree, 5 = Strongly Agree.</p>
  </div>

  <!-- QUESTIONS -->
  <form id="quiz">
    <!-- Clarity -->
    <div class="card"><h3>Clarity</h3>
      <div class="q"><h4>1. Every initiative I touch has a single accountable owner.</h4><div class="scale" data-q="c1"></div></div>
      <div class="q"><h4>2. Success criteria are defined before work starts.</h4><div class="scale" data-q="c2"></div></div>
      <div class="q"><h4>3. I prefer structure and role clarity over flexibility.</h4><div class="scale" data-q="c3"></div></div>
      <div class="q"><h4>4. My team rarely has to guess what I expect.</h4><div class="scale" data-q="c4"></div></div>
    </div>

    <!-- Prioritization -->
    <div class="card"><h3>Prioritization</h3>
      <div class="q"><h4>5. I quickly pause low-value projects to protect focus.</h4><div class="scale" data-q="p1"></div></div>
      <div class="q"><h4>6. I routinely test work against strategy alignment.</h4><div class="scale" data-q="p2"></div></div>
      <div class="q"><h4>7. I would rather do fewer things well than many halfway.</h4><div class="scale" data-q="p3"></div></div>
      <div class="q"><h4>8. I actively shield my team from distractions and scope creep.</h4><div class="scale" data-q="p4"></div></div>
    </div>

    <!-- Execution Systems -->
    <div class="card"><h3>Execution Systems</h3>
      <div class="q"><h4>9. I run on clear rhythms and cadences.</h4><div class="scale" data-q="e1"></div></div>
      <div class="q"><h4>10. I keep dashboards or trackers to monitor execution.</h4><div class="scale" data-q="e2"></div></div>
      <div class="q"><h4>11. Major decisions are documented for visibility.</h4><div class="scale" data-q="e3"></div></div>
      <div class="q"><h4>12. Meetings I lead produce clear outputs.</h4><div class="scale" data-q="e4"></div></div>
    </div>

    <!-- Accountability & Trust -->
    <div class="card"><h3>Accountability & Trust</h3>
      <div class="q"><h4>13. I publicly recognize reliable follow-through.</h4><div class="scale" data-q="t1"></div></div>
      <div class="q"><h4>14. I escalate risks quickly rather than let them linger.</h4><div class="scale" data-q="t2"></div></div>
      <div class="q"><h4>15. Commitments are visible to others, not private.</h4><div class="scale" data-q="t3"></div></div>
      <div class="q"><h4>16. I ask for and act on feedback from my team.</h4><div class="scale" data-q="t4"></div></div>
    </div>

    <div class="grid">
      <button type="button" id="submit">See my results</button>
      <button type="reset" class="secondary" id="resetBtn">Reset</button>
    </div>
  </form>

  <!-- RESULTS -->
  <div class="card" id="results" style="display:none">
    <h3>Your Results</h3>
    <p id="summary"></p>
    <div class="result" id="archetype"></div>
    <p class="footer-note" id="recommendation"></p>
    <div class="grid" style="margin-top:12px">
      <button type="button" id="copyBtn" class="secondary">Copy results</button>
      <button type="button" id="pdfBtn">Print / Save PDF</button>
    </div>
    <div style="margin-top:12px">
      <a id="cta" href="https://calendly.com/" target="_blank" style="text-decoration:none">
        <button type="button">Book a workshop or coaching session</button>
      </a>
    </div>
  </div>

  <div class="card">
    <strong>Privacy</strong>
    <p class="muted">All scoring runs locally in your browser. No data is sent to a server.</p>
  </div>

  <footer class="muted" style="text-align:center; margin:24px 0">
    © <span id="yr"></span> The Execution Discipline Method™ — Systems for Scale
  </footer>
</div>

<script>
  const questions = [
    'c1','c2','c3','c4',
    'p1','p2','p3','p4',
    'e1','e2','e3','e4',
    't1','t2','t3','t4'
  ];
  const groups = {
    Clarity:['c1','c2','c3','c4'],
    Prioritization:['p1','p2','p3','p4'],
    'Execution Systems':['e1','e2','e3','e4'],
    'Accountability & Trust':['t1','t2','t3','t4']
  };
  const labels = ['1','2','3','4','5'];

  // render radios
  document.querySelectorAll('.scale').forEach(sc=>{
    const key = sc.dataset.q;
    labels.forEach(v=>{
      const id = key+'_'+v;
      const lab = document.createElement('label');
      lab.innerHTML = `<input type="radio" name="${key}" value="${v}" /> ${v}`;
      lab.htmlFor = id;
      sc.appendChild(lab);
    });
  });

  const updateProgress=()=>{
    const answered = questions.filter(q=>document.querySelector(`input[name="${q}"]:checked`)).length;
    const pct = Math.round((answered/questions.length)*100);
    document.getElementById('bar').style.width = pct+'%';
    document.getElementById('progress-label').textContent = 'Progress: '+pct+'%';
  };
  document.addEventListener('change', e=>{
    if(e.target.matches('input[type="radio"]')) updateProgress();
  });

  const sum = keys => keys.reduce((acc,k)=>{
    const el = document.querySelector(`input[name="${k}"]:checked`);
    return acc + (el ? Number(el.value) : 0);
  },0);

  const archetypeText = (topKey)=>{
    switch(topKey){
      case 'Clarity': return {
        name:'The Visionary',
        desc:'You set direction and define success. Best next lever: make clarity visible with Role Clarity Cards and a Decision Log.'
      };
      case 'Prioritization': return {
        name:'The Operator',
        desc:'You protect focus and sequence work. Best next lever: align the org with a clear Operating Rhythm.'
      };
      case 'Execution Systems': return {
        name:'The Architect',
        desc:'You thrive on cadence and dashboards. Best next lever: balance systems with Trust Signals and recognition.'
      };
      case 'Accountability & Trust': return {
        name:'The Steward',
        desc:'You build ownership and culture. Best next lever: enforce Action Registers and escalation lanes.'
      };
      default: return {name:'Hybrid', desc:'You show strengths across styles. Use the method to round out any low pillar.'};
    }
  };

  document.getElementById('submit').addEventListener('click', ()=>{
    // ensure all answered
    const missing = questions.filter(q=>!document.querySelector(`input[name="${q}"]:checked`));
    if(missing.length){
      alert('Please answer all questions before viewing results.');
      return;
    }
    // pillar scores
    const pillarScores = {};
    Object.keys(groups).forEach(k=>{
      pillarScores[k] = sum(groups[k]);
    });

    // determine top pillar(s)
    const entries = Object.entries(pillarScores);
    entries.sort((a,b)=>b[1]-a[1]);
    const top = entries[0]; const second = entries[1];
    const topKey = (second && second[1]===top[1]) ? 'Hybrid' : top[0];

    // compile summary
    const total = entries.reduce((a,[,v])=>a+v,0); // max 80
    const pct = Math.round((total/80)*100);
    const summary = `Total score: ${total}/80 (${pct}%). Pillar breakdown → ` +
      entries.map(([k,v])=>`${k}: ${v}/20`).join(' | ');

    // archetype block
    const arc = archetypeText(topKey);
    const archEl = document.getElementById('archetype');
    archEl.innerHTML = `<p><strong>Archetype:</strong> ${arc.name}</p><p>${arc.desc}</p>`;

    // recommendation
    let rec = '';
    if(pct < 55) rec = 'Recommendation: Start with a 2-Day Intensive to install the operating system quickly.';
    else if(pct < 70) rec = 'Recommendation: Run a Full-Day Workshop or a 4-Week Sprint to build rhythm and accountability.';
    else rec = 'Recommendation: Half-Day Workshop + Follow-On Coaching to sustain discipline and trust signals.';
    document.getElementById('recommendation').textContent = rec;

    document.getElementById('summary').textContent = summary;
    document.getElementById('results').style.display = 'block';
    window.scrollTo({top:document.getElementById('results').offsetTop-12, behavior:'smooth'});
  });

  document.getElementById('resetBtn').addEventListener('click', ()=>{
    document.getElementById('results').style.display='none';
    updateProgress();
  });

  document.getElementById('copyBtn').addEventListener('click', async ()=>{
    const txt = document.getElementById('summary').textContent + '\n' +
                document.getElementById('archetype').innerText + '\n' +
                document.getElementById('recommendation').innerText;
    try{
      await navigator.clipboard.writeText(txt);
      alert('Results copied to clipboard.');
    }catch(e){
      alert('Copy failed. Select the text and copy manually.');
    }
  });

  document.getElementById('pdfBtn').addEventListener('click', ()=>{ window.print(); });
  document.getElementById('yr').textContent = new Date().getFullYear();
</script>
</body>
</html>

