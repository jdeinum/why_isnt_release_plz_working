# Not Working Report

I was being dumb, it was right in the docs:

```
The publish field

Publish to cargo registry.

If true, release-plz runs cargo publish. (Default). If false, release-plz
doesn't run cargo publish.

With this option disabled, release-plz will continue creating git tags. However,
note that release-plz will still use the cargo registry to check what's the
latest release, so you still need to run cargo publish by yourself.
```

I was expecting that if publish = false, that we could use the git history to
actually determine the latest version, and what commit it corresponded to so
that we can check commits since that moment. At that point you can get a tag
you're working off of (i.e v0.1.1) and a series of commits which you use to
determine the next semantic versioned tag for the project.

Will see if I can make a PR for this.
