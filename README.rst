Updating
-----------

To update syncthing, it has proven useful to update the tarball URL and hash
and then
  a) comment generated-sources.json in syncthing.yaml
  b) enable network for the build, i.e. uncomment the build-args
  c) run flatpak-builder, e.g.
     flatpak-builder --user  --ccache --keep-build-dirs  --force-clean -v  --repo=/tmp/fb.repo fpbuilder net.syncthing.syncthing.yaml
  d) run the go-vendor generator, e.g.
     python3 ~/vcs/flatpak-builder-tools/go-get/flatpak-go-vendor-generator.py  .flatpak-builder/build//syncthing/vendor/modules.txt > generated-sources.json
  e) undo a) and b)
