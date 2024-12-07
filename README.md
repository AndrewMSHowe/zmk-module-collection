# ZMK Module Collection

This repository is a proof of concept of a more official collection of modules as mentioned in [this PR](https://github.com/zmkfirmware/zmk/pull/2456).

The modules listed in this repository are **not** properly vetted, nor do they have any guarantees regarding things interacting nicely. 
They are also not bound to any particular version of ZMK. 

## Usage

To use this, add this module as a project to your `config/west.yml`:

```yaml
manifest:
  projects:
    - name: zmk-module-collection
      url: git@github.com:Nick-Munnich/zmk-module-collection.git
      revision: main
      import:
         name-allowlist: 
             - zmk-module-placeholder
```

Then you can add any modules you wish to include from this collection under the `name-allowlist` like so:

```yaml
manifest:
  projects:
    - name: zmk-module-collection
      url: git@github.com:Nick-Munnich/zmk-module-collection.git
      revision: main
      import:
         name-allowlist: 
             - zmk-keyboards-akohekohe
             - zmk-components-vik
             - zmk-behavior-tri-state
```

## Adding Additional Modules

Modules not listed in this collection can be added as usual. If you wish to add modules to this collection, you can either contact me about it, make an issue, or make a PR directly following the same format as existing modules.