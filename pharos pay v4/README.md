# PharosPay 🏛️

> USDC Payroll Platform on Pharos Atlantic Testnet

---

## 🚀 Deploy to Vercel (3 steps)

### Option A — Vercel CLI (fastest)
```bash
npm i -g vercel
vercel
```
Follow the prompts. Done — you get a live URL instantly.

---

### Option B — GitHub + Vercel Dashboard

1. **Push to GitHub**
   ```bash
   git init
   git add .
   git commit -m "PharosPay launch"
   gh repo create pharospay --public --push --source=.
   ```

2. **Import on Vercel**
   - Go to [vercel.com/new](https://vercel.com/new)
   - Click **"Import Git Repository"**
   - Select your `pharospay` repo
   - Leave all settings as default — Vercel auto-detects static
   - Click **Deploy**

3. **Done** — you get a `pharospay.vercel.app` URL

---

## ⚙️ Configuration

| Setting | Value |
|---|---|
| Framework | None (Static) |
| Build Command | *(leave empty)* |
| Output Directory | *(leave empty / `.`)* |
| Install Command | *(leave empty)* |

---

## 🔗 Network Details

| | |
|---|---|
| Network | Pharos Atlantic |
| Chain ID | 688689 |
| RPC | `https://atlantic.dplabs-internal.com` |
| Explorer | [testnet.pharosscan.xyz](https://testnet.pharosscan.xyz) |
| Faucet | [testnet.pharosnetwork.xyz](https://testnet.pharosnetwork.xyz) |

---

## 🧪 Test Mode

The app runs in **Test Mode** by default — payments are simulated, no real USDC needed.

To go live:
1. Deploy a MockERC20 contract on Pharos Atlantic (via Remix)
2. Open `index.html`, find `USDC_ADDRESS` and replace `'PASTE_YOUR_USDC_ADDRESS_HERE'` with your contract address
3. Set `TEST_MODE = false`
4. Redeploy

---

## 📁 File Structure

```
pharospay/
├── index.html      ← entire app (self-contained)
├── vercel.json     ← Vercel routing config
├── package.json    ← project metadata
└── .gitignore
```
