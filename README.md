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
/* Trendy Fashion — SPA single-file logic
   - localStorage used for users, session, cart, orders
   - Hash routing: #/home #/products #/login #/register #/checkout
*/

const ROOT = document.getElementById('app-root');
const CART_MODAL = document.getElementById('cart-modal');
const CART_ITEMS = document.getElementById('cart-items');
const CART_TOTAL = document.getElementById('cart-total');
const CART_COUNT = document.getElementById('cart-count');
const AUTH_BTN = document.getElementById('auth-btn');

const SITE = {
  name: "Trendy Fashion",
  currencySymbol: "₹"
};

// sample products (replace images with your own)
const PRODUCTS = [
  {id:"t1", title:"Urban Leather Jacket", price:2999, img:"https://images.unsplash.com/photo-1541099649105-f69ad21f3246?q=80&w=1400&auto=format&fit=crop"},
  {id:"t2", title:"Sleek Bomber Jacket", price:2499, img:"https://images.unsplash.com/photo-1541099649106-f69ad21f3247?q=80&w=1400&auto=format&fit=crop"},
  {id:"t3", title:"Denim Street Jeans", price:1499, img:"https://images.unsplash.com/photo-1512436991641-6745cdb1723f?q=80&w=1400&auto=format&fit=crop"},
  {id:"t4", title:"Premium Hoodie", price:1299, img:"https://images.unsplash.com/photo-1602810318868-6b3f1f0a3f3a?q=80&w=1400&auto=format&fit=crop"},
  {id:"t5", title:"Chic Silk Scarf", price:899, img:"https://images.unsplash.com/photo-1520975913364-5c5bcd0c7f3f?q=80&w=1400&auto=format&fit=crop"},
  {id:"t6", title:"Classic Oxford Shirt", price:1199, img:"https://images.unsplash.com/photo-1541099649108-f69ad21f3249?q=80&w=1400&auto=format&fit=crop"},
  {id:"t7", title:"Street Sneaker", price:1999, img:"https://images.unsplash.com/photo-1526178610530-54b9d04f8a2b?q=80&w=1400&auto=format&fit=crop"},
  {id:"t8", title:"Accessories Pack", price:699, img:"https://images.unsplash.com/photo-1526178610540-54b9d04f8a2c?q=80&w=1400&auto=format&fit=crop"}
];

// ------- storage helpers -------
function load(key, fallback){ try{ const v=localStorage.getItem(key); return v?JSON.parse(v):fallback }catch(e){return fallback}}
function save(key,val){ localStorage.setItem(key, JSON.stringify(val))}

// users/session/cart/orders
let USERS = load('tf_users', {}); // {email: {name,email,password}}
let SESSION = load('tf_session', null); // email
let CART = load('tf_cart', {}); // {productId: qty}
let ORDERS = load('tf_orders', []); // [{id, email, items, total, date}]

document.getElementById('year').textContent = new Date().getFullYear();
updateCartUI();
renderRoute();

// navigation listeners
window.addEventListener('hashchange', renderRoute);
document.getElementById('open-cart').addEventListener('click', ()=> toggleCart(true));
document.getElementById('close-cart').addEventListener('click', ()=> toggleCart(false));
document.getElementById('clear-cart').addEventListener('click', ()=> { CART={}; saveCart(); updateCartUI(); renderRoute(); });
document.getElementById('go-to-checkout').addEventListener('click', ()=>{
  location.hash = '#/checkout';
  toggleCart(false);
});

AUTH_BTN.addEventListener('click', ()=>{
  if(SESSION) { // show menu: logout or orders
    if(confirm('Logout from ' + SESSION + ' ?')){ SESSION=null; saveSession(); renderRoute() }
  } else location.hash = '#/login';
});

// ----- routing -----
function renderRoute(){
  const hash = location.hash || '#/home';
  if(hash.startsWith('#/products')) return renderProducts();
  if(hash.startsWith('#/login')) return renderLogin();
  if(hash.startsWith('#/register')) return renderRegister();
  if(hash.startsWith('#/checkout')) return renderCheckout();
  if(hash.startsWith('#/orders')) return renderOrders();
  return renderHome();
}

