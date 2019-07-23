### A drop-dead simple deployment:

1. <!-- .element: class="fragment" --> Build the app
2. <!-- .element: class="fragment" --> `scp` a tarball to production
3. <!-- .element: class="fragment" --> `rsync` the files into the web root

Note:

Let's imagine a bare-bones deployment: we do anything necessary to build the app, then we need to get it to prod, right? Let's try scp ("secure copy") to copy it to prod.

Then, on prod, we'll unarchive the tarball and use rsync to copy any changed files.
