# ore-pool-cli

ore-pool is the first mining pool project since the launch of ORE v2. Users can connect to the pool using **ore-pool-cli** to contribute computing power and earn ORE rewards, with all costs covered by the pool.

Website: https://ore-pool.com/ (About mining pool's status and infos)

## Features
- Start mining with just your SOL address and computing power
- No private key, no gas fees, no RPC, no risk of loss
- Exclusive mining pool strategy to maximize machine profitability
- Friendly for low-power machines, profitable even with low reward rate

## Usage
### Download

- **Linux:** Download the `ore-pool-cli` binary (compatible with Ubuntu 20.04 and 22.04).
- **Windows:** Download the `ore-pool-cli.exe` executable.
- **macOS:**
  - For Apple Silicon (M1/M2), download `ore-pool-cli_aarch64-apple-darwin`.
  - For Intel x86 architecture, download `ore-pool-cli_x86_64-apple-darwin`.


### Mine
```
./ore-pool-cli mine --address YOUR_SOL_ADDRESS
```
**Note: Currently, mining is on devnet. Mainnet mining will automatically start on August 6th, 2024, at 00:00 UTC.**

Running this single command starts mining immediately (Default to using machine threads for mining). You can use the same address on multiple machines, and all rewards will accumulate to the same address.

### Claim
**No need to claim manually.** The mining pool now automatically distribute ORE to addresses with pending amounts exceeding a certain threshold, typically 0.01 ORE, every hour on the hour.

### Status
```
./ore-pool-cli status --address YOUR_SOL_ADDRESS
-------------------------------------------------------------------
Status -- Claimable Rewards: 2.6377 ORE, Total Mined: 2.6377 ORE
Invitation -- Invite Code: DYA17D, Invites: 2, Rewards: 0.0023 ORE
-------------------------------------------------------------------
```
You can immediately check mining profits using this command. Additionally, the mining pool will send this information to the mining client program every few minutes.

## Service Fees
After extensive research and effort in developing the mining pool and optimizing mining strategies, as well as considering the operational costs of maintaining the pool (including machine, Gas, and RPC costs), a 7% base fee will be deducted from mining rewards as a service fee, and a dynamic fee that changes with the price of ORE.

## Invitation System
- Use an invitation code to get a 1% reduction in service fees.
- Invite others and earn 1% of their mining rewards (included in the 7% service fee).

### Mine with invitation code
```
./ore-pool-cli mine --address YOUR_SOL_ADDRESS --invcode INV_CODE
```
**Note: An invitation code can only be used during the initial registration of an address.**

## Disclaimer
**Important: Use at your own risk! This is NOT an official product. Not affiliated with ORE team.**

Due to the pool still being in the testing phase, the pool might be paused for updates or other reasons. Under normal circumstances, the client will automatically restart mining once the service is restored. To stay informed about the latest updates, please follow the Telegram Announcements channel.

## Community

[Telegram Group](https://t.me/ore_pool_group)

[Telegram Announcements](https://t.me/ore_pool_annoucement)

## Future Plans
- [x] **Build MacOS Client**
- **Optimize hash algorithm efficiency**
- **GPU Mining Support**
- **Open source the code after an audit**

Happy mining!