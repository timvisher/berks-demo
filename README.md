# vagrant without vagrant-berkshelf

`vagrant-berkshelf` has been deprecated. This is intended to be a very
minimal example of how to get along without it.

You write your custom cookbooks in `cookbooks`, add them to your local
`Berksfile` using `:path => …` entries, and then run `berks vendor`
whenever you need to provision your machine. The last step is safest if
you first delete the `berks-cookbooks` directory. Otherwise I've seen it
occassionaly recursively duplicate the tree each time which ends up using
quite a bit of disk space and causes the provision to take longer as the
directory takes longer and longer to mount.
