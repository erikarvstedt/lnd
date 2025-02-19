# Release Notes

## DB

* Split channeldb [`UpdateInvoice`
  implementation](https://github.com/lightningnetwork/lnd/pull/7377) logic in 
  different update types.

## Watchtowers 

* Let the task pipeline [only carry 
  wtdb.BackupIDs](https://github.com/lightningnetwork/lnd/pull/7623) instead of 
  the entire retribution struct. This reduces the amount of data that needs to 
  be held in memory. 

## RPC

* [SendOutputs](https://github.com/lightningnetwork/lnd/pull/7631) now adheres
  to the anchor channel reserve requirement.

* The [UpdateNodeAnnouncement](https://github.com/lightningnetwork/lnd/pull/7568)
  API can no longer be used to set/unset protocol features that are defined by 
  LND.  

  Custom node announcement feature bits can also be specified in config using 
  the `dev` build tag and `--protocol.custom-nodeann`, `--protocol.custom-init` 
  and `--protocol.custom-invoice` flags to set feature bits for various feature
  "sets", as defined in [BOLT 9](https://github.com/lightning/bolts/blob/master/09-features.md).

## Misc

* [Generate default macaroons
independently](https://github.com/lightningnetwork/lnd/pull/7592) on wallet
unlock or create.


# Contributors (Alphabetical Order)

* Carla Kirk-Cohen
* Daniel McNally
* Elle Mouton
* hieblmi
* Jordi Montes
