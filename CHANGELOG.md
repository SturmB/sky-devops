# Changelog

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
-  Badges and CI [[7374f34](https://github.com/SturmB/sky-devops/commit/7374f3488db4da579818108fc47efa50deb78b1f)]
-  Merge branch 'master' of github.com:SturmB/sky-devops [[9126c85](https://github.com/SturmB/sky-devops/commit/9126c85e6fc030349586279c5a46e8436acd385e)]
-  Create ansible-lint.yml [[9900d82](https://github.com/SturmB/sky-devops/commit/9900d82c0d9c25f1c87cd34bcd526d67fa9db839)]
-  Pre-Commit [[8277c15](https://github.com/SturmB/sky-devops/commit/8277c1566e633d9a8b49b36fa01907d47a9b0951)]
-  Ansible-Lint [[6f7351e](https://github.com/SturmB/sky-devops/commit/6f7351eb440e14ec09a5a21ae8f665a5b61eca28)]
-  Big Readme [[ee330aa](https://github.com/SturmB/sky-devops/commit/ee330aa10b48a173442db8c74720f1f8a30c4648)]
-  Inventory fix [[345e1bd](https://github.com/SturmB/sky-devops/commit/345e1bd2ee4964bf6d4fbaada9f540776cdeb808)]
-  Restart Apache [[3739dbf](https://github.com/SturmB/sky-devops/commit/3739dbf555e2938df976883cfb7d2a68ad135692)]
-  Redmine Testing [[45a8c60](https://github.com/SturmB/sky-devops/commit/45a8c604c43aa21e9dc28d36e3063021ee1fb801)]
-  Initial Pass [[3201983](https://github.com/SturmB/sky-devops/commit/3201983d7eab17879b39257888cc3ce3bf58c641)]
-  env fix [[6c41359](https://github.com/SturmB/sky-devops/commit/6c41359d0c51b59c12f18bc54f1cc472e498937e)]
-  ACS tag [[ee14d48](https://github.com/SturmB/sky-devops/commit/ee14d485d839d1622a5a51d19c09092531490176)]
-  ACS [[647ed1f](https://github.com/SturmB/sky-devops/commit/647ed1f33d25252a7d51fa71d3dbdcec53ac8202)]
-  www-data [[979ce4a](https://github.com/SturmB/sky-devops/commit/979ce4a772e4cd64da3e8b8ed84fe770cc1ed931)]
-  NPM [[a137f81](https://github.com/SturmB/sky-devops/commit/a137f8119031039f58097b34f78a6dc164438008)]
-  Restart Apache Handler [[0f83529](https://github.com/SturmB/sky-devops/commit/0f835299d2e461d31c6f90b80ed0cfd93807c317)]
-  Whitespace [[3daba1a](https://github.com/SturmB/sky-devops/commit/3daba1a41083191b4dd410882dcfe596cb133d1a)]
-  Zip [[c108448](https://github.com/SturmB/sky-devops/commit/c108448df794c6f084a2e069c0f2f0a1bf74bcf5)]
-  php-mbstring [[4058714](https://github.com/SturmB/sky-devops/commit/40587148d9585eed5a110a62be7a86c9b56c3bd0)]
-  Laravel [[cff6934](https://github.com/SturmB/sky-devops/commit/cff6934191fe57bd8fd58ee626eae749b7504402)]
-  cupnapkin & sky [[ad7c03f](https://github.com/SturmB/sky-devops/commit/ad7c03f6ec944460d0c900faaa332b2d70631b2a)]
-  RewriteEngine On [[4339906](https://github.com/SturmB/sky-devops/commit/4339906d577e9e82236c978aa1d71db575f35d67)]
-  IPv6 [[62bf5e5](https://github.com/SturmB/sky-devops/commit/62bf5e596c3c8f5e8bc38c3a868ebc8d1f6b874a)]
-  Structure Set [[6d89b08](https://github.com/SturmB/sky-devops/commit/6d89b08c87265e4b8df520a66c2cf070a8f351bf)]
-  Redmine Email [[a31fb48](https://github.com/SturmB/sky-devops/commit/a31fb48284b6cdc5d39f9ab71f8abc84e38e258c)]
-  Redmine [[54808e8](https://github.com/SturmB/sky-devops/commit/54808e82f904d104a00eabd35dc0ded2ce18f46f)]
-  do_abl added [[03b5d6f](https://github.com/SturmB/sky-devops/commit/03b5d6f4c2ad908531b4103a867d3eb77ab2f00e)]
-  Template Corrections [[ba6f029](https://github.com/SturmB/sky-devops/commit/ba6f0293e0f1aa1245b8c24edb6787176b09b623)]
-  Vars [[309d8da](https://github.com/SturmB/sky-devops/commit/309d8daee7baf664a968f1780d730092ce0ace03)]
-  Templating [[173f079](https://github.com/SturmB/sky-devops/commit/173f079a88223057792c87fafabf3b6980d44dff)]
-  Vault [[2f24a6f](https://github.com/SturmB/sky-devops/commit/2f24a6f245be7e4b2ffd4e4429e7e31f0d7a743f)]
-  Schedule + Webservers [[3245353](https://github.com/SturmB/sky-devops/commit/3245353a72d6820e7d45c7ae9089245b390d0acb)]
-  ACS & AYS [[c48e03e](https://github.com/SturmB/sky-devops/commit/c48e03eb5a80f66b21e23544549e1d7eb49580f7)]
-  Docker Compose [[58d3770](https://github.com/SturmB/sky-devops/commit/58d37702ebd4146dd088f8c572367aa831de0eef)]
-  Schedule [[4350486](https://github.com/SturmB/sky-devops/commit/4350486697e8b0548e8dc230b7194713118c9974)]
-  HAProxy [[57c8803](https://github.com/SturmB/sky-devops/commit/57c88034a605344b79dbf050661669619001d0e0)]
-  ACS & AYS Working [[9c064b3](https://github.com/SturmB/sky-devops/commit/9c064b3a8aa3e14a517a794e43be85e6bfabf247)]
-  first commit [[a18d4bc](https://github.com/SturmB/sky-devops/commit/a18d4bc5e49ff1eba412b3bc59b62e8c6c7f6935)]
