## Running a blog on the blockchain

- Practice project where I'm following along to a tutorial.

## Getting Started

- Run the development server: `npm run dev` or `yarn dev`. Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.
- To run the tests: `npx hardhat test`.
- To see test accounts: `npx hardhat node`. This command also starts the local network (so ensure this is running when you deploy your contract).

## How it was built

### Setup

- Install NextJS and packages.
- Amend `hardhat.config.js`.
- Set up global styles and add relevant images to `public` folder.

### Write smart contract and deploy

- Add Blog contract to `contracts` folder.
- Set up blog tests in `test` folder to check you're happy with the contract.
- Set up the `deploy.js` script to deploy the contract. Ensure the local network is running using `npx hardhat node`, then deploy using `npx hardhat run scripts/deploy.js --network localhost`.
- Copy the private key of the first hardhat test account (by default, this is the owner of the contract), and import it to your Metamask extension. Be sure to set the network to localhost 8545.

### NextJS

- Create `.env.local` file in root directory and add `ENVIRONMENT="local"` and `NEXT_PUBLIC_ENVIRONMENT="local"`. This allows us to switch between `local`, `testnet` and `mainnet` environments.
- Set up `context.js` to manage state across the React app.
- Set up the app's layout in `pages/_app.ts`.
- Create `pages/index.tsx` and `pages/create-post.tsx`.
- Create route to view a post at `/pages/post/:id` and edit a post at `/pages/edit-post/:id`.

### Deploy to Mumbai testnet

- Add to the Mumbai testnet to your Metamask wallet with these [details](https://docs.polygon.technology/docs/develop/network-details/network/).
- Get some testnet tokens: [https://faucet.polygon.technology/](https://faucet.polygon.technology/)
