# Trendy-fashion-
3D premium e-commerce website for Trendy Fashion
/* Trendy Fashion — 3D premium look */
:root{
  --accent:#b08b4f;
  --bg:#0f1724;
  --card:#0b1220;
  --muted:#9aa3b2;
  --glass: rgba(255,255,255,0.04);
  --glass-2: rgba(255,255,255,0.02);
  --container:1100px;
  --radius:14px;
  --glass-border: rgba(255,255,255,0.06);
  --gold-grad: linear-gradient(135deg,#f7e6c9,#c79b5a 60%);
}

*{box-sizing:border-box;margin:0;padding:0}
html,body{height:100%}
body{
  font-family:Inter,system-ui,Segoe UI,Roboto,Helvetica,Arial,sans-serif;
  background: radial-gradient(1200px 600px at 10% 20%, rgba(176,139,79,0.06), transparent),
              linear-gradient(180deg,#081226 0%, #07101b 100%);
  color:#e6eef6;
  -webkit-font-smoothing:antialiased;
  -moz-osx-font-smoothing:grayscale;
}

/* container */
.container{max-width:var(--container);margin:0 auto;padding:18px}

/* topbar */
.topbar{position:sticky;top:0;backdrop-filter: blur(6px);background:linear-gradient(180deg, rgba(255,255,255,0.02), transparent);border-bottom:1px solid rgba(255,255,255,0.03);z-index:50}
.brand-wrap{display:flex;align-items:center;gap:12px}
.brand-3d{width:56px;height:56px;border-radius:12px;display:flex;align-items:center;justify-content:center; perspective:700px}
.logo-face{
  width:46px;height:46px;border-radius:10px;display:flex;align-items:center;justify-content:center;
  background: linear-gradient(145deg,#111827,#001027);
  box-shadow: 0 8px 30px rgba(0,0,0,0.6), inset 0 -6px 16px rgba(255,255,255,0.02);
  transform: rotateX(18deg) rotateY(-8deg);
  border: 1px solid rgba(255,255,255,0.06);
  font-weight:700;color:var(--gold, #ffdca3);
}
.brand-text{line-height:1}
.brand-title{font-weight:800;color:var(--accent);font-size:1.05rem}
.brand-sub{font-size:0.75rem;color:var(--muted)}

/* nav */
.nav{margin-left:20px;flex:1}
.nav a{color:var(--muted);text-decoration:none;margin-right:14px;font-weight:600;padding:8px;border-radius:10px;transition:all .18s}
.nav a:hover{background:rgba(255,255,255,0.02);color:#fff}

/* header actions */
.header-actions{display:flex;align-items:center;gap:8px}
.ghost{background:transparent;border:1px solid rgba(255,255,255,0.04);padding:8px 12px;border-radius:10px;color:var(--muted);cursor:pointer}
.cart-btn{background:var(--accent);color:#081018;padding:8px 12px;border-radius:10px;cursor:pointer;font-weight:700}

/* main */
.main{padding:28px 18px}

/* hero */
.hero{
  background: linear-gradient(120deg, rgba(255,255,255,0.02), rgba(176,139,79,0.03));
  border-radius:var(--radius);padding:28px;display:flex;gap:20px;align-items:center;
  box-shadow: 0 20px 40px rgba(3,7,18,0.6);
  transform-style: preserve-3d;
}
.hero-left{flex:1}
.hero h1{font-size:2rem;margin-bottom:8px}
.hero p{color:var(--muted);margin-bottom:12px}
.hero .cta{padding:12px 16px;border-radius:12px;border:0;background:var(--gold-grad);color:#091018;font-weight:800;cursor:pointer;box-shadow:0 8px 30px rgba(176,139,79,0.12)}

/* product grid */
.grid{display:grid;grid-template-columns:repeat(4,1fr);gap:18px;margin-top:22px}
.card{
  background: linear-gradient(180deg, rgba(255,255,255,0.02), transparent);
  border-radius:12px;padding:14px;position:relative;overflow:visible;border:1px solid var(--glass-border);
  box-shadow: 0 10px 30px rgba(2,6,13,0.6);
  transform: translateZ(0);
}
.prod-img{width:100%;height:220px;border-radius:10px;object-fit:cover;margin-bottom:10px;box-shadow: 0 12px 30px rgba(2,6,13,0.45)}
.prod-title{font-weight:700;color:#fff}
.prod-sub{color:var(--muted);font-size:0.9rem;margin-top:6px}
.prod-row{display:flex;align-items:center;justify-content:space-between;margin-top:10px}
.price{font-weight:800;color:var(--accent)}
.add-btn{padding:8px 12px;border-radius:10px;border:0;background: linear-gradient(90deg,#caa36a,#8a5f2a);color:#071018;cursor:pointer;font-weight:800;box-shadow:0 8px 20px rgba(136,84,38,0.15)}

/* 3d tag */
.tag-3d{position:absolute;right:14px;top:14px;background:linear-gradient(180deg, rgba(255,255,255,0.03), transparent);padding:6px 10px;border-radius:10px;border:1px solid rgba(255,255,255,0.03);font-weight:700}

/* cart modal */
.cart-modal{position:fixed;inset:0;display:none;align-items:center;justify-content:center;background:rgba(0,0,0,0.5);z-index:80}
.cart-modal.show{display:flex}
.cart-panel{width:420px;background:linear-gradient(180deg, rgba(255,255,255,0.02), transparent);border-radius:12px;padding:18px;border:1px solid rgba(255,255,255,0.03)}
.cart-items{max-height:320px;overflow:auto;margin-top:8px}
.cart-item{display:flex;gap:12px;padding:10px 0;border-bottom:1px solid rgba(255,255,255,0.02)}
.cart-item img{width:72px;height:72px;object-fit:cover;border-radius:8px}
.meta{flex:1}
.qty-controls{display:flex;gap:8px;align-items:center;margin-top:8px}
.dec,.inc{width:34px;height:34px;border-radius:8px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:#fff;cursor:pointer}
.btn-primary{background:var(--accent);color:#081018;padding:10px 14px;border-radius:10px;border:0;cursor:pointer;font-weight:800}
.btn-outline{background:transparent;border:1px solid rgba(255,255,255,0.04);color:var(--muted);padding:8px 12px;border-radius:10px;cursor:pointer}

/* forms */
.form{background:linear-gradient(180deg, rgba(255,255,255,0.01), transparent);padding:18px;border-radius:12px;border:1px solid rgba(255,255,255,0.03);width:100%;max-width:480px}
.form input{width:100%;padding:10px;border-radius:8px;border:1px solid rgba(255,255,255,0.04);margin-top:10px;background:transparent;color:#fff}

/* footer */
.footer{margin-top:36px;padding:18px 0;border-top:1px solid rgba(255,255,255,0.02)}
.footer-grid{display:flex;justify-content:space-between;align-items:center}

/* responsive */
@media (max-width:1100px){.grid{grid-template-columns:repeat(3,1fr)}}
@media (max-width:760px){.grid{grid-template-columns:repeat(2,1fr)}.hero{flex-direction:column;align-items:flex-start}.nav{display:none}}
@media (max-width:420px){.grid{grid-template-columns:1fr}}
/* small helpers */
.muted{color:var(--muted)}
.small{font-size:0.95rem}