// ----- UI sections -----
function renderHome(){
  AUTH_BTN.textContent = SESSION ? `Hi, ${SESSION}` : 'Login';
  ROOT.innerHTML = `
    <section class="hero">
      <div class="hero-left">
        <h1>Step into premium streetwear</h1>
        <p class="muted">Trendy, sustainable and crafted for the city. Explore our curated collection.</p>
        <div style="margin-top:14px">
          <button class="cta" id="btn-shop">Shop Now</button>
        </div>
      </div>
      <div class="hero-right">
        <img src="${PRODUCTS[0].img}" alt="" style="width:320px;border-radius:12px;box-shadow:0 30px 80px rgba(2,6,13,0.6)">
      </div>
    </section>

    <section style="margin-top:22px">
      <div style="display:flex;justify-content:space-between;align-items:center">
        <h2>Featured</h2>
        <a href="#/products" class="muted">View all →</a>
      </div>
      <div class="grid" id="featured-grid"></div>
    </section>
  `;

  document.getElementById('btn-shop').addEventListener('click', ()=> location.hash='#/products');

  const grid = document.getElementById('featured-grid');
  PRODUCTS.slice(0,4).forEach(p=>{
    const card = document.createElement('div'); card.className='card';
    card.innerHTML = `
      <div class="tag-3d">NEW</div>
      <img class="prod-img" src="${p.img}" alt="${escapeHTML(p.title)}">
      <div class="prod-title">${escapeHTML(p.title)}</div>
      <div class="prod-sub muted">Trendy design • Urban fit</div>
      <div class="prod-row">
        <div class="price">${SITE.currencySymbol} ${p.price.toFixed(2)}</div>
        <button class="add-btn" data-id="${p.id}">Add</button>
      </div>
    `;
    grid.appendChild(card);
  });
  attachAddButtons();
}

function renderProducts(){
  AUTH_BTN.textContent = SESSION ? `Hi, ${SESSION}` : 'Login';
  ROOT.innerHTML = `
    <h2>All Products</h2>
    <div class="grid" id="product-grid"></div>
  `;
  const grid = document.getElementById('product-grid');
  PRODUCTS.forEach(p=>{
    const card = document.createElement('div'); card.className='card';
    card.innerHTML = `
      <div class="tag-3d">TREND</div>
      <img class="prod-img" src="${p.img}" alt="${escapeHTML(p.title)}">
      <div class="prod-title">${escapeHTML(p.title)}</div>
      <div class="prod-sub muted">Limited stock</div>
      <div class="prod-row">
        <div class="price">${SITE.currencySymbol} ${p.price.toFixed(2)}</div>
        <button class="add-btn" data-id="${p.id}">Add</button>
      </div>
    `;
    grid.appendChild(card);
  });
  attachAddButtons();
}

function renderLogin(){
  ROOT.innerHTML = `
    <h2>Login</h2>
    <div class="form">
      <input id="login-email" placeholder="Email" />
      <input id="login-password" placeholder="Password" type="password" />
      <div style="display:flex;gap:8px;margin-top:12px">
        <button id="btn-login" class="btn-primary">Login</button>
        <button id="btn-to-register" class="btn-outline">Register</button>
      </div>
    </div>
  `;
  document.getElementById('btn-to-register').addEventListener('click', ()=> location.hash='#/register');
  document.getElementById('btn-login').addEventListener('click', ()=>{
    const email = document.getElementById('login-email').value.trim().toLowerCase();
    const pass = document.getElementById('login-password').value;
    if(!email || !pass){ alert('Enter email and password'); return; }
    if(!USERS[email]){ alert('User not found. Please register.'); return; }
    if(USERS[email].password !== pass){ alert('Incorrect password'); return; }
    SESSION = email; saveSession(); alert('Logged in'); location.hash='#/home'; renderRoute();
  });
}

function renderRegister(){
  ROOT.innerHTML = `
    <h2>Create Account</h2>
    <div class="form">
      <input id="reg-name" placeholder="Full name" />
      <input id="reg-email" placeholder="Email" />
      <input id="reg-password" placeholder="Password" type="password" />
      <div style="display:flex;gap:8px;margin-top:12px">
        <button id="btn-register" class="btn-primary">Register</button>
        <button id="btn-to-login" class="btn-outline">Login</button>
      </div>
    </div>
  `;
  document.getElementById('btn-to-login').addEventListener('click', ()=> location.hash='#/login');
  document.getElementById('btn-register').addEventListener('click', ()=>{
    const name = document.getElementById('reg-name').value.trim();
    const email = (document.getElementById('reg-email').value||'').trim().toLowerCase();
    const pass = document.getElementById('reg-password').value;
    if(!name||!email||!pass){ alert('Fill all fields'); return; }
    if(USERS[email]){ alert('Email already registered'); return; }
    USERS[email] = {name, email, password: pass};
    save('tf_users', USERS);
    SESSION = email; saveSession();
    alert('Account created and logged in');
    location.hash='#/home';
    renderRoute();
  });
}

