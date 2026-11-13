# Rudpair

A prototype website for a stablecoin payroll product on the NEAR blockchain. Companies offer employees the option to receive salary in USDC or EURC, paid into the employee's own self-custody wallet. The company's wallet app adds services on top, but never holds the employee's private key.

**Status:** Prototype (Phase 0). All names, balances, rates and dates on the site are examples. "Rudpair" is a working name.

## What the site shows

The prototype is a single-page website that presents the product as a set of services and a phased roadmap.

### Six employee services

| Service | What it does |
| --- | --- |
| Flexible yield | Employees move idle USDC or EURC into a flexible pool and withdraw at any time. The APY is variable. |
| Hourly task swaps | An employee posts a task with role, hours and hourly rate. A colleague in a similar position takes it. Payment is held in escrow and released on confirmation. |
| Lifetime discount | A wallet-linked discount on the company's other products, applied automatically at checkout. |
| P2P transfers | Send stablecoins to another wallet by NEAR account name. RWA transfers follow each issuer's own rules. |
| Bill split | When several people take a service together, one creates a bill and the others approve and pay their share. The service activates once every share is funded. |
| Due bill | An alternative to a credit card. Employees take selected services now and repay from the next payslip, if the company allows it. Only services on a preset allowlist qualify. |

### Company and onboarding features

- **Company console:** each company sets up its own private workspace. It can switch services on or off, set the discount and due-bill limit, and add its name and brand color. A live phone preview shows what employees will see.
- **Access-code onboarding:** an employee joins a company with an access code, connects their wallet and agrees to share their KYC status and wallet address with the company. The demo code is `ACME-7K4Q`.

### Roadmap

| Phase | Scope |
| --- | --- |
| 0 | Prototype on NEAR testnet, wallet connect, clickable demo |
| 1 | Payroll contract, flexible yield, P2P transfers, access-code onboarding with KYC |
| 2 | Lifetime discount, bill split, company console |
| 3 | Task marketplace with escrow, due bill |
| 4 | RWA transfers, independent audit, mainnet pilot |

Each phase ends with a gate that must pass before the next one starts. Durations on the site are rough planning estimates.

## Trust model

The employee controls the money. The company controls the rules.

- The employee's wallet holds the private key and signs every transfer, deposit and payment.
- The company app handles payroll schedules, perk rules, ledgers and requests. It cannot move an employee's funds.
- The company sees an employee's wallet address and KYC status only after the employee joins with the access code and agrees.

## Open decisions

These need an owner before Phase 1:

- **EURC on NEAR.** Native USDC is live on NEAR. EURC availability needs to be confirmed with Circle. If it is missing, the options are a bridged EURC or another euro stablecoin.
- **Payroll law and tax.** Paying salary in stablecoins depends on each country. Get legal advice and written employee consent before any real payment.
- **Yield source.** Decide where the yield comes from and show its risks next to the rate.
- **Lifetime discount.** Decide whether it stays after an employee leaves.
- **Due-bill defaults.** Decide what happens if an employee leaves with an unpaid balance.
- **KYC and privacy.** Choose a KYC provider and decide which fields the company may see. Data protection law can limit this.
- **Lost keys.** Self-custody means the company cannot recover a lost key. Decide how employees are guided to back up their wallet.

## Project structure

```
Rudpair Prototype.html   The whole site: HTML, CSS and JavaScript in one file
README.md       This file
```

The file keeps its original name, `Rudpair Prototype.html`, from before the project was renamed to Rudpair.

## Running it

Open `Rudpair Prototype.html` in any modern browser. No build step or server is needed.

The page loads three fonts from Google Fonts (Bricolage Grotesque, IBM Plex Sans, IBM Plex Mono) and falls back to system fonts if they are unavailable. It has no other dependencies.

## Technical notes

- Plain HTML, CSS and vanilla JavaScript.
- Light and dark themes follow the viewer's system setting.
- Responsive down to phone width.
- Scroll effects: reveal on scroll, progress bar, active menu link, and a count-up on the payslip. They are turned off when the viewer's device has "reduce motion" enabled.
- The interactive demos (yield estimator, company console preview, access-code join, copy email) run entirely in the browser. Nothing is sent to a server and no blockchain is connected yet.

## Contact

- Email: c0c1mamun@gmail.com
- X: https://x.com/mamun0x
- web: mamun0.netlify.app
## Disclaimer

This is a prototype for demonstration. Nothing in it is financial, legal or tax advice.
