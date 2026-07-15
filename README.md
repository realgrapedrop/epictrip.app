<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/epictrip-wordmark-dark.svg">
  <img src="assets/epictrip-wordmark-light.svg" width="380" alt="Epic Trip">
</picture>

**The AI travel agent that builds your family road trip, rides along on the road, and turns its best moments into awarded badges on the XRP Ledger.**

[![Powered by XRPL](https://img.shields.io/badge/Powered%20by-XRPL-AFE6CE)](https://xrpl.org)
[![Make Waves 2026](https://img.shields.io/badge/Make%20Waves-2026-1C3B5A)](https://hackathons.xrpl-commons.org/)

Epic Trip is a trip planner for families. You describe the trip you want, and Roadie, the AI
travel agent built into the app, interviews you and builds the whole thing: the route, the
hotels, curated things to do at every stop, planned events, and an EV charging plan. Then the
app rides along during the trip itself, with checklists, a shared journal, group expenses, and
live vehicle status. And when someone earns it, a captain awards them a badge: a one of a
kind artwork in the Epic Trip style, minted on the XRP Ledger, that the family keeps forever.

> **This repo is the concept and the high level design, not the app's source code.** It exists
> so the Make Waves on XRPL community can see what Epic Trip is and exactly how it uses XRP,
> RLUSD, and the XRP Ledger.

<p align="center">
  <img src="assets/epictrip-how-it-works.svg" alt="How Epic Trip works: the app lane (tell Roadie about your trip, Roadie builds the whole trip, the crew rides along) and the XRP Ledger lane (a badge is awarded by a captain, one of a kind numbered art is created in the Epic Trip style, it is pinned to IPFS, and an NFT is minted to the family wallet). Payments settle in RLUSD, wallet to wallet." width="920">
</p>

## The idea

Planning a big family trip takes weeks, and the memories of it end up scattered across camera
rolls and group chats. Epic Trip fixes both halves.

- **The planning is done by an AI that does real work.** Roadie does not hand you a wall of
  suggestions. It writes an actual, structured, editable trip into the app, down to which
  Supercharger to stop at and what to do with the kids in each town.
- **The memories become awarded keepsakes on a public ledger.** When someone earns it, a
  captain or co pilot gives them a badge: Navigator, Road DJ, Trip MVP, and more. Each badge is
  one of a kind art in the Epic Trip house style, stamped with its category and a unique mint
  number, and minted to the family's wallet on the XRP Ledger. Not screenshots. Collectibles
  the family owns, viewable in any XRPL wallet, for pennies.

## Why the XRP Ledger

The ledger is the memory and money layer of Epic Trip, and it is what we are building during
Make Waves.

- **Trip Memory badges.** A captain or co pilot awards a badge to the person who earned it,
  writes what it was for, and the app paints a one of a kind artwork inspired by those words,
  pins it to IPFS with its metadata, and mints it as an NFT gifted to the family wallet. Each
  trip has a limited supply of badges, so every one means something. A full trip of awards
  costs well under a dollar, something only XRPL's tiny fees make sensible.
- **RLUSD payments.** The paid tier and extra AI trips settle in RLUSD, a digital dollar on the
  XRP Ledger. No card fees, no middleman, and the price of a subscription arrives whole.
- **Crew settle up.** The app already tracks who paid for what on the trip. Settle up squares
  the whole crew wallet to wallet in RLUSD for fractions of a cent.
- **We never hold anyone's money.** Every payment is signed in the member's own wallet. The
  only key the app keeps is the badge minter, and it holds pocket change.

## How a badge is born

1. A captain or co pilot awards a badge inside the app: they pick who earned it, pick a
   category (Navigator, Explorer, Snack Captain, Road DJ, Memory Keeper, Trooper, Trip MVP),
   and write what it was for.
2. The app paints one of a kind art in the Epic Trip style, inspired by what they wrote, and
   stamps it with the category and a globally unique mint number.
3. The art and its metadata are pinned to IPFS so any wallet or marketplace can render it.
4. An NFT is minted on the XRP Ledger (one collection per trip) and offered to the family
   wallet so that only they can claim it. Badges are soulbound: keepsakes, not trading cards.
5. The person who earned it gets an email with their badge, ready to share.

The public side of a badge is only its art, category, and mint number. Names, stories, and
places stay private with the family. Nothing personal ever goes on a public ledger.

## Why Epic Trip is different

- Trip organizers (TripIt, Wanderlog) tidy up bookings but cannot create a plan.
- AI chat planners suggest itineraries as text you still have to build somewhere else.
- Epic Trip's AI output **is** the app's live state, the app stays open during the trip, and no
  travel product anywhere mints your trip's memories on a public ledger.

## Under the hood

Epic Trip is a web app with passkey sign in (no passwords, ever) and a family crew model: two
captains, four co pilots, and four read only tagalongs per trip. The XRPL layer is built on the
proven core of **Tiplet**, our earlier Make Waves project: wallet connect (Xaman, GemWallet,
Crossmark), RLUSD settlement verified from the ledger itself, NFT minting via xrpl.js, IPFS
pinning, and AI art generation, all already tested on the XRPL Testnet.

## What we will never claim

- We never take custody of funds. Wallets sign, the ledger settles, we watch.
- Trip Memory badges are keepsakes, not investments. The art is generated and whimsical.
- We never put names, stories, or places on chain. The public side of a badge is art, a
  category, and a number.
- The AI plans well, but it is a travel agent, not a guarantee of good weather.

## Status

The app itself is built and running, the badge pipeline is live on the XRPL Testnet today
(art generated, pinned to IPFS, minted soulbound, gifted to the family wallet), and a real
family road trip happens inside the Make Waves window. The build order for the challenge:
awarded badges on Testnet, then Mainnet, then RLUSD subscriptions and settle up.

---

Built by [@realgrapedrop](https://github.com/realgrapedrop). Questions? DM
[@realgrapedrop](https://x.com/realgrapedrop) on X.