function renderCheckout(){
  if(!SESSION){ if(!confirm('You must login to checkout. Login now?')) return location.hash='#/login'; location.hash='#/login'; return; }
  const items = Object.keys(CART).map(id=>{
    const p = PRODUCTS.find(x=>x.id===id);
    return {id:p.id, title:p.title, price:p.price, qty:CART[id], subtotal: p.price * CART[id], img:p.img}
  });
  if(items.length===0){ alert('Cart is empty'); location.hash='#/products'; return; }

  let total = items.reduce((s,it)=> s+it.subtotal, 0);

  ROOT.innerHTML = `
    <h2>Checkout</h2>
    <div style="display:flex;gap:18px;flex-wrap:wrap">
      <div style="flex:1;min-width:300px">
        <div class="form">
          <h3>Shipping details</h3>
          <input id="ship-name" placeholder="Full name" value="${escapeHTML(USERS[SESSION].name)}" />
          <input id="ship-phone" placeholder="Phone" />
          <input id="ship-address" placeholder="Address, city, pincode" />
        </div>
      </div>
      <div style="width:380px">
        <div class="form">
          <h3>Order summary</h3>
          <div id="summary-items"></div>
          <div style="margin-top:12px;display:flex;justify-content:space-between">
            <div class="muted">Total</div>
            <div style="font-weight:800">${SITE.currencySymbol} ${total.toFixed(2)}</div>
          </div>
          <div style="margin-top:12px;display:flex;gap:8px">
            <button id="btn-pay" class="btn-primary">Place Order (Demo)</button>
            <button id="btn-cancel" class="btn-outline">Cancel</button>
          </div>
          <div style="margin-top:10px;color:var(--muted);font-size:0.9rem">
            This is a demo checkout. To accept real payments integrate Stripe or Razorpay (I can provide).
          </div>
        </div>
      </div>
    </div>
  `;

  const summary = document.getElementById('summary-items');
  items.forEach(it=>{
    const el = document.createElement('div'); el.style.display='flex'; el.style.justifyContent='space-between'; el.style.marginTop='8px';
    el.innerHTML = `<div>${escapeHTML(it.title)} x ${it.qty}</div><div>${SITE.currencySymbol} ${it.subtotal.toFixed(2)}</div>`;
    summary.appendChild(el);
  });

  document.getElementById('btn-cancel').addEventListener('click', ()=> location.hash='#/cart');
  document.getElementById('btn-pay').addEventListener('click', ()=> {
    // demo payment: create order, clear cart, save
    const order = {
      id: 'ORD' + Date.now(),
      email: SESSION,
      items,
      total,
      date: new Date().toISOString()
    };
    ORDERS.push(order); save('tf_orders', ORDERS);
    CART = {}; saveCart();
    alert('Order placed! Order ID: ' + order.id);
    location.hash='#/orders';
  });
}

function renderOrders(){
  if(!SESSION){ alert('Login to see orders'); location.hash='#/login'; return; }
  ROOT.innerHTML = `<h2>Your Orders</h2><div id="orders-list"></div>`;
  const list = document.getElementById('orders-list');
  const my = ORDERS.filter(o=>o.email===SESSION);
  if(my.length===0){ list.innerHTML = '<div class="muted">No orders yet.</div>'; return; }
  my.reverse().forEach(o=>{
    const el = document.createElement('div'); el.className='card'; el.style.marginBottom='12px';
    el.innerHTML = `<div style="display:flex;justify-content:space-between"><div><strong>Order ${o.id}</strong><div class="muted">${new Date(o.date).toLocaleString()}</div></div><div style="font-weight:800">${SITE.currencySymbol} ${o.total.toFixed(2)}</div></div>`;
    o.items.forEach(i=>{
      const item = document.createElement('div'); item.style.marginTop='8px';
      item.innerHTML = `${escapeHTML(i.title)} x ${i.qty} — ${SITE.currencySymbol} ${i.subtotal.toFixed(2)}`;
      el.appendChild(item);
    });
    list.appendChild(el);
  });
}

