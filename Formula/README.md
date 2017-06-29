Homebrew installer for Mac OS X

To test locally, first fork the github.com/hyperledger/homebrew-fabric
repository to your personal GitHub account. Then, clone your fork to your
laptop/workstation. Checkout the Gerrit CR for the change to be tested and
apply to your local clone. Then push the changes to your personal fork.

e.g. following the fork step:

```bash
git clone git@github.com:<your-github-id>/homebrew-fabric.git
cd homebrew-fabric
git fetch ssh://<your-lf-id>s@gerrit.hyperledger.org:29418/homebrew-fabric refs/changes/41/11241/5 && git checkout FETCH_HEAD
git push origin HEAD:master
```

**Note:** you may also use the GitHub desktop client to clone and push.

If you have previously installed the Hyperledger Fabric tap,
you should first uninstall it to test an update.

```bash
brew untap hyperledger/fabric
```

The next step, you can install **your** tap with the following:

```bash
brew tap <your-github-id>/homebrew-fabric
```

Now that you have the tap based on your personal fork installed, you can
test the command.

```bash
brew install fabric-tools
```

Then, check to see whether the binaries have been properly installed:

```bash
which cryptogen
which configtxgen
which configtxlator
```

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.
