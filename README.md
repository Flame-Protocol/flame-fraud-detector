# FLAME Fraud Detection System

SOX-compliant fraud detection and analysis platform for checking client submissions.

## Live Demo
https://flame-protocol.github.io/flame-fraud-detector/

## Features

- **Real-time Analysis** - Paste suspicious content, get instant fraud scoring
- **SOX 404 Compliant** - Sarbanes-Oxley Section 404 internal controls
- **SHA-256 Verification** - Cryptographic hash of all analyzed content
- **Audit Trail** - Document IDs and timestamps for every analysis
- **Downloadable Reports** - Export analysis reports for records

## Scoring Methodology

| Score | Verdict | Recommended Action |
|-------|---------|-------------------|
| 150+ | DEFINITE FRAUD | DO NOT PROCEED - CONFIRMED SCAM |
| 100-149 | HIGHLY SUSPICIOUS | EXTREME CAUTION - LIKELY FRAUDULENT |
| 50-99 | SUSPICIOUS | ADDITIONAL VERIFICATION REQUIRED |
| 25-49 | QUESTIONABLE | ENHANCED DUE DILIGENCE RECOMMENDED |
| <25 | APPEARS LEGITIMATE | STANDARD VERIFICATION PASSED |

## Red Flag Categories

| Category | Points | Description |
|----------|--------|-------------|
| IMPOSSIBLE_AMOUNT | +80 | Amounts exceeding realistic limits |
| IMPOSSIBLE_METHOD | +70 | Invalid transfer methods (e.g., trillions to debit card) |
| ADVANCE_FEE | +70 | "Pay fee to release funds" patterns |
| KNOWN_SCAM | +70 | Prince/inheritance/lottery narratives |
| CREDENTIAL_HARVEST | +60 | Requests for card/PIN/password |
| WALLET_DRAIN | +60 | Wallet validation/sync scams |
| FALSE_PROMISE | +60 | "Guaranteed returns" / "Risk free" |
| BAIT_LANGUAGE | +60 | "Congratulations! You've won!" |
| FAKE_SYSTEM | +50 | "Connecting to database..." displays |
| FAKE_VERIFICATION | +50 | Fake "Identity Verified" messages |
| FAKE_APPROVAL | +50 | Fraudulent approval codes |
| INTERMEDIARY_SCAM | +50 | "Bridge/swap for me" requests |
| SECRECY_DEMAND | +50 | "Don't tell anyone" instructions |
| UNTRACEABLE_PAYMENT | +50 | Western Union/crypto only |
| URGENCY_TACTIC | +40 | "Act now!" pressure |
| OFFSHORE_INDICATOR | +30 | International transfer mentions |
| LEGITIMATE_MARKER | -10 to -15 | Valid IBAN/SWIFT/MT103 (reduces score) |

## Usage

### Web Interface
1. Open https://flame-protocol.github.io/flame-fraud-detector/
2. Paste suspicious content (email, screenshot text, document)
3. Click "Analyze Content"
4. Review score, verdict, and red flags
5. Download report for records

### Checking Client Submissions
Before processing any client transaction:
1. Copy all submitted documentation text
2. Run through fraud detector
3. If score ≥ 50: Request additional verification
4. If score ≥ 100: Do not proceed, investigate further
5. Save report to client file

## Installation (Self-Hosted)

```bash
git clone https://github.com/Flame-Protocol/flame-fraud-detector.git
cd flame-fraud-detector
# Open index.html in browser - no server required
```

## Deployment to GitHub Pages

```bash
cd ~/Downloads
git clone https://github.com/Flame-Protocol/flame-fraud-detector.git
cd flame-fraud-detector
# Add files
git add .
git commit -m "Deploy FLAME Fraud Detection System"
git push origin main
```

Then enable GitHub Pages:
1. Go to: https://github.com/Flame-Protocol/flame-fraud-detector/settings/pages
2. Source: Deploy from branch
3. Branch: main / (root)
4. Save

## API Integration (Coming Soon)

```javascript
// Future API endpoint
POST https://api.flameqmm.app/v1/fraud/analyze
Headers: X-API-Key: your_api_key
Body: { "content": "text to analyze" }
```

## Contact

**GB Dynamics Inc**
- Email: admin@flameqmm.app
- Phone: 916-891-7552

## Compliance

- SOX Section 404 Internal Controls
- SHA-256 Cryptographic Verification
- Immutable Audit Trail
- SPEC_HASH: 0xf1ab854ae097ac6445bd55ba58d903655ad1f41d6caadaa0a21a9b4c320046be

## License

Proprietary - GB Dynamics Inc / FLAME Protocol
