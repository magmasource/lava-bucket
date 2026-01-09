# magmasource lava-bucket bucket for Scoop

<!-- Uncomment the following line after replacing placeholders -->
<!-- [![Tests](https://github.com/<username>/<bucketname>/actions/workflows/ci.yml/badge.svg)](https://github.com/<username>/<bucketname>/actions/workflows/ci.yml) [![Excavator](https://github.com/<username>/<bucketname>/actions/workflows/excavator.yml/badge.svg)](https://github.com/<username>/<bucketname>/actions/workflows/excavator.yml) -->

## What is Scoop and how do I install it?

Scoop is a Windows command-line installer.

Go to [scoop.sh](https://scoop.sh) snd follow the Quickstart instructions there.

## What do the manifests in lava-bucket do?

These manifests tell Scoop how to fetch and install pre-compiled alphaMELTS binaries (similar to the [magmasource/lava-spout](https://github.com/magmasource/homebrew-lava-spout/) Homebrew tap for macOS and Linux). Scoop will install Perl, if appropriate, make links and set the Path variable so that running the 'install.command' Perl script is not required.

At the moment the only manifest is 'alphamelts' for the standalone app. A 'libalphamelts' manifest to install the dynamically link library (.dll) needed by alphaMELTS for MATLAB/Python will be available in the next release.

## How do I install these manifests?

After Scoop has been installed/updated, run the following:

```pwsh
scoop bucket add lava-bucket https://github.com/magmasource/lava-bucket
scoop install lava-bucket/<manifestname>
```

Substitute the manifest name (e.g. 'alphamelts') for '&lt;manifestname&gt;'.

## Scoop documentation

`scoop help`, [README](https://github.com/ScoopInstaller/Scoop#readme) or check [Scoop's Wiki](https://github.com/ScoopInstaller/Scoop/wiki).