// ----- cart helpers -----
function attachAddButtons(){
  document.querySelectorAll('.add-btn').forEach(btn=>{
    btn.addEventListener('click', ()=> {
      addToCart(btn.dataset.id, 1);
      animateAdd(btn);
    });
  });
}
function addToCart(id, qty=1){
  CART[id] = (CART[id]||0) + qty;
  saveCart();
  updateCartUI();
}
function removeFromCart(id){ delete CART[id]; saveCart(); updateCartUI(); renderRoute(); }
function changeQty(id, qty){ if(qty<=0) removeFromCart(id); else CART[id]=qty; saveCart(); updateCartUI(); renderRoute(); }
function saveCart(){ save('tf_cart', CART); }
function updateCartUI(){
  const count = Object.values(CART).reduce((s,x)=>s+x,0);
  CART_COUNT.textContent = count;
  // render cart items in modal
  CART_ITEMS.innerHTML = '';
  let total=0;
  const ids = Object.keys(CART);
  if(ids.length===0) CART_ITEMS.innerHTML = '<p class="muted">Your cart is empty.</p>';
  ids.forEach(id=>{
    const p = PRODUCTS.find(x=>x.id===id);
    const qty = CART[id];
    const sub = p.price * qty; total += sub;
    const row = document.createElement('div'); row.className='cart-item';
    row.innerHTML = `<img src="${p.img}" alt=""><div class="meta"><div style="display:flex;justify-content:space-between"><div><strong>${escapeHTML(p.title)}</strong><div class="muted"> ${SITE.currencySymbol} ${p.price.toFixed(2)}</div></div><div>${SITE.currencySymbol} ${sub.toFixed(2)}</div></div><div class="qty-controls"><button class="dec" data-id="${id}">-</button><div style="min-width:32px;text-align:center">${qty}</div><button class="inc" data-id="${id}">+</button><button class="remove" data-id="${id}" style="margin-left:auto">Remove</button></div></div>`;
    CART_ITEMS.appendChild(row);
  });
  CART_TOTAL.textContent = total.toFixed(2);
  // listeners
  CART_ITEMS.querySelectorAll('.inc').forEach(b=> b.addEventListener('click', ()=> changeQty(b.dataset.id, CART[b.dataset.id]+1)));
  CART_ITEMS.querySelectorAll('.dec').forEach(b=> b.addEventListener('click', ()=> changeQty(b.dataset.id, CART[b.dataset.id]-1)));
  CART_ITEMS.querySelectorAll('.remove').forEach(b=> b.addEventListener('click', ()=> removeFromCart(b.dataset.id)));
}

function toggleCart(show){
  if(show){ CART_MODAL.classList.add('show'); CART_MODAL.setAttribute('aria-hidden','false'); } else { CART_MODAL.classList.remove('show'); CART_MODAL.setAttribute('aria-hidden','true'); }
}

// small UI nicety: button pulse
function animateAdd(btn){
  btn.animate([{transform:'translateY(0)'},{transform:'translateY(-6px)'},{transform:'translateY(0)'}],{duration:400,easing:'ease-out'});
}

// helpers
function escapeHTML(s=''){ return String(s).replace(/[&<>"']/g, c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c])); }

function saveSession(){ save('tf_session', SESSION); save('tf_users', USERS); save('tf_orders', ORDERS); save('tf_cart', CART) }

// initial load
function init(){
  AUTH_BTN.textContent = SESSION ? `Hi, ${SESSION}` : 'Login';
  updateCartUI();
}
init();
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Trendy Fashion — Shop</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header class="topbar">
    <div class="brand-wrap container">
      <div class="brand-3d">
        <div class="logo-face">TF</div>
      </div>
      <div class="brand-text">
        <div class="brand-title">Trendy Fashion</div>
        <div class="brand-sub">Premium • 3D • Urban</div>
      </div>

      <nav class="nav">
        <a href="#/home">Home</a>
        <a href="#/products">Products</a>
      </nav>

      <div class="header-actions">
        <button id="auth-btn" class="ghost">Login</button>
        <button id="open-cart" class="cart-btn">🛒 <span id="cart-count">0</span></button>
      </div>
    </div>
  </header>

  <main class="container main" id="app-root">
    <!-- app renders here -->
  </main>

  <!-- Cart Modal -->
  <div class="cart-modal" id="cart-modal" aria-hidden="true">
    <div class="cart-panel">
      <button class="close" id="close-cart">✕</button>
      <h2>Your Cart</h2>
      <div id="cart-items" class="cart-items"></div>
      <div class="cart-footer">
        <div class="total">Total: ₹ <span id="cart-total">0.00</span></div>
        <div class="cart-actions">
          <button id="clear-cart" class="btn-outline">Clear</button>
          <button id="go-to-checkout" class="btn-primary">Checkout</button>
        </div>
      </div>
    </div>
  </div>

  <footer class="footer">
    <div class="container footer-grid">
      <div>
        <div class="brand-title small">Trendy Fashion</div>
        <div class="muted">Premium apparel, direct to you.</div>
      </div>
      <div class="muted">© <span id="year"></span> Trendy Fashion</div>
      <div>Contact: +91 90000 00000</div>
    </div>
  </footer>

  <script src="app.js"></script>
</body>
</html>
