## Running a blog on the blockchain

- Practice project where I'm following along to a tutorial.

## Getting Started

- Run the development server: `npm run dev` or `yarn dev`. Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.
- To run the tests: `npx hardhat test`.
- To see test accounts: `npx hardhat node`. This command also starts the local network (so ensure this is running when you deploy your contract).

## How it was built

- Install NextJS and packages.
- Amend `hardhat.config.js`.
- Set up global styles and add relevant images to `public` folder.
- Add Blog contract to `contracts` folder.
- Set up blog tests in `test` folder to check you're happy with the contract.
- Set up the `deploy.js` script to deploy the contract. Ensure the local network is running using `npx hardhat node`, then deploy using `npx hardhat run scripts/deploy.js --network localhost`.
