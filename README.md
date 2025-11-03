# kanopi/templr Homebrew Formula

This formula can build the templr package from source or pull from bottles.

This repo is automatically updated by goreleaser in github.com/kanopi/templr. It does not need to be manually fixed.

Updating (manual, obsolete):

* Add the url and sha256 of the new release source-code tarball to the homebrew-templr local version.
* Create new bottles on linux and macOS (before pushing new formula:
```
   brew uninstall templr
   cd homebrew-templr  # directory with new source
   brew install --build-from-source Formula/templr.rb
   brew uninstall templr
   brew install --build-bottle Formula/templr.rb
   brew bottle --force-core-tap Formula/templr.rb
```
* Add the bottles into the formula per the output of `brew bottle` above. 
* Add the bottles to the github release.
* Create the PR for the new homebrew version.

I'm quite sure we'll automate most of this, but this is the documented process at this time.

You should be able to build from source any time using `brew reinstall --build-from-source templr`
