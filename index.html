<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>AI-Assisted Detection Engineering and SOC Investigation Platform</title>
<meta name="description" content="Purple-team and AI-assisted detection engineering platform: ATT&amp;CK-aligned Atomic Red Team execution, telemetry collection, AQL detection generation, and AI validation." />
<style>
  :root {
    --bg: #0b0f14;
    --bg-raised: #111721;
    --bg-sunken: #080b10;
    --border: #1e2733;
    --border-strong: #2b3746;
    --text: #dce3ec;
    --text-dim: #8d9bab;
    --text-faint: #64707e;
    --accent: #4f9ecf;
    --accent-dim: #2d5f80;
    --purple: #8b7ac8;
    --warn: #c9a227;
    --mono: ui-monospace, "SF Mono", "Cascadia Mono", "Roboto Mono", Menlo, Consolas, monospace;
    --sans: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
  }

  * { box-sizing: border-box; }

  html { -webkit-text-size-adjust: 100%; }

  body {
    margin: 0;
    background: var(--bg);
    color: var(--text);
    font-family: var(--sans);
    font-size: 16px;
    line-height: 1.65;
    -webkit-font-smoothing: antialiased;
  }

  .wrap {
    max-width: 960px;
    margin: 0 auto;
    padding: 0 24px 96px;
  }

  /* ---------- header ---------- */

  header {
    border-bottom: 1px solid var(--border);
    background: linear-gradient(180deg, #0e141c 0%, var(--bg) 100%);
    padding: 64px 24px 48px;
  }

  header .inner {
    max-width: 960px;
    margin: 0 auto;
  }

  .eyebrow {
    font-family: var(--mono);
    font-size: 12px;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: var(--accent);
    margin: 0 0 14px;
  }

  h1 {
    font-size: 34px;
    line-height: 1.25;
    font-weight: 600;
    margin: 0 0 14px;
    letter-spacing: -0.015em;
  }

  .subtitle {
    font-size: 17px;
    color: var(--text-dim);
    max-width: 68ch;
    margin: 0 0 24px;
  }

  .badges {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }

  .badge {
    font-family: var(--mono);
    font-size: 11.5px;
    letter-spacing: 0.04em;
    padding: 4px 10px;
    border: 1px solid var(--border-strong);
    border-radius: 3px;
    color: var(--text-dim);
    background: var(--bg-raised);
  }

  .badge.status {
    border-color: var(--accent-dim);
    color: var(--accent);
  }

  /* ---------- sections ---------- */

  section { margin-top: 56px; }

  h2 {
    font-size: 13px;
    font-family: var(--mono);
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--text-faint);
    font-weight: 600;
    margin: 0 0 20px;
    padding-bottom: 10px;
    border-bottom: 1px solid var(--border);
  }

  h3 {
    font-size: 15px;
    font-weight: 600;
    margin: 28px 0 10px;
    color: var(--text);
  }

  p { margin: 0 0 14px; color: var(--text-dim); }
  p.lead { color: var(--text); }

  a { color: var(--accent); text-decoration: none; }
  a:hover { text-decoration: underline; }

  code {
    font-family: var(--mono);
    font-size: 13px;
    background: var(--bg-sunken);
    border: 1px solid var(--border);
    border-radius: 3px;
    padding: 1px 5px;
    color: var(--text);
  }

  /* ---------- workflow diagram ---------- */

  .flow {
    display: flex;
    flex-direction: column;
    align-items: stretch;
    gap: 0;
    margin: 0 0 8px;
  }

  .flow-step {
    background: var(--bg-raised);
    border: 1px solid var(--border-strong);
    border-left: 3px solid var(--accent-dim);
    border-radius: 4px;
    padding: 13px 16px;
    display: flex;
    align-items: baseline;
    gap: 14px;
  }

  .flow-step .n {
    font-family: var(--mono);
    font-size: 11px;
    color: var(--text-faint);
    min-width: 18px;
  }

  .flow-step .label {
    font-size: 14.5px;
    color: var(--text);
    font-weight: 500;
  }

  .flow-step .note {
    font-size: 12.5px;
    color: var(--text-faint);
    margin-left: auto;
    font-family: var(--mono);
  }

  .flow-arrow {
    height: 18px;
    margin-left: 26px;
    border-left: 1px solid var(--border-strong);
    position: relative;
  }

  .flow-arrow::after {
    content: "";
    position: absolute;
    left: -4px;
    bottom: -1px;
    width: 7px;
    height: 7px;
    border-right: 1px solid var(--border-strong);
    border-bottom: 1px solid var(--border-strong);
    transform: rotate(45deg);
  }

  .flow.planned .flow-step {
    border-left-color: var(--purple);
    border-style: dashed;
    background: transparent;
  }

  /* ---------- architecture ---------- */

  .arch-tier {
    background: var(--bg-raised);
    border: 1px solid var(--border);
    border-radius: 4px;
    padding: 12px 16px;
    display: flex;
    align-items: baseline;
    justify-content: space-between;
    gap: 16px;
    flex-wrap: wrap;
  }

  .arch-tier .name { font-size: 14.5px; color: var(--text); font-weight: 500; }
  .arch-tier .tech { font-family: var(--mono); font-size: 12px; color: var(--text-faint); }

  /* ---------- lists / grids ---------- */

  .grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(270px, 1fr));
    gap: 12px;
  }

  .card {
    background: var(--bg-raised);
    border: 1px solid var(--border);
    border-radius: 4px;
    padding: 14px 16px;
  }

  .card .t {
    font-size: 14px;
    font-weight: 600;
    color: var(--text);
    margin-bottom: 5px;
  }

  .card .d {
    font-size: 13px;
    color: var(--text-dim);
    line-height: 1.55;
  }

  /* ---------- roadmap table ---------- */

  table {
    width: 100%;
    border-collapse: collapse;
    font-size: 14px;
  }

  th {
    text-align: left;
    font-family: var(--mono);
    font-size: 11px;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--text-faint);
    font-weight: 600;
    padding: 0 12px 10px 0;
    border-bottom: 1px solid var(--border);
  }

  td {
    padding: 11px 12px 11px 0;
    border-bottom: 1px solid var(--border);
    color: var(--text-dim);
    vertical-align: top;
  }

  td:first-child { color: var(--text); }

  .pill {
    display: inline-block;
    font-family: var(--mono);
    font-size: 11px;
    letter-spacing: 0.04em;
    padding: 2px 8px;
    border-radius: 3px;
    border: 1px solid var(--border-strong);
    color: var(--text-faint);
    white-space: nowrap;
  }

  .pill.progress { border-color: var(--accent-dim); color: var(--accent); }
  .pill.planned  { border-color: #463c6b; color: var(--purple); }

  /* ---------- callouts ---------- */

  .callout {
    border: 1px solid var(--border-strong);
    border-left: 3px solid var(--warn);
    background: var(--bg-raised);
    border-radius: 4px;
    padding: 16px 18px;
  }

  .callout .t {
    font-family: var(--mono);
    font-size: 11.5px;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--warn);
    margin-bottom: 8px;
  }

  .callout p:last-child { margin-bottom: 0; }

  .callout.info { border-left-color: var(--purple); }
  .callout.info .t { color: var(--purple); }

  footer {
    margin-top: 72px;
    padding-top: 20px;
    border-top: 1px solid var(--border);
    font-size: 13px;
    color: var(--text-faint);
  }

  @media (max-width: 620px) {
    header { padding: 44px 20px 36px; }
    h1 { font-size: 26px; }
    .wrap { padding: 0 20px 64px; }
    .flow-step { flex-wrap: wrap; }
    .flow-step .note { margin-left: 32px; }
  }
