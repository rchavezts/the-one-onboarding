<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Welcome to The One</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap');

  *{margin:0;padding:0;box-sizing:border-box;}

  :root{
    --navy:#1c2c46;
    --navy-deep:#102a6b;
    --blue-1:#1a4fb0;
    --blue-2:#2f80d6;
    --blue-3:#4ba3e3;
    --cyan:#38c6ef;
    --slate:#5a6577;
    --line:#e3eaf2;
    --bg:#eef3f9;
  }

  body{
    font-family:'Plus Jakarta Sans',-apple-system,Segoe UI,Roboto,sans-serif;
    color:var(--navy);
    background:var(--bg);
    line-height:1.55;
    padding:24px 16px 60px;
  }

  .wrap{max-width:720px;margin:0 auto;}

  /* ---------- HERO ---------- */
  .hero{
    background:#fff;border-radius:20px;overflow:hidden;
    box-shadow:0 10px 40px rgba(28,44,70,.10);margin-bottom:30px;
  }
  .band{display:flex;height:7px;}
  .band div{flex:1;}
  .band .b1{background:var(--navy-deep);}
  .band .b2{background:var(--blue-1);}
  .band .b3{background:var(--blue-2);}
  .band .b4{background:var(--blue-3);}
  .band .b5{background:var(--cyan);}

  .hero-body{padding:34px 30px 30px;text-align:center;}
  .hero img{width:100%;max-width:210px;height:auto;margin:0 auto 22px;}
  .plan-pill{
    display:inline-block;font-size:11px;font-weight:800;letter-spacing:1.5px;
    padding:5px 13px;border-radius:20px;background:#dbeafe;color:#1d4ed8;margin-bottom:16px;
  }
  .hero h1{font-size:27px;font-weight:800;letter-spacing:-.3px;margin-bottom:8px;}
  .hero p{color:var(--slate);font-size:15.5px;max-width:460px;margin:0 auto;}

  /* ---------- STEPPER ---------- */
  .steps{position:relative;}
  .steps::before{
    content:'';position:absolute;left:23px;top:14px;bottom:40px;width:2px;
    background:linear-gradient(to bottom,var(--blue-1),var(--blue-3));opacity:.35;
  }

  .step{position:relative;padding-left:62px;margin-bottom:22px;}
  .step-num{
    position:absolute;left:0;top:0;width:48px;height:48px;border-radius:13px;
    background:var(--navy);color:#fff;font-weight:800;font-size:18px;
    display:flex;align-items:center;justify-content:center;z-index:2;
    box-shadow:0 4px 12px rgba(28,44,70,.18);
  }
  .step:nth-child(1) .step-num{background:var(--navy-deep);}
  .step:nth-child(2) .step-num{background:var(--blue-1);}
  .step:nth-child(3) .step-num{background:var(--blue-2);}
  .step:nth-child(4) .step-num{background:var(--blue-2);}
  .step:nth-child(5) .step-num{background:var(--blue-3);}
  .step:nth-child(6) .step-num{background:var(--blue-3);}
  .step:nth-child(7) .step-num{background:var(--cyan);}

  .card{
    background:#fff;border-radius:14px;padding:22px 24px;
    box-shadow:0 4px 18px rgba(28,44,70,.07);
  }
  .card h2{font-size:19px;font-weight:800;margin-bottom:7px;}
  .card .lead{color:var(--slate);font-size:14.5px;margin-bottom:16px;}

  .points{list-style:none;}
  .points li{
    font-size:14px;color:#33455f;padding:6px 0 6px 24px;position:relative;
  }
  .points li::before{
    content:'';position:absolute;left:0;top:11px;width:8px;height:8px;border-radius:50%;
    background:var(--blue-2);
  }

  /* ---------- LOOM PLACEHOLDER ---------- */
  .loom{
    margin-top:16px;border-radius:11px;overflow:hidden;
    background:linear-gradient(135deg,#1c2c46 0%,#1a4fb0 100%);
    aspect-ratio:16/9;display:flex;flex-direction:column;
    align-items:center;justify-content:center;text-align:center;padding:20px;
  }
  .loom .play{
    width:54px;height:54px;border-radius:50%;background:rgba(255,255,255,.18);
    display:flex;align-items:center;justify-content:center;margin-bottom:12px;
    border:2px solid rgba(255,255,255,.5);
  }
  .loom .play::before{
    content:'';border-style:solid;border-width:9px 0 9px 15px;
    border-color:transparent transparent transparent #fff;margin-left:3px;
  }
  .loom .lbl{color:#fff;font-size:14px;font-weight:700;}
  .loom .sub{color:#aec6ec;font-size:12px;margin-top:3px;}
  /*  ▼▼▼  TO ADD A VIDEO: delete this .loom block and paste your Loom embed iframe here  ▼▼▼  */

  /* ---------- HIGH-ONLY (IDX) ---------- */
  .high-only{display:none;}
  body.tier-high .high-only{display:block;}

  .idx-flag{
    margin-top:14px;background:#fdf8ef;border:1px solid #f4e3c4;border-left:4px solid #d4870b;
    border-radius:10px;padding:14px 16px;
  }
  .idx-flag .tag{
    font-size:10px;font-weight:800;letter-spacing:1px;color:#b3700a;
    background:#fdebc8;display:inline-block;padding:3px 9px;border-radius:12px;margin-bottom:7px;
  }
  .idx-flag h3{font-size:15px;font-weight:800;margin-bottom:4px;color:var(--navy);}
  .idx-flag p{font-size:13.5px;color:#6b5320;}

  /* ---------- FOOTER ---------- */
  .footer-card{
    margin-top:30px;background:linear-gradient(135deg,#102a6b 0%,#1a4fb0 100%);
    border-radius:16px;padding:26px 28px;text-align:center;
  }
  .footer-card h2{color:#fff;font-size:18px;font-weight:800;margin-bottom:7px;}
  .footer-card p{color:#cdddf4;font-size:14px;}
  .footer-card a{color:#fff;font-weight:700;text-decoration:underline;}

  .tiny{text-align:center;color:#9aa6b6;font-size:11.5px;margin-top:22px;}

  @media(max-width:480px){
    .hero-body{padding:28px 20px 24px;}
    .card{padding:18px 18px;}
    .step{padding-left:54px;}
    .step-num{width:42px;height:42px;font-size:16px;}
    .steps::before{left:20px;}
  }
</style>
</head>
<body>
<div class="wrap">

  <!-- HERO -->
  <div class="hero">
    <div class="band"><div class="b1"></div><div class="b2"></div><div class="b3"></div><div class="b4"></div><div class="b5"></div></div>
    <div class="hero-body">
      <img src="https://assets.cdn.filesafe.space/CtoueTZMCvD2i46ZsDWW/media/6a3c40dd817563b473dedcda.png" alt="The One — CRM & Marketing Platform">
      <div class="plan-pill" id="planPill">YOUR PLAN</div>
      <h1 id="greeting">Welcome to The One</h1>
      <p>This is your command center. Follow the steps below to get comfortable — you'll be running your business from here in no time.</p>
    </div>
  </div>

  <!-- STEPS -->
  <div class="steps">

    <!-- 1 -->
    <div class="step">
      <div class="step-num">1</div>
      <div class="card">
        <h2>Start here</h2>
        <p class="lead">A quick tour of what The One does and how everything fits together.</p>
        <div class="loom">
          <div class="play"></div>
          <div class="lbl">Welcome walkthrough</div>
          <div class="sub">Video coming soon</div>
        </div>
      </div>
    </div>

    <!-- 2 -->
    <div class="step">
      <div class="step-num">2</div>
      <div class="card">
        <h2>Your dashboard</h2>
        <p class="lead">The home screen shows your business at a glance — the moment you log in.</p>
        <ul class="points">
          <li>New leads, active deals, and tasks all in one view</li>
          <li>Your numbers update in real time as activity comes in</li>
          <li>Click any widget to jump straight to the details</li>
        </ul>
        <div class="loom">
          <div class="play"></div>
          <div class="lbl">Dashboard tour</div>
          <div class="sub">Video coming soon</div>
        </div>
      </div>
    </div>

    <!-- 3 -->
    <div class="step">
      <div class="step-num">3</div>
      <div class="card">
        <h2>Your pipelines</h2>
        <p class="lead">Every lead moves through a pipeline so you always know what's next.</p>
        <ul class="points">
          <li>Four pipelines: Lead, Buyer, Seller, and Renter</li>
          <li>Drag a contact between stages as the deal progresses</li>
          <li>Nothing falls through the cracks — every stage has a next step</li>
        </ul>
        <div class="loom">
          <div class="play"></div>
          <div class="lbl">Working your pipelines</div>
          <div class="sub">Video coming soon</div>
        </div>
      </div>
    </div>

    <!-- 4 -->
    <div class="step">
      <div class="step-num">4</div>
      <div class="card">
        <h2>Capturing leads</h2>
        <p class="lead">New leads flow in automatically and become contacts you can work instantly.</p>
        <ul class="points">
          <li>Your forms and landing pages create contacts the moment someone submits</li>
          <li>Your contact card captures anyone who saves your info</li>
        </ul>

        <!-- HIGH TIER ONLY: IDX -->
        <div class="high-only">
          <div class="idx-flag">
            <span class="tag">INCLUDED WITH YOUR PLAN</span>
            <h3>Your IDX home search</h3>
            <p>Buyers searching listings on your site become leads here too — and their activity shows up on your IDX dashboard in the left menu, so you can see exactly what they're browsing.</p>
          </div>
        </div>

        <div class="loom">
          <div class="play"></div>
          <div class="lbl">Where leads come from</div>
          <div class="sub">Video coming soon</div>
        </div>
      </div>
    </div>

    <!-- 5 -->
    <div class="step">
      <div class="step-num">5</div>
      <div class="card">
        <h2>Staying in touch</h2>
        <p class="lead">Reach your contacts by text and email, and let them book you directly.</p>
        <ul class="points">
          <li>Ready-made email and text templates — send in seconds</li>
          <li>Your calendar lets clients book appointments without the back-and-forth</li>
          <li>Every conversation lives on the contact, so you never lose the thread</li>
        </ul>
        <div class="loom">
          <div class="play"></div>
          <div class="lbl">Messaging &amp; booking</div>
          <div class="sub">Video coming soon</div>
        </div>
      </div>
    </div>

    <!-- 6 -->
    <div class="step">
      <div class="step-num">6</div>
      <div class="card">
        <h2>Your contact card</h2>
        <p class="lead">Your branded digital card — the fastest way to share your info and capture leads.</p>
        <ul class="points">
          <li>Share the link in person, in your bio, or in an email signature</li>
          <li>People can save your contact, call, text, or email in one tap</li>
          <li>Add it to your phone's home screen so it's always handy</li>
        </ul>
        <div class="loom">
          <div class="play"></div>
          <div class="lbl">Using your contact card</div>
          <div class="sub">Video coming soon</div>
        </div>
      </div>
    </div>

    <!-- 7 -->
    <div class="step">
      <div class="step-num">7</div>
      <div class="card">
        <h2>Finish your setup</h2>
        <p class="lead">A few things only you can connect — do these and you're fully live.</p>
        <ul class="points">
          <li>Connect your calendar so bookings sync to you</li>
          <li>Set up your phone number for calls and texts</li>
          <li>Connect your email so messages send from your address</li>
        </ul>
        <div class="loom">
          <div class="play"></div>
          <div class="lbl">Connecting your accounts</div>
          <div class="sub">Video coming soon</div>
        </div>
      </div>
    </div>

  </div>

  <!-- FOOTER -->
  <div class="footer-card">
    <h2>Stuck on anything?</h2>
    <p>We're here to help. Reach out at <a href="mailto:support@theonecrm.com">support@theonecrm.com</a> and we'll get you sorted.</p>
  </div>

  <p class="tiny">The One — CRM &amp; Marketing Platform</p>

</div>

<script>
  (function(){
    var params = new URLSearchParams(window.location.search);
    var tier = (params.get('tier') || '').trim().toLowerCase();
    var name = (params.get('name') || '').trim();

    // Tier gating — only show IDX content for High
    if(tier === 'high'){ document.body.classList.add('tier-high'); }

    // Plan pill label
    var pill = document.getElementById('planPill');
    var labels = { starter:'STARTER PLAN', mid:'MID PLAN', high:'HIGH PLAN' };
    if(labels[tier]){ pill.textContent = labels[tier]; }
    else { pill.style.display = 'none'; }

    // Personalized greeting
    if(name){
      var safe = name.replace(/[<>]/g,'');
      document.getElementById('greeting').textContent = 'Welcome, ' + safe + '!';
    }
  })();
</script>
</body>
</html>
