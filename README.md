---

# 🧠 AI Merchant Underwriting Agent

### For GrabCredit & GrabInsurance

Behavior-Based Embedded Finance Engine

---

## 🚀 Live Demo

🌐 **Website:**
[https://ai-underwriting-agent-grabon.vercel.app/login](https://ai-underwriting-agent-grabon.vercel.app/login)

🎥 **Loom Walkthrough (6 Parts):**
Part 1: [https://www.loom.com/share/2c56fd3d2c7247249b7716aa66353e2a](https://www.loom.com/share/2c56fd3d2c7247249b7716aa66353e2a)
Part 2: [https://www.loom.com/share/50dd0f14a938475e8b4e5f2e7792e060](https://www.loom.com/share/50dd0f14a938475e8b4e5f2e7792e060)
Part 3: [https://www.loom.com/share/534f8380580541a4a806627c6787de20](https://www.loom.com/share/534f8380580541a4a806627c6787de20)
Part 4: [https://www.loom.com/share/92efb13246ea454b82d355f99b73e4dd](https://www.loom.com/share/92efb13246ea454b82d355f99b73e4dd)
Part 5: [https://www.loom.com/share/9e3f11f0b24d4b239cd7624998e6e401](https://www.loom.com/share/9e3f11f0b24d4b239cd7624998e6e401)
Part 6: [https://www.loom.com/share/7f9f4c2419c94f7ca2588ca88c84581d](https://www.loom.com/share/7f9f4c2419c94f7ca2588ca88c84581d)

---

# 🏦 Problem Statement

GrabOn has transaction-level merchant data.

But today:

* Merchant lending decisions are static
* Risk is not dynamically priced
* Capital exposure is not simulated
* Offers are not behavior-triggered
* Insurance cross-sell is not embedded

This project answers:

> How can GrabOn convert transaction intelligence into a real embedded finance engine?

---

# 💡 What We Built

A **deterministic, explainable, behavior-based underwriting engine** that:

* Scores merchants using transaction behavior
* Assigns risk tiers
* Dynamically prices credit
* Simulates NBFC capital exposure
* Triggers WhatsApp offer delivery
* Logs every decision for audit
* Supports stress testing

This is not UI simulation.
This is financial logic operationalized.

---

# 🧮 Core Financial Logic

All underwriting decisions are built using structured financial formulas.

---

## 1️⃣ Risk Score Model

Risk is computed using weighted transaction features:

* Revenue stability
* Refund ratio
* Coupon dependency
* Customer concentration
* Order frequency
* Seasonality volatility

Each feature contributes to a final **0–100 risk score**.

---

## 2️⃣ Probability of Default (PD)

Mapped from risk score:

PD = Risk Score / 100

Used in capital modeling.

---

## 3️⃣ Expected Loss (EL)

EL = PD × Exposure × LGD

Where:

* Exposure = Loan Limit
* LGD = Loss Given Default (assumed %)

---

## 4️⃣ RAROC

RAROC = (Interest Income − Expected Loss) / Capital Allocated

Ensures capital efficiency.

---

## 🎯 Tiering Logic

| Tier   | Risk Score | Meaning       |
| ------ | ---------- | ------------- |
| Tier 1 | 0–30       | Low Risk      |
| Tier 2 | 31–60      | Moderate Risk |
| Tier 3 | 61–80      | High Risk     |
| Reject | 81+        | Too Risky     |

---

# 🧩 System Architecture

```
Merchant Data
     ↓
Risk Engine (src/lib/risk-engine.ts)
     ↓
Pricing Engine (pricing.ts)
     ↓
Exposure Control (exposure.ts)
     ↓
Offer Decision
     ↓
WhatsApp Trigger (twilio.ts)
     ↓
Audit Log (logger.ts)
     ↓
Admin Panel
```

Built using:

* Next.js (App Router)
* TypeScript
* Bun runtime
* Tailwind CSS
* shadcn/ui
* Twilio WhatsApp
* Vercel Deployment

---

# 🗂 Project Structure (Not exactly correct, will be changed later)

```
ai-underwriting-agent-grabon/
│
├── public/                  # Static assets
├── src/
│   ├── app/
│   │   ├── admin/           # Admin dashboard
│   │   ├── dashboard/       # Merchant dashboard
│   │   ├── login/           # Role-based login
│   │   └── profile/
│   │
│   ├── components/          # UI components
│   ├── hooks/
│   ├── lib/                 # Core underwriting engines
│   │   ├── risk-engine.ts
│   │   ├── pricing.ts
│   │   ├── exposure.ts
│   │   ├── twilio.ts
│   │   └── claude.ts
│   │
│   ├── types/
│   └── data/
│
├── README.md
├── package.json
└── next.config.ts
```

---

# 📊 Key Features Demonstrated

### ✅ Tier 1 Merchant Approval

Low refund, stable revenue → high limit, low rate

### ✅ Tier 3 Merchant

Higher volatility → lower limit, higher rate

### ❌ Rejection Case

High refund ratio + high concentration → auto reject

### 📩 WhatsApp Offer Delivery

Offer sent programmatically

### 🧾 Admin Audit Panel

Every underwriting decision logged

### ⚡ Stress Testing

Modify refund ratio → tier changes live

---

# 💻 Local Setup
git clone https://github.com/sai-vishal03/ai-underwriting-agent-grabon.git
cd ai-underwriting-agent-grabon
npm install
npm run dev

Visit:
http://localhost:3000

---

# 🧠 Why This Is Strong

This system demonstrates:

* Deterministic underwriting
* Capital simulation
* Risk-based pricing
* Explainability
* Offer distribution
* Audit compliance
* Stress test modeling

It simulates how NBFC partners would actually evaluate embedded merchant loans.

---

# 🔌 Future Enhancements (High-Impact Roadmap)

## 1️⃣ Bureau Score Integration

Integrate CIBIL/Experian API to blend external credit profile with transaction data.

---

## 2️⃣ PayU / Payment Rails Integration

Connect real settlement data for:

* Live cashflow-based lending
* Real-time repayment tracking
* Settlement-linked deductions

---

## 3️⃣ Production PD Model

Replace deterministic PD with:

* Logistic Regression
* Gradient Boosting
* Survival Model for default timing

---

## 4️⃣ Insurance Underwriting Layer

Add:

* Claim probability model
* Merchant fraud detection
* Dynamic premium pricing

---

## 5️⃣ MCP (Model Context Protocol) Integration

Although not required in the brief, this system can integrate MCP to:

* Connect structured merchant context to LLM agents
* Enable conversational underwriting review
* Allow natural-language credit analyst queries
* Auto-generate risk memos
* Build AI Credit Committee simulations

This would transform the engine into a full AI Risk Co-Pilot.

---

## 6️⃣ Real-Time Capital Dashboard

* Portfolio VaR
* Sector concentration heatmap
* Dynamic provisioning simulation

---

# 🏁 Business Impact

If deployed at scale:

* GrabOn monetizes transaction intelligence
* Embedded finance increases merchant stickiness
* NBFC risk becomes data-driven
* Insurance cross-sell becomes behavior-based
* Capital allocation becomes optimized

This moves GrabOn from:

Affiliate Platform → Embedded Financial Infrastructure Layer

---

# 🏆 Final Positioning

This project demonstrates how GrabOn can:

* Operationalize its proprietary transaction data moat
* Deploy behavior-based merchant finance
* Ensure explainability and audit compliance
* Simulate capital economics realistically

We are not just offering loans.

We are turning transaction intelligence into a financial services engine.

---

📜 License

MIT

---
