### What does our deployment process look like right now?

* <!-- .element: class="fragment" --> (S)FTP?
* <!-- .element: class="fragment" --> SSH + `git pull`?
* <!-- .element: class="fragment" --> Docker?

Note:

When you're moving towards continuous delivery, it's important to consider how you're deploying today.

Are you simply SFTP-ing files? SSH-ing into the target server(s) and running `git pull`? Are you compiling CSS and JavaScript there, too?

Maybe you're using Docker containers and better orchestration, but how are those containers being built?
