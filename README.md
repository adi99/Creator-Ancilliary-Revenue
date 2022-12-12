# NFT Club

## 💡 Inspiration



## 💻 What It Does

Solana Patreon is a Patreon-inspired dApp allowing creators to gain a following and provide unique benefits to their fans. Fans support creators with SOL by subscribing for benefits that the creators provide. As this application is 100% on chain, there is no person or platform in the middle dictating what is or is not allowed or taking a cut of a creator's revenue. This empowers creators both in terms of freedom and financially, allowing them to reap maximum reward for their work.

The three main pillars of this dApp are Creators, Benefits, and Subscriptions. Creators authenticate through their wallet, create Benefits they offer to their subscribers, have the ability to modify their relevant data and offerings through a Creator Hub, and have their own landing page for themselves and other users to view.

Benefits are constituted by a name, description, and an access link. The link is in place to route users to a page with relevant details of the Benefit offered.

Lastly, Subscriptions are the vehicle through which users support Creators, gaining access to the Benefits they offer and helping contribute with payments of SOL.

## ▶️ Demo

[![Solana Patreon Demo]()](https://www.loom.com/share/c9892eb6b47042f0b759df314083c05d 'Solana Patreon')

## 🧠 Challenges/Learnings

- Structuring our Rust program such that we could specify how much storage Creator and Benefit instances would take up. Since Solana needs to know how much rent to charge users, a dynamically-sizing data structure would not suit us. Having an arbitrary number of Benefits for each Creator forced us to devise a workaround.
- Coming up with a way to structure our Creator and Benefit accounts to allow fetching of all Benefits pertinent to a Creator without the use of a dynamically-sizing data structure and figuring out how to create them using a PDA.
- Finding a way to delete arbitrary Benefits without causing costly operations.
- Learning how to use Rust and Anchor to define constraints and permissions for error checking and security.
- Learning more about how Solana programs work and how to clean up corrupted data

## 🏅 Accomplishments

- Completing our first full stack blockchain project
- Creating a proof of concept of a dApp that can actually be used to empower creators
- Learning how to perform CRUD operations on the Solana blockchain
- Figuring out a cheap way to store creator's benefits on chain without a dynamically-resizing data structure

## 🚀 What's Next for Solana Patreon

- Adding a gatekeeper for additional security
- Creating a more seamless UI and experience

## 🏃️ Installing and Running Locally

- Make sure you have Rust, Anchor, Solana, and npm/yarn installed
- Clone the repository
- In project root, run `npm install`
- Run `anchor build`
- Run `anchor deploy`
- If `anchor deploy` fails due to insufficient funds, grant yourself more devnet SOL with `solana airdrop 2`
 - If failed deploys drain your SOL and the airdrop is rate limiting you, you can use `solana program close --buffers` to retrieve the SOL from the failed deploys.
- `cd app`
- Run `npm install`
- To start the app, run `npm run dev` and go to `http://localhost:3000` in your browser
