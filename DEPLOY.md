# DEPLOYMENT INSTRUCTIONS

## Step 1: Create GitHub Repository

Go to: https://github.com/organizations/Flame-Protocol/repositories/new

Create new repo:
- Name: `flame-fraud-detector`
- Description: `FLAME Protocol Fraud Detection System - SOX Compliant Analysis`
- Public
- DO NOT initialize with README (we have our own)

## Step 2: Deploy Files

Run these commands on flame-node-000:

```bash
cd ~/Downloads

# Unzip the package
unzip flame-fraud-detector.zip
cd flame-fraud-detector

# Initialize git and push
git init
git add .
git commit -m "Deploy FLAME Fraud Detection System v1.0"
git branch -M main
git remote add origin https://github.com/Flame-Protocol/flame-fraud-detector.git
git push -u origin main
```

## Step 3: Enable GitHub Pages

1. Go to: https://github.com/Flame-Protocol/flame-fraud-detector/settings/pages
2. Source: **Deploy from branch**
3. Branch: **main** / **(root)**
4. Click **Save**

Wait 2-3 minutes for deployment.

## Step 4: Verify

Your fraud detector is now live at:
```
https://flame-protocol.github.io/flame-fraud-detector/
```

## File Structure

```
flame-fraud-detector/
├── index.html       # Main application (single-file, no dependencies)
├── README.md        # Documentation
└── DEPLOY.md        # This file
```

## How to Use for Client Submissions

### Before Processing ANY Transaction:

1. Open: https://flame-protocol.github.io/flame-fraud-detector/
2. Copy ALL text from client submission (emails, documents, screenshots)
3. Paste into the analysis box
4. Click **Analyze Content**
5. Check the score:

| Score | Action |
|-------|--------|
| 0-24 | ✅ Proceed with standard verification |
| 25-49 | ⚠️ Enhanced due diligence required |
| 50-99 | 🟡 Request additional verification before proceeding |
| 100-149 | 🔴 High risk - Do not proceed without investigation |
| 150+ | ⛔ DEFINITE FRAUD - Do not proceed |

6. Click **Download PDF Report**
7. Save report to client file

### Red Flags That Auto-Fail (Score 150+):

- Impossible amounts (trillions)
- "Pay fee to release funds"
- Lottery/inheritance/prince narratives
- Requests for credentials
- "Validate/sync your wallet"

## Updating the System

To add new fraud patterns or update the interface:

1. Edit `index.html` locally
2. Push to GitHub:
```bash
cd ~/Downloads/flame-fraud-detector
git add .
git commit -m "Update fraud patterns"
git push origin main
```

GitHub Pages will auto-deploy in ~2 minutes.

## Support

- Email: admin@flameqmm.app
- Phone: 916-891-7552
