# fiesta plugin inventory

The 56 root-level plugin JARs across the five live Oracle and Luna plugin directories were inventoried at 03:06 IST on 2026-11-26. FiestaSpawnGuard 1.0.1 was deployed to Oracle main at 04:00. At 05:16, ViaVersion and ViaBackwards 5.12.3 were deployed to Oracle main, Oracle queue, and Luna queue; all six JARs were rehashed and load-checked after startup. The remaining 49 JARs and 13 Oracle PlaceholderAPI expansions retain the hashes from the 03:06 check. A JAR in the plugins folder may not have loaded. Versions come from JAR metadata; SHA-256 identifies the inspected file. Some are custom Fiesta plugins.

Get third-party plugins from their official publishers and check licenses and compatibility before using them. The following custom projects are available separately: [AgyBridge](https://github.com/open-fiestasmp/AgyBridge), [FiestaChatArchive](https://github.com/open-fiestasmp/FiestaChatArchive), [FiestaFlightGuard](https://github.com/open-fiestasmp/FiestaFlightGuard), [FiestaGlobalQueue](https://github.com/open-fiestasmp/FiestaQueueBridge), [FiestaPhysicalMarket](https://github.com/open-fiestasmp/FiestaPhysicalMarket), [FiestaQueueHold](https://github.com/open-fiestasmp/FiestaQueueHold), and [FiestaSpawnGuard](https://github.com/open-fiestasmp/FiestaSpawnGuard). The AgyBridge and FiestaChatArchive repositories omit Fiesta-specific locations or paths; their published builds therefore differ from the installed jars. This inventory includes no plugin binaries, configs, or player databases.

## PlaceholderAPI expansions

These 13 expansion JARs were present on the Oracle game server on 2026-11-25. They are separate from the 56 root-level plugin JARs below. Their JARs do not declare a version in the metadata inspected, so the table records the installed filename and SHA-256 instead. Expansion JARs and their configuration are not included here.

| Jar | Expansion | Version | SHA-256 |
| --- | --- | --- | --- |
| `Expansion-chunkexplore.jar` | ChunkExplore | not declared | `c0bc57aaba0c8ce3b8cd373a5d2bddb1191145c5737bef717abc5d5b260c4510` |
| `Expansion-currency.jar` | Currency | not declared | `99985fd037741af2d65e260b59a232498696e61f4a03c6d55243998ba63351fe` |
| `Expansion-fiestaemerald.jar` | FiestaEmerald | not declared | `5441186de8a01681f670a0e47f6cdcfeb2f7d14e85b875556fb57f7d0b9db8a5` |
| `Expansion-fiestaphysical.jar` | FiestaPhysical | not declared | `585d750be2f24ca73a0b0bca682fc835c039e39ae28d86341cd468b886090242` |
| `Expansion-fiestasell.jar` | FiestaSell | not declared | `101294616e9ee226c4b78567904b1dac8b03adf3744d6db6729ee5b0c420c795` |
| `Expansion-fiestaworldinfo.jar` | FiestaWorldInfo | not declared | `1e1cc106088d2f4c063f19c6c3c4d3e24c4e823b6a2fc5fd85bf022bc7cafbc6` |
| `Expansion-fixexplosions.jar` | FixExplosions | not declared | `dfa3a1c6ce8ec21364e153c0732f48dd2c73acad3d92d23872c181ffde6f11d9` |
| `Expansion-player.jar` | Player | not declared | `a35574bbbe9ce8868821154371fd754e66402a3828c7453b8ce32bc536e8ac6c` |
| `Expansion-rtp.jar` | RTP | not declared | `fa53f50d58afca2e4770247db4df88de8a0fd3c5112fe9d383a91a9aa7ef5d7d` |
| `Expansion-server.jar` | Server | not declared | `91c7b6983b95905208e73d998ed0e18b1ff5c057cd910329392cc0332e9a3f21` |
| `Expansion-statistic.jar` | Statistic | not declared | `24bace77953663c1f432dbf179dfedaea4950d1875dad56615eb78fe3ffb5cee` |
| `Expansion-teams.jar` | Teams | not declared | `0ddd17eff3f6d08195369e7042b5be6075e4dc4bc5f1e56f92c2ffdcacb646ed` |
| `Expansion-vault.jar` | Vault | not declared | `33d630ede9a4c1cb2c0bd4ef1d382f95c7614c80de45a354d2a09e8f5669ca5e` |

## Oracle game server

| Jar | Plugin | Version | SHA-256 |
| --- | --- | --- | --- |
| `AgyBridge.jar` | AgyBridge | `1.0.0` | `c3777cae05049bb8101af163f37095691fc881048b4bc2b4d8a6a11478fd3120` |
| `AuthMe-6.0.1-Paper.jar` | AuthMe | `6.0.1-b2770` | `7704335e9e73a634d9d926344f77897f4c74f78f82453a59f5aa0f8d2722450a` |
| `BlueMap-5.29-spigot.jar` | BlueMap | `5.29` | `8b1fa1d5b86b5db212be1812af904afee90939b57594c849f487b132d5200d29` |
| `ChatFilter.jar` | ChatFilter | `1.0.0` | `45d2e9f6e93c754a0f5e5c7badf22562276bbac53623f81cb969732f32b8cb4e` |
| `Chunky-Bukkit-1.5.3.jar` | Chunky | `1.5.3` | `530d2c7430a96a39957391b7088be144daa3108f7665896d1c23aa8dd4af32f3` |
| `CoreProtect-24.0.jar` | CoreProtect | `24.0` | `66cd362089bb8430e5a018ee77e9b433bf0dc9e65590d5f1a043a78d60415696` |
| `DecentHolograms-2.10.2.jar` | DecentHolograms | `2.10.2` | `99bc2b7b0af7846cc45d5800ea0acfae6846d479e048b8e5995c5afa53df27be` |
| `DeluxeMenus.jar` | DeluxeMenus | `1.14.1-Release` | `ec10a1317152aa57d76eec8cb3e1e7dc7f52e45c7a5d742c0baa1e394496ec20` |
| `EssentialsX-2.22.0.jar` | Essentials | `2.22.0` | `bda4685105977fca2e209820a9f0ad24275bd103390a03236f38e59bfdac58e6` |
| `EssentialsXChat-2.22.0.jar` | EssentialsChat | `2.22.0` | `e5b0211f98af1eaba712d9294997639a39209db1fc842394a0923820073ec65a` |
| `EssentialsXSpawn-2.22.0.jar` | EssentialsSpawn | `2.22.0` | `dd5377c4c921b9b67814209f4f6646ffbb959729003e721ec5e63c47c7c010b8` |
| `FiestaChatArchive.jar` | FiestaChatArchive | `1.1.0` | `0411cdbfdebdb2065a8e6bdf91c17cf125f631ecdad56708e4646cf693a40e64` |
| `FiestaFlightGuard.jar` | FiestaFlightGuard | `1.0.0` | `786b0182ba031f4dc4742eb859aa7d976c8af9eeeea25ecfb4556e3d68080c53` |
| `FiestaPhysicalMarket.jar` | FiestaPhysicalMarket | `0.2.0` | `9ccc67062f424b04109b6b357337a6a27d01cb06c928066dfc7fb20eb7a17f8e` |
| `FiestaSpawnGuard.jar` | FiestaSpawnGuard | `1.0.1` | `efc71f9c0d21bacdd8a996ba725ab854e017922f4b7395be29080d921f1b466c` |
| `GrimAC.jar` | GrimAC | `2.3.74` | `3ac71c0b6ef8ab586c1dd3ab4c0b3254394ef39d048e4985efb2898b9fef628c` |
| `LandClaimPlugin-3.4.0.jar` | LandClaimPlugin | `3.4.0` | `5d9c64fcd1225a0820c4b634b6a52e682e38599d90f19fbb7ee6b4f4c65ce53e` |
| `LuckPerms-Bukkit-5.5.71.jar` | LuckPerms | `5.5.71` | `49cecb66fa1fd22a133039a490e9c1e5095a238e7cd66eb9d2a16fe6c897550d` |
| `PlaceholderAPI.jar` | PlaceholderAPI | `2.12.3` | `fde03259f5af6938f3c33eeb4d814000a1adabf1d2304ce14970be81f609a437` |
| `SkinsRestorer.jar` | SkinsRestorer | `15.12.6` | `a85b4a370f988741c9a38f4d0498262edacbf3220314790ac1c127461996359c` |
| `TAB.jar` | TAB | `6.1.2` | `7ee17e6211abc025fafff0cf93ee97d1a21022cfd80aed696be32fab9f43c8bc` |
| `VaultUnlocked-2.20.2.jar` | Vault | `2.20.2` | `bd9e7a31f1b2d31a591497174887eea7ae7e632c6b179da13e4f0ad732de2df7` |
| `ViaBackwards-5.12.3.jar` | ViaBackwards | `5.12.3` | `181f3aadbd172ddc1819e2114d0c2aeccc640f2f1adf6d92144bfbedf1a96e83` |
| `ViaRewind.jar` | ViaRewind | `4.1.4-SNAPSHOT` | `d8d5e721aa2875878bf0a7a8f26d95055c896191246a9e85af977130add30a7c` |
| `ViaVersion-5.12.3.jar` | ViaVersion | `5.12.3` | `f7ee2e4f5bc9fd3fa93f4f5ae7e8a2292eb8adf8a0fbdbffbf880833bb4d7259` |
| `WorldEdit.jar` | WorldEdit | `7.4.5+7590-b8dc4c1` | `e5696a6d064b9969437a8888be91b0941148a28e0c3736de1554a00254a5d142` |
| `ajQueue.jar` | ajQueue | `2.9.1-b276` | `0e90e946b98ba9bd9aea0dbf97c2b8b9599e96ae8821e559b253f0c59a54a8c7` |
| `floodgate-spigot.jar` | floodgate | `2.2.5-SNAPSHOT` | `21570aff9ce17d6983928e8552777760e1ede5050026b04c686b0ae112e6fd7e` |
| `minimotd-paper-2.2.5.jar` | MiniMOTD | `2.2.5` | `a1f5bff3abf4c9c90bd4417ce26612e621c83a1564f3fc7aa39848996cbea6c6` |
| `packetevents-spigot.jar` | packetevents | `2.14.0` | `060087c58ec268eae7dd0eb1f17ac3bea1eaadda1693414141ff64e506091bd7` |

## Oracle proxy

| Jar | Plugin | Version | SHA-256 |
| --- | --- | --- | --- |
| `AuthMe-6.0.1-Velocity.jar` | AuthMe Velocity | `6.0.1-b2770` | `d2e511398e4a8bbecd38e9434a98610cc8fa081462df687efb04682e24939e6e` |
| `Geyser-Velocity.jar` | Geyser-Velocity | `2.12.1-b1284 (git-master-da836ca)` | `df0e646deb0b62d3092d0f9467ea192ffcdde342401d02c9c2e45ea351ef68dd` |
| `ajQueue.jar` | ajQueue | `2.9.1-b276` | `0e90e946b98ba9bd9aea0dbf97c2b8b9599e96ae8821e559b253f0c59a54a8c7` |
| `fiesta-global-queue.jar` | FiestaGlobalQueue | `0.1.0-dev` | `b05b43fa4eefa8ce01c760495fe1427a1527afb3f78e71c9512149f7aa323132` |
| `floodgate-velocity.jar` | floodgate | `2.2.5-SNAPSHOT (b141-81b65cc)` | `649835022de37ff09255fc626d4bfe7bc2a3b926d07b0dfaf1f51e12bf37001d` |
| `minimotd-velocity.jar` | MiniMOTD | `2.2.5` | `b5d01ae7596b951f842d105d8a70552bf75761ced2bd413739d627c59b058ed5` |
| `SkinsRestorer.jar` | SkinsRestorer | `15.12.6` | `a85b4a370f988741c9a38f4d0498262edacbf3220314790ac1c127461996359c` |

## Oracle queue

| Jar | Plugin | Version | SHA-256 |
| --- | --- | --- | --- |
| `FiestaQueueHold.jar` | FiestaQueueHold | `1.1.1` | `e3f9c07eb8424d43aec195fe38fa3d053b37c000be147a60d1e5a0bc9f99cee6` |
| `SkinsRestorer.jar` | SkinsRestorer | `15.12.6` | `a85b4a370f988741c9a38f4d0498262edacbf3220314790ac1c127461996359c` |
| `ViaBackwards-5.12.3.jar` | ViaBackwards | `5.12.3` | `181f3aadbd172ddc1819e2114d0c2aeccc640f2f1adf6d92144bfbedf1a96e83` |
| `ViaRewind.jar` | ViaRewind | `4.1.4-SNAPSHOT` | `d8d5e721aa2875878bf0a7a8f26d95055c896191246a9e85af977130add30a7c` |
| `ViaVersion-5.12.3.jar` | ViaVersion | `5.12.3` | `f7ee2e4f5bc9fd3fa93f4f5ae7e8a2292eb8adf8a0fbdbffbf880833bb4d7259` |
| `floodgate-spigot.jar` | floodgate | `2.2.5-SNAPSHOT` | `21570aff9ce17d6983928e8552777760e1ede5050026b04c686b0ae112e6fd7e` |

## Luna proxy

| Jar | Plugin | Version | SHA-256 |
| --- | --- | --- | --- |
| `AuthMe-6.0.1-Velocity.jar` | AuthMe Velocity | `6.0.1-b2770` | `d2e511398e4a8bbecd38e9434a98610cc8fa081462df687efb04682e24939e6e` |
| `Geyser-Velocity.jar` | Geyser-Velocity | `2.12.1-b1284 (git-master-da836ca)` | `df0e646deb0b62d3092d0f9467ea192ffcdde342401d02c9c2e45ea351ef68dd` |
| `ajQueue.jar` | ajQueue | `2.9.1-b276` | `0e90e946b98ba9bd9aea0dbf97c2b8b9599e96ae8821e559b253f0c59a54a8c7` |
| `fiesta-global-queue.jar` | FiestaGlobalQueue | `0.1.0-dev` | `b05b43fa4eefa8ce01c760495fe1427a1527afb3f78e71c9512149f7aa323132` |
| `floodgate-velocity.jar` | floodgate | `2.2.5-SNAPSHOT (b141-81b65cc)` | `649835022de37ff09255fc626d4bfe7bc2a3b926d07b0dfaf1f51e12bf37001d` |
| `minimotd-velocity.jar` | MiniMOTD | `2.2.5` | `b5d01ae7596b951f842d105d8a70552bf75761ced2bd413739d627c59b058ed5` |
| `SkinsRestorer.jar` | SkinsRestorer | `15.12.6` | `a85b4a370f988741c9a38f4d0498262edacbf3220314790ac1c127461996359c` |

## Luna queue

| Jar | Plugin | Version | SHA-256 |
| --- | --- | --- | --- |
| `FiestaQueueHold.jar` | FiestaQueueHold | `1.1.1` | `e3f9c07eb8424d43aec195fe38fa3d053b37c000be147a60d1e5a0bc9f99cee6` |
| `SkinsRestorer.jar` | SkinsRestorer | `15.12.6` | `a85b4a370f988741c9a38f4d0498262edacbf3220314790ac1c127461996359c` |
| `ViaBackwards-5.12.3.jar` | ViaBackwards | `5.12.3` | `181f3aadbd172ddc1819e2114d0c2aeccc640f2f1adf6d92144bfbedf1a96e83` |
| `ViaRewind.jar` | ViaRewind | `4.1.4-SNAPSHOT` | `d8d5e721aa2875878bf0a7a8f26d95055c896191246a9e85af977130add30a7c` |
| `ViaVersion-5.12.3.jar` | ViaVersion | `5.12.3` | `f7ee2e4f5bc9fd3fa93f4f5ae7e8a2292eb8adf8a0fbdbffbf880833bb4d7259` |
| `floodgate-spigot.jar` | floodgate | `2.2.5-SNAPSHOT` | `21570aff9ce17d6983928e8552777760e1ede5050026b04c686b0ae112e6fd7e` |
