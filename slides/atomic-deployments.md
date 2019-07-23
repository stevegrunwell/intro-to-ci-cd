### Atomic Deployments

<dl>
    <div class="fragment">
        <dt>releases/</dt>
        <dd>Contains multiple, timestamped deployments</dd>
    </div>
    <div class="fragment">
        <dt>shared/</dt>
        <dd>Data that should persist between deployments</dd>
    </div>
    <div class="fragment">
        <dt>current</dt>
        <dd>Symlink to the current release in <code>releases/</code></dd>
    </div>
</dl>

Note:

I learned from Capistrano in the Ruby community.

General idea is zero-downtime deployments by keeping multiple copies of the app on the server in the releases directory.

Common elements — configuration, logs, user uploads, etc. — will live in a shared directory, and those things will be symlinked in.

When we make a release, we'll update the `current` symlink to point to the new release. This symlink is treated as our web root.