</style>
</head>
<body>

<header>
  <div class="inner">
    <p class="eyebrow">Purple Team · Detection Engineering</p>
    <h1>AI-Assisted Detection Engineering and SOC Investigation Platform</h1>
    <p class="subtitle">
      A lab platform for running ATT&amp;CK-aligned Atomic Red Team tests, collecting the telemetry they
      generate, producing AQL detection logic from that telemetry, validating it with AI assistance, and
      pairing it with D3FEND defensive guidance.
    </p>
    <div class="badges">
      <span class="badge status">Prototype / lab platform</span>
      <span class="badge">MITRE ATT&amp;CK</span>
      <span class="badge">Atomic Red Team</span>
      <span class="badge">Elastic</span>
      <span class="badge">AQL</span>
      <span class="badge">D3FEND</span>
    </div>
  </div>
</header>

<div class="wrap">

  <!-- ============ OVERVIEW ============ -->
  <section>
    <h2>Overview</h2>
    <p class="lead">
      Detection engineering tends to stall in the gap between a technique existing in ATT&amp;CK and a
      tested rule that actually fires on it. Closing that gap by hand means standing up a target, running
      the technique, hunting for the telemetry it produced, guessing at field names, writing a query, and
      re-running everything to check the result.
    </p>
    <p>
      This platform turns that loop into one guided workflow. A technique is selected from the ATT&amp;CK
      matrix, the matching Atomic Red Team test is executed against a lab target, and the telemetry the
      test actually generated becomes the input to detection logic — rather than an assumed schema.
      Generated queries are AQL, reviewed with AI assistance, and paired with defensive guidance so the
      output reads as a defensive recommendation, not just a query string.
    </p>
    <p>
      The current focus is the Detection Lab path. An AI SOC Agent investigation module is a planned
      expansion and is documented below as direction, not as shipped functionality.
    </p>
  </section>

  <!-- ============ WORKFLOW ============ -->
  <section>
    <h2>Detection Lab Workflow</h2>
    <div class="flow">
      <div class="flow-step"><span class="n">01</span><span class="label">Select MITRE ATT&amp;CK technique</span><span class="note">matrix UI</span></div>
      <div class="flow-arrow"></div>
      <div class="flow-step"><span class="n">02</span><span class="label">Run Atomic Red Team test</span><span class="note">dynamic test discovery</span></div>
      <div class="flow-arrow"></div>
      <div class="flow-step"><span class="n">03</span><span class="label">Collect telemetry from Windows target</span><span class="note">live output</span></div>
      <div class="flow-arrow"></div>
      <div class="flow-step"><span class="n">04</span><span class="label">Retrieve logs from Elastic/Elasticsearch</span><span class="note">ingestion delay handled</span></div>
      <div class="flow-arrow"></div>
      <div class="flow-step"><span class="n">05</span><span class="label">Generate AQL detection logic</span><span class="note">AQL + YAML rule</span></div>
      <div class="flow-arrow"></div>
      <div class="flow-step"><span class="n">06</span><span class="label">Validate detection with AI</span><span class="note">assistive review</span></div>
      <div class="flow-arrow"></div>
      <div class="flow-step"><span class="n">07</span><span class="label">Review telemetry and defensive guidance</span><span class="note">evidence + D3FEND</span></div>
    </div>
    <p style="margin-top:18px">
      Each stage feeds the next, so the resulting AQL is written against fields that were genuinely
      present in the events the technique produced. AI validation is an assistive review step, not a
      guarantee of detection quality — a human reviewer is still expected in the loop.
    </p>
  </section>

  <!-- ============ CAPABILITIES ============ -->
  <section>
    <h2>Current Capabilities</h2>
    <div class="grid">
      <div class="card">
        <div class="t">MITRE ATT&amp;CK matrix interface</div>
        <div class="d">Browse tactics and techniques; the technique selection drives the rest of the workflow.</div>
      </div>
      <div class="card">
        <div class="t">Atomic Red Team execution</div>
        <div class="d">Tests are discovered dynamically from the target rather than hardcoded, so the list reflects what is installed.</div>
      </div>
      <div class="card">
        <div class="t">Windows target attack validation</div>
        <div class="d">Execution is brokered through a control node to the Windows target VM, with live command output streamed to the UI.</div>
      </div>
      <div class="card">
        <div class="t">Elastic telemetry lookup</div>
        <div class="d">Post-execution log retrieval from Elastic indices, accounting for the delay before events become searchable.</div>
      </div>
      <div class="card">
        <div class="t">AQL detection generation</div>
        <div class="d">Detection logic generated from observed telemetry, rendered as AQL alongside a structured YAML rule definition.</div>
      </div>
      <div class="card">
        <div class="t">AI-assisted query validation</div>
        <div class="d">An LLM-backed adjudication step judges whether detection logic plausibly matches the telemetry that was collected.</div>
      </div>
      <div class="card">
        <div class="t">Detection library matching</div>
        <div class="d">Telemetry is evaluated against a rule library to show existing coverage and coverage gaps before new logic is written.</div>
      </div>
      <div class="card">
        <div class="t">D3FEND defensive guidance</div>
        <div class="d">Techniques are mapped toward defensive countermeasures. The concept is implemented; mapping breadth is still expanding.</div>
      </div>
      <div class="card">
        <div class="t">Log viewer and evidence review</div>
        <div class="d">Table and raw-JSON views of the underlying telemetry, so detection logic traces back to the events that justified it.</div>
      </div>
    </div>
  </section>

  <!-- ============ ARCHITECTURE ============ -->
  <section>
    <h2>Architecture Overview</h2>
    <div class="flow">
      <div class="arch-tier"><span class="name">Frontend UI</span><span class="tech">Next.js · React · Tailwind</span></div>
      <div class="flow-arrow"></div>
      <div class="arch-tier"><span class="name">Backend API</span><span class="tech">route handlers · execution / logs / detection</span></div>
      <div class="flow-arrow"></div>
      <div class="arch-tier"><span class="name">Kali control node</span><span class="tech">SSH · single execution path</span></div>
      <div class="flow-arrow"></div>
      <div class="arch-tier"><span class="name">Windows target VM</span><span class="tech">remote execution</span></div>
      <div class="flow-arrow"></div>
      <div class="arch-tier"><span class="name">Atomic Red Team execution</span><span class="tech">technique simulation</span></div>
      <div class="flow-arrow"></div>
      <div class="arch-tier"><span class="name">Winlogbeat / Elastic Agent</span><span class="tech">log shipping</span></div>
      <div class="flow-arrow"></div>
      <div class="arch-tier"><span class="name">Elastic / Elasticsearch</span><span class="tech">telemetry store</span></div>
      <div class="flow-arrow"></div>
      <div class="arch-tier"><span class="name">Detection Lab UI</span><span class="tech">results · evidence · guidance</span></div>
    </div>

    <h3>Design notes</h3>
    <div class="grid">
      <div class="card">
        <div class="t">The control node is not optional</div>
        <div class="d">All remote execution is brokered through the control node rather than dispatched directly to the target, keeping a single auditable execution path.</div>
      </div>
      <div class="card">
        <div class="t">Telemetry is read from Elastic</div>
        <div class="d">Detection logic is built against what the SIEM actually ingested — the same data a deployed rule would run over.</div>
      </div>
      <div class="card">
        <div class="t">Ingestion latency is expected</div>
        <div class="d">Events are not searchable the instant a test finishes; retrieval accounts for that rather than assuming immediate availability.</div>
      </div>
      <div class="card">
        <div class="t">The pipeline is modular</div>
        <div class="d">Attack execution, log retrieval, and detection generation are separate routes and libraries, so a stage can change independently.</div>
      </div>
    </div>
  </section>

  <!-- ============ AI SOC AGENT ============ -->
  <section>
    <h2>AI SOC Agent — Future Module</h2>
    <div class="callout info">
      <div class="t">Planned module</div>
      <p>
        The routing surface for this module exists in the codebase as scaffolding; the investigation
        logic below is not implemented yet. It is documented to record intended direction, not current
        behavior.
      </p>
    </div>
    <p style="margin-top:18px">
      The Detection Lab answers whether a detection exists and fires. The next module is meant to answer
      the question that follows an alert: what actually happened, and what should be done about it.
    </p>
    <div class="flow planned">
      <div class="flow-step"><span class="n">01</span><span class="label">Detection fires</span></div>
      <div class="flow-arrow"></div>
      <div class="flow-step"><span class="n">02</span><span class="label">Alert appears in AI SOC Investigations</span></div>
      <div class="flow-arrow"></div>
      <div class="flow-step"><span class="n">03</span><span class="label">Analyst runs AI SOC Agent</span></div>
      <div class="flow-arrow"></div>
      <div class="flow-step"><span class="n">04</span><span class="label">Agent collects evidence</span></div>
      <div class="flow-arrow"></div>
      <div class="flow-step"><span class="n">05</span><span class="label">Agent queries Elastic/SIEM</span></div>
      <div class="flow-arrow"></div>
      <div class="flow-step"><span class="n">06</span><span class="label">Agent generates findings</span></div>
      <div class="flow-arrow"></div>
      <div class="flow-step"><span class="n">07</span><span class="label">Agent assigns verdict</span></div>
      <div class="flow-arrow"></div>
      <div class="flow-step"><span class="n">08</span><span class="label">Agent recommends remediation</span></div>
    </div>
    <p style="margin-top:18px">
      The intent is a reviewable investigation record — evidence, findings, verdict, remediation — with
      the analyst as the decision-maker rather than the agent acting autonomously. Verdicts are meant to
      be advisory and traceable back to the evidence that produced them.
    </p>
  </section>

  <!-- ============ ROADMAP ============ -->
  <section>
    <h2>Roadmap</h2>
    <table>
      <thead>
        <tr><th style="width:62%">Item</th><th>Status</th></tr>
      </thead>
      <tbody>
        <tr><td>Linux VM attack execution</td><td><span class="pill planned">Planned</span></td></tr>
        <tr><td>Expanded ATT&amp;CK tactic/technique coverage</td><td><span class="pill progress">In progress</span></td></tr>
        <tr><td>Improved telemetry-to-technique mapping</td><td><span class="pill progress">In progress</span></td></tr>
        <tr><td>Deeper D3FEND mapping</td><td><span class="pill progress">In progress</span></td></tr>
        <tr><td>Alert creation from validated detections</td><td><span class="pill planned">Planned</span></td></tr>
        <tr><td>AI SOC Agent investigation workflow</td><td><span class="pill planned">Planned</span></td></tr>
        <tr><td>Evidence locker</td><td><span class="pill planned">Planned</span></td></tr>
        <tr><td>Investigation timeline</td><td><span class="pill planned">Planned</span></td></tr>
        <tr><td>Alert queue</td><td><span class="pill planned">Planned</span></td></tr>
        <tr><td>Remediation recommendations</td><td><span class="pill planned">Planned</span></td></tr>
        <tr><td>Cloud log sources</td><td><span class="pill planned">Planned</span></td></tr>
        <tr><td>Multi-agent SOC roles</td><td><span class="pill planned">Planned</span></td></tr>
      </tbody>
    </table>
  </section>

  <!-- ============ DISCLAIMER ============ -->
  <section>
    <h2>Safety &amp; Legal Disclaimer</h2>
    <div class="callout">
      <div class="t">Authorized lab use only</div>
      <p>
        This project is intended only for authorized lab environments, detection engineering research,
        purple-team validation, and defensive security testing. Do not run attack simulations against
        systems you do not own or have explicit permission to test.
      </p>
      <p>
        Running adversary simulation tooling against systems without authorization is illegal in most
        jurisdictions. Atomic Red Team tests make real changes to the target host — run them only
        against disposable lab VMs you can restore, and prefer non-destructive, non-administrative
        tests. You are responsible for the environment you point this at.
      </p>
    </div>
  </section>

  <footer>
    Lab / prototype platform under active development. Capability descriptions reflect current focus;
    items marked planned or in progress are not finished. See the repository
    <a href="../README.md">README</a> for setup and environment configuration.
  </footer>

</div>
</body>
</html>
