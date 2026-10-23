# Redesign Your Favourite App on Solana — Jupiter ("Intent Studio & Execution Guard")
**Bounty:** Superteam India — *Redesign Your Favourite App on Solana* ($1,500 USDC)
**Designer / Handle:** `big-chungus`
**Live Prototype Package:** `/workspace/bounties/high-value/solana-app-redesign-jupiter/index.html` (Interactive Before/After + Desktop/Mobile Switcher)

---

## Direct Answers to Superteam Earn Eligibility Questions

1. **Which app did you redesign, and which features did you pick?**
   We redesigned **Jupiter (`jup.ag`)** across Desktop and Mobile, focusing on four tightly connected core interactions:
   - **(1) Pre-Sign Outcome & MEV/Slippage Confidence Strip:** Replacing buried slippage settings with a visual "Min Received vs. Expected Range" confidence bar right inside the swap card.
   - **(2) Unified Intent Switcher (Instant / Limit / DCA / Value-Average):** Collapsing four separate top-level tabs into a single inline execution-mode pill bar that preserves token pair state when switching modes.
   - **(3) Real-Time Validator Landing & Priority Fee Predictor:** Showing actual post-Alpenglow landing probability (`Standard` vs `Turbo` vs `Jito Protected`) in plain dollar terms (`$0.004`) rather than cryptic lamport/micro-lamport toggles.
   - **(4) One-Thumb Mobile Execution Sheet:** Moving the mobile token selector, percentage quick-chips (`25% / 50% / MAX`), and slide-to-confirm action into the bottom 45% thumb zone.

2. **What was the biggest problem you found in the current design, in 2–3 sentences?**
   New and intermediate users face severe cognitive overload on Jupiter because critical execution parameters—dynamic slippage, MEV protection, priority fee landing probability, and multi-hop route price impact—are fragmented across separate modals and developer-oriented settings menus. Furthermore, switching between Instant Swap, Limit Order, and DCA resets the user's mental model and screen layout, while on mobile the primary token-selection and amount controls sit in the upper unreachable thumb zone.

---

## UX Case Study: Why This Redesign Improves the Experience

### Problem 1: Hidden Slippage & Fee Anxiety Before Signing
- **Before (Current Jupiter UX):** Users see a single quoted output number and small badges like `Dynamic 0.5%` or ` Ultra` at the top corner. When volatility spikes, users either get reverted transactions or suffer unexpected slippage without understanding why.
- **After (Redesigned "Execution Guard" Card):** Directly beneath the `You Receive` field, a clean visual range bar displays **Guaranteed Floor (`Minimum Received`)** alongside **Expected Fill**, plus a single toggle between **MEV Shield (Zero Sandwich)** and **Fastest Quorum**.

### Problem 2: Fragmented Tabs Between Swap, Trigger (Limit), and Recurring (DCA)
- **Before (Current Jupiter UX):** Switching from a Market Swap to a Limit Order or DCA navigates to a different view with different card geometry, forcing users to re-orient.
- **After (Inline Intent Pill Bar):** A tactile 3-segment switcher (`Instant` · `Target Price` · `Split Over Time`) morphs only the bottom 72px parameter tray inside the same card while preserving token pair, balance badges, and route visualization.

### Problem 3: Mobile Ergonomics & Multi-Step Modals
- **Before (Current Jupiter Mobile):** Selecting a token or adjusting slippage opens stacked overlays that obscure live chart movement and require top-of-screen reach.
- **After (Bottom-Anchored Thumb Sheet):** All interactive controls live in the lower ergonomic zone with a 1-tap `Compare Before / After` and `Desktop / Mobile` toggle in `index.html`.
