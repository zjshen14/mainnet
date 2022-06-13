# shield-v2 Upgrade

There is a planned upgrade on shentu-2.2 network at height `<TBD>`, which approximately correspond to `Date TBD`. The upgrade is a simple binary swap:

 1. Stop the running certik daemon after the upgrade height is reached (the node will stop producing new blocks asking for a binary update).
 2. Replace the binary with the v2.4.0 version.
 3. Start the daemon with the new binary.

Make sure you do <b>NOT</b> perform `certik unsafe-reset-all` or delete the data directory, as it will require you to sync from the beginning of shentu-2.2 network. The above steps are sufficient to perform this upgrade.

You can find the release notes and built binaries here: https://github.com/ShentuChain/shentu/releases/tag/v2.4.0.

### (Optional)

To automate your upgrade process, you can use [cosmovisor](https://docs.cosmos.network/master/run-node/cosmovisor.html). However, we encourage monitoring the process during the time of the actual upgrade to ensure the node upgrades in a timely manner.

