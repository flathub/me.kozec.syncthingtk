Updating
-----------

To update syncthing, it has proven useful to
  a) comment generated-sources.json
  b) enable network for the build
  c) run flatpak-builder
  d) run the go-vendor generator, e.g.
     python3 ~/vcs/flatpak-builder-tools/go-get/flatpak-go-vendor-generator.py  .flatpak-builder/build//syncthing/vendor/modules.txt > generated-sources.json
  e) undo a) and b)
