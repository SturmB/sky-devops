# Changelog

<a name="1.7.0"></a>
## 1.7.0 (2021-06-30)

### Added

- ✨ Adds SqlBak for the staging server's MySQL containers [[e38f90d](https://github.com/skyunlimitedinc/sky-devops/commit/e38f90d12ea69f6232ac31d58d03913f42396b03)]

### Changed

- 🔧 Fixes a couple of npm keywords [[c11ceef](https://github.com/skyunlimitedinc/sky-devops/commit/c11ceef42250a98044d922b785625c1ca6022161)]
- 🔧 Re-arranges `package.json` with `fixpack` [[2ba883d](https://github.com/skyunlimitedinc/sky-devops/commit/2ba883df72b281a48b2790ca153ebefe42e567b0)]
- 🔧 Fleshes out `package.json` [[b37a9a7](https://github.com/skyunlimitedinc/sky-devops/commit/b37a9a731b2b43531969d5f553e1ee24f256bf39)]
- 🔧 Adds PhpStorm config files [[fff86e5](https://github.com/skyunlimitedinc/sky-devops/commit/fff86e56430e397d2328808f0af900832e84807f)]

### Fixed

- 🐛 Fixes Sqlbak implementation [[7875943](https://github.com/skyunlimitedinc/sky-devops/commit/7875943a11f65a9ddc11bbaa48fb0351e707dd97)]
- 🐛 Ensures directories exist before templating to them [[2316c41](https://github.com/skyunlimitedinc/sky-devops/commit/2316c416b3fdefe4b5cb1f9c702829d29f220b12)]

### Miscellaneous

- 📝 Fixes the Table of Contents in the README [[57d11ef](https://github.com/skyunlimitedinc/sky-devops/commit/57d11ef0114b6f4519aceac5c9b4ee22b62da7db)]
- 🙈 Ignores files created by the VS Code 'Local History' extension [[191283d](https://github.com/skyunlimitedinc/sky-devops/commit/191283d88eaa24c191170789717011faad153ea5)]
- 📝 Updates the documentation [[7e56d0d](https://github.com/skyunlimitedinc/sky-devops/commit/7e56d0db2aad018deca4d2048b46b9f9d913a0ba)]


<a name="1.6.1"></a>
## 1.6.1 (2021-04-12)

### Miscellaneous

- 🚀 Adds 'deployer' user and sets it as owner for the web document [[35f6366](https://github.com/SturmB/sky-devops/commit/35f6366c68191e144fe7af61df3d5411a3a7b9c1)]


<a name="1.6.0"></a>
## 1.6.0 (2021-04-12)

### Added

- ✨ Adds a standalone Accents droplet [[6d36920](https://github.com/SturmB/sky-devops/commit/6d36920ca7cfa10715c929df89b54e69e988bf04)]

### Miscellaneous

- 📝 Fixes a spelling error [[adf668f](https://github.com/SturmB/sky-devops/commit/adf668f23355ebd7c0deb5a4de70afee2a655ef2)]


<a name="1.5.3"></a>
## 1.5.3 (2021-03-02)

### Miscellaneous

- 🩹 Tags redmine while provisioning [[b8c1314](https://github.com/SturmB/sky-devops/commit/b8c1314a6d5f826403773881e7cccf91e68a0d50)]
- 📦 Ensures necessary packages are installed for Laravel [[e4531b4](https://github.com/SturmB/sky-devops/commit/e4531b4e5d445fd804bca59b23dc0934a7c847c5)]


<a name="1.5.2"></a>
## 1.5.2 (2021-02-18)

### Miscellaneous

- 🩹 Sets the environment template to use redis for caching [[938847b](https://github.com/SturmB/sky-devops/commit/938847b48a31e6f6ca5ff85469745552f5f9935b)]


<a name="1.5.1"></a>
## 1.5.1 (2021-02-18)

### Changed

- 👽 Explicitly defines Docker container default behavior [[41451a4](https://github.com/SturmB/sky-devops/commit/41451a43b9e86fa387c73a626c0daaf6a1f25f73)]

### Miscellaneous

- ⚗️ Looks up the correct home directory [[3b476f4](https://github.com/SturmB/sky-devops/commit/3b476f449f5a774f4ce975646779743a9fb6fdb4)]


<a name="1.5.0"></a>
## 1.5.0 (2021-02-15)

### Added

- ✨ Adds redis and php-redis to Laravel servers [[eec3bb6](https://github.com/SturmB/sky-devops/commit/eec3bb6fc73ece11d244fd57521ada9bf3f110af)]

### Changed

- 🗃️ Uses the latest version of MySQL for ACS/AYS db [[c898e62](https://github.com/SturmB/sky-devops/commit/c898e6279163c21f2ea07dec722e63298f7e7ffd)]
- 🗃️ Sets Sky Schedule to use the latest MySQL version [[95498b1](https://github.com/SturmB/sky-devops/commit/95498b1dc1e71b9c10458a8f96993ee4e510ae2f)]

### Fixed

- 🐛 Restarts the balancer for all service-based playbooks [[3dd0bc6](https://github.com/SturmB/sky-devops/commit/3dd0bc601b5542927c7b8ee10f433fdbdad63953)]
- 🐛 Makes sure to restart the balancer if any of the services were changed [[2a91f84](https://github.com/SturmB/sky-devops/commit/2a91f8424523680e74ac7721dd8606d8b28c878f)]
- 🐛 Ensures php-redis is enabled in `php.ini` [[dc0b625](https://github.com/SturmB/sky-devops/commit/dc0b62508e3cf87fdf1f6732919028b6b2728cc3)]


<a name="1.4.2"></a>
## 1.4.2 (2021-02-09)

### Fixed

- 🐛 Adds Redis service to the `webservers.yml` playbook [[e82e032](https://github.com/SturmB/sky-devops/commit/e82e0321f88f0de623f956fecf146fc092e9964a)]


<a name="1.4.1"></a>
## 1.4.1 (2021-02-05)

### Fixed

- 🐛 Adds redis support + a custom volume for it [[5bb4f84](https://github.com/SturmB/sky-devops/commit/5bb4f84e186030244ecf021f6ebb2a2154ff4582)]


<a name="1.4.0"></a>
## 1.4.0 (2021-02-05)

### Added

- ✨ Transfers routines as well! [[fbaa262](https://github.com/SturmB/sky-devops/commit/fbaa262fab9ed83d963c6674c1683381673bd51c)]


<a name="1.3.0"></a>
## 1.3.0 (2021-02-05)

### Changed

- ♻️ Makes database handling much more portable and modular [[43b9bf5](https://github.com/SturmB/sky-devops/commit/43b9bf5acc3a0cc34fc10fc1e2e415c681488322)]

### Removed

- 🔥 Removes seemingly unnecessary docker-compose file [[e300f29](https://github.com/SturmB/sky-devops/commit/e300f294a51625c3c1d445520992e556844378ed)]


<a name="1.2.0"></a>
## 1.2.0 (2021-02-04)

### Changed

- ♻️ Vastly cleans up the db get/put functions [[24d255a](https://github.com/SturmB/sky-devops/commit/24d255a86214b0301dcf9d7b78c54603bec7ef9d)]


<a name="1.1.1"></a>
## 1.1.1 (2021-02-04)

### Added

- ✨ Dumps local db data and imports it to the host [[f15153f](https://github.com/SturmB/sky-devops/commit/f15153ff0e5cc848c97b34aeebf49cbce170ed5b)]
- ✨ Adds other MySQL users to db container [[95ba319](https://github.com/SturmB/sky-devops/commit/95ba319b7ac0a810b937899bbc566456f717377f)]
- ✨ Adds dump playbook for ACS and AYS database [[cdcf8eb](https://github.com/SturmB/sky-devops/commit/cdcf8eb68ec87f3a1bdf38156661f8fb745e6277)]

### Changed

- ♻️ Uses correct variable names [[4524687](https://github.com/SturmB/sky-devops/commit/45246878ca4a98ad908db31e864e5a834cf04c69)]

### Removed

- 🔥 Remove the MySQL configuration file (no more logging general queries) [[30a4cbb](https://github.com/SturmB/sky-devops/commit/30a4cbb460ca54a9c1ba0310f5d8c630903fc374)]

### Fixed

- 🐛 Adds db setup to the dumping playbook [[ac010c8](https://github.com/SturmB/sky-devops/commit/ac010c8fc2c94b32e6e8509f35bcbdba357f9e90)]
- 🐛 Fixes variable name in the docker `.env` template [[5401e25](https://github.com/SturmB/sky-devops/commit/5401e25623a6a696d19f5e231c0a30893c29a988)]

### Miscellaneous

- ⚗️ Disable pre-populating the schedule db, too [[81573e0](https://github.com/SturmB/sky-devops/commit/81573e0be9c5d701e058061078f56e6556d93914)]
- ⚗️ Test 'dbinit' when dbms isn't pre-populated [[92995d4](https://github.com/SturmB/sky-devops/commit/92995d4473dc12e3463e3358300b510d89fcc529)]
- 🩹 Minor adjustments to clean up code [[a3b27f2](https://github.com/SturmB/sky-devops/commit/a3b27f27b4956ba364d826316be270e33203a826)]
- 🚧 Fixes connecting to container db and adding `skyadmin` user [[6eed672](https://github.com/SturmB/sky-devops/commit/6eed672f8299f80be57f1f707677a8df411edd23)]
- 🚧 Attempting to automate initializing the ACS db in a container [[8595758](https://github.com/SturmB/sky-devops/commit/85957587c05535a4638d8d6a1d6522aa94237a50)]


<a name="1.1.0"></a>
## 1.1.0 (2021-01-27)

### Added

- ✨ Adds redis service to docker-compose template [[93c02d9](https://github.com/SturmB/sky-devops/commit/93c02d99236542630847e768223de9f206c59b40)]
- ✨ Adds the `mysqldump` feature for Sky Schedule [[d836edf](https://github.com/SturmB/sky-devops/commit/d836edf6cc4bd37281b8d6f738f28c5e0ab460a6)]

### Changed

- ♻️ Adds new variable for pulling docker images [[ab8720f](https://github.com/SturmB/sky-devops/commit/ab8720f2ff100132c29ea24d0cd4d87fe7d20ce6)]
- 👽 Uses latest SHA (59440291) [[ba52bc9](https://github.com/SturmB/sky-devops/commit/ba52bc9aa4affb4606853df69fa21bdb4adb086f)]
- 🔧 Updates Ansible Lint for the GitHub Action [[b079a5b](https://github.com/SturmB/sky-devops/commit/b079a5bce6bb1cffae72a3afcd325fc8f6d39797)]
- 🏗️ Fixes staging playbooks to be more stable and clean [[c2cb0be](https://github.com/SturmB/sky-devops/commit/c2cb0bece96ad9e1dd4836ba82ad403c658111dd)]

### Removed

- 🔥 Removes arguments from ansible-lint action [[6dfd714](https://github.com/SturmB/sky-devops/commit/6dfd7145eb9f1ccc667446e9ac6089e78446477a)]

### Fixed

- 🐛 Fixes incorrect indention [[aa5ecbd](https://github.com/SturmB/sky-devops/commit/aa5ecbdaf55cc15f9cfd79922990b2e1111260ae)]

### Miscellaneous

- 📦 Adds redis container for Sky Schedule [[ddb19e7](https://github.com/SturmB/sky-devops/commit/ddb19e7f1acef3148e3e39a4a93c89843fc16b5e)]
- 🩹 Adds `--opt` during dumping just to be safe [[4bb410a](https://github.com/SturmB/sky-devops/commit/4bb410a910eff703b252131b6b566894a302bec8)]
- 🚧 Copying Sky Schedule data to local [[b3c1f0e](https://github.com/SturmB/sky-devops/commit/b3c1f0e8e0d08e46d4f948cc9f93e2a120fd492b)]
- ⚗️ Trying the `targets` parameter [[cac7b43](https://github.com/SturmB/sky-devops/commit/cac7b433e4f26a4b844a605ba2a4d740535b5af2)]
- 🔨 Adds arguments to ansible-lint action [[ee84830](https://github.com/SturmB/sky-devops/commit/ee84830615f6c6c3f6895984ec0369cb05e061d7)]
- 🔨 Adds Ansible Lint configuration [[c672690](https://github.com/SturmB/sky-devops/commit/c672690b4abad339082a81b583d9253b612bed96)]


<a name="1.0.0"></a>
## 1.0.0 (2020-11-23)

### Added

- ✨ Adds playbook for updating packages and rebooting [[b85c88a](https://github.com/SturmB/sky-devops/commit/b85c88a75eaf52ee6ca24ce359036b5632c6e0dd)]
- ✨ Prunes dangling images in AA [[c6d2173](https://github.com/SturmB/sky-devops/commit/c6d21733751fe7c1002f0dafb1d2b16e50ff33af)]
- ✨ Continues getting American Accents working [[7b01d3a](https://github.com/SturmB/sky-devops/commit/7b01d3ac3ff0e9dadff5176ab63af43d80ad72e5)]
- ✨ Adds American Accents [[8a9dc6a](https://github.com/SturmB/sky-devops/commit/8a9dc6a803eac7570afdd88732fa85f8cd26c204)]

### Changed

- 🚚 Gives the package updater playbook a better name [[057fa9f](https://github.com/SturmB/sky-devops/commit/057fa9f3a7223b5aef8b544d5056715de19dfef2)]
- ♻️ Separates provisioning from preparing [[266073f](https://github.com/SturmB/sky-devops/commit/266073ff21ff9026434867b9b224cefac8974661)]
- 👽 Updates task modules to use the FQCN [[b6e7d5e](https://github.com/SturmB/sky-devops/commit/b6e7d5e415d71102f39777e7a9832b31e7d83a2a)]

### Removed

- 🔥 Removes the "ansible-lint" GitHub action [[9c65a5f](https://github.com/SturmB/sky-devops/commit/9c65a5f8dca6880f48b6f89710694e1d75a4bfb6)]

### Fixed

- 🐛 Pulls the latest AA image before creating its container [[434f7d1](https://github.com/SturmB/sky-devops/commit/434f7d1e77f2c633561b0d713e2d98e44493bbb2)]

### Miscellaneous

- 📝 Adds instructions for `update-packages.yml` [[3887cb9](https://github.com/SturmB/sky-devops/commit/3887cb9dacbdcc9f5ad1c6321fc40abfbe2377ff)]
- 📝 Adds **American Accents** info to `README.md` [[d0503d7](https://github.com/SturmB/sky-devops/commit/d0503d76260103dd90261f67c77aacaffb1e3ad9)]
- 🛂 Fixes user creation not being idempotent [[4d2c55a](https://github.com/SturmB/sky-devops/commit/4d2c55ae3f2964f31b1428c98fc578ef1103e8dc)]
- Badges and CI [[7374f34](https://github.com/SturmB/sky-devops/commit/7374f3488db4da579818108fc47efa50deb78b1f)]
- Merge branch 'master' of github.com:SturmB/sky-devops [[9126c85](https://github.com/SturmB/sky-devops/commit/9126c85e6fc030349586279c5a46e8436acd385e)]
- Create ansible-lint.yml [[9900d82](https://github.com/SturmB/sky-devops/commit/9900d82c0d9c25f1c87cd34bcd526d67fa9db839)]
- Pre-Commit [[8277c15](https://github.com/SturmB/sky-devops/commit/8277c1566e633d9a8b49b36fa01907d47a9b0951)]
- Ansible-Lint [[6f7351e](https://github.com/SturmB/sky-devops/commit/6f7351eb440e14ec09a5a21ae8f665a5b61eca28)]
- Big Readme [[ee330aa](https://github.com/SturmB/sky-devops/commit/ee330aa10b48a173442db8c74720f1f8a30c4648)]
- Inventory fix [[345e1bd](https://github.com/SturmB/sky-devops/commit/345e1bd2ee4964bf6d4fbaada9f540776cdeb808)]
- Restart Apache [[3739dbf](https://github.com/SturmB/sky-devops/commit/3739dbf555e2938df976883cfb7d2a68ad135692)]
- Redmine Testing [[45a8c60](https://github.com/SturmB/sky-devops/commit/45a8c604c43aa21e9dc28d36e3063021ee1fb801)]
- Initial Pass [[3201983](https://github.com/SturmB/sky-devops/commit/3201983d7eab17879b39257888cc3ce3bf58c641)]
- env fix [[6c41359](https://github.com/SturmB/sky-devops/commit/6c41359d0c51b59c12f18bc54f1cc472e498937e)]
- ACS tag [[ee14d48](https://github.com/SturmB/sky-devops/commit/ee14d485d839d1622a5a51d19c09092531490176)]
- ACS [[647ed1f](https://github.com/SturmB/sky-devops/commit/647ed1f33d25252a7d51fa71d3dbdcec53ac8202)]
- www-data [[979ce4a](https://github.com/SturmB/sky-devops/commit/979ce4a772e4cd64da3e8b8ed84fe770cc1ed931)]
- NPM [[a137f81](https://github.com/SturmB/sky-devops/commit/a137f8119031039f58097b34f78a6dc164438008)]
- Restart Apache Handler [[0f83529](https://github.com/SturmB/sky-devops/commit/0f835299d2e461d31c6f90b80ed0cfd93807c317)]
- Whitespace [[3daba1a](https://github.com/SturmB/sky-devops/commit/3daba1a41083191b4dd410882dcfe596cb133d1a)]
- Zip [[c108448](https://github.com/SturmB/sky-devops/commit/c108448df794c6f084a2e069c0f2f0a1bf74bcf5)]
- php-mbstring [[4058714](https://github.com/SturmB/sky-devops/commit/40587148d9585eed5a110a62be7a86c9b56c3bd0)]
- Laravel [[cff6934](https://github.com/SturmB/sky-devops/commit/cff6934191fe57bd8fd58ee626eae749b7504402)]
- cupnapkin & sky [[ad7c03f](https://github.com/SturmB/sky-devops/commit/ad7c03f6ec944460d0c900faaa332b2d70631b2a)]
- RewriteEngine On [[4339906](https://github.com/SturmB/sky-devops/commit/4339906d577e9e82236c978aa1d71db575f35d67)]
- IPv6 [[62bf5e5](https://github.com/SturmB/sky-devops/commit/62bf5e596c3c8f5e8bc38c3a868ebc8d1f6b874a)]
- Structure Set [[6d89b08](https://github.com/SturmB/sky-devops/commit/6d89b08c87265e4b8df520a66c2cf070a8f351bf)]
- Redmine Email [[a31fb48](https://github.com/SturmB/sky-devops/commit/a31fb48284b6cdc5d39f9ab71f8abc84e38e258c)]
- Redmine [[54808e8](https://github.com/SturmB/sky-devops/commit/54808e82f904d104a00eabd35dc0ded2ce18f46f)]
- do_abl added [[03b5d6f](https://github.com/SturmB/sky-devops/commit/03b5d6f4c2ad908531b4103a867d3eb77ab2f00e)]
- Template Corrections [[ba6f029](https://github.com/SturmB/sky-devops/commit/ba6f0293e0f1aa1245b8c24edb6787176b09b623)]
- Vars [[309d8da](https://github.com/SturmB/sky-devops/commit/309d8daee7baf664a968f1780d730092ce0ace03)]
- Templating [[173f079](https://github.com/SturmB/sky-devops/commit/173f079a88223057792c87fafabf3b6980d44dff)]
- Vault [[2f24a6f](https://github.com/SturmB/sky-devops/commit/2f24a6f245be7e4b2ffd4e4429e7e31f0d7a743f)]
- Schedule + Webservers [[3245353](https://github.com/SturmB/sky-devops/commit/3245353a72d6820e7d45c7ae9089245b390d0acb)]
- ACS & AYS [[c48e03e](https://github.com/SturmB/sky-devops/commit/c48e03eb5a80f66b21e23544549e1d7eb49580f7)]
- Docker Compose [[58d3770](https://github.com/SturmB/sky-devops/commit/58d37702ebd4146dd088f8c572367aa831de0eef)]
- Schedule [[4350486](https://github.com/SturmB/sky-devops/commit/4350486697e8b0548e8dc230b7194713118c9974)]
- HAProxy [[57c8803](https://github.com/SturmB/sky-devops/commit/57c88034a605344b79dbf050661669619001d0e0)]
- ACS & AYS Working [[9c064b3](https://github.com/SturmB/sky-devops/commit/9c064b3a8aa3e14a517a794e43be85e6bfabf247)]
- first commit [[a18d4bc](https://github.com/SturmB/sky-devops/commit/a18d4bc5e49ff1eba412b3bc59b62e8c6c7f6935)]
