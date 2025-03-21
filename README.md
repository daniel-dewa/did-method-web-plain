# `did:well-known` Decentralized Identifiers Method Spec

This repository contains the `did:well-known` Decentralized Identifier Method
Specification. You can access the latest version of this specification here:

<https://github.com/daniel-dewa/did-method-well-known>

## TODO

1. Update spec in `index.html`.
2. Stabilize.
3. Implement.

## Inspired by `did:web`

A number of issues such as:

- Permitting did documents at arbitrary sub paths ([w3c-ccg/did-method-web#50](https://github.com/w3c-ccg/did-method-web/pull/50), [w3c-ccg/did-method-web#84](https://github.com/w3c-ccg/did-method-web/issues/84))
- Permitting off-domain redirects ([w3c-ccg/did-method-web#55](https://github.com/w3c-ccg/did-method-web/issues/55), [w3c-ccg/did-method-web#71](https://github.com/w3c-ccg/did-method-web/issues/71))

As well as adding:

- An (optional) insecure version to ease development <br />
  Permits specifying insecure `http`-scheme for use in testing / development: `did:well-known:http:...`

Compelled us to create `did:well-known`.

## Changes (compared to `did:web`)

- Revert to using `/.well-known/did.json` and `/.well-known/did.json/foo/bar`
- Insecure `did:well-known`s (optional) <br />
  `did:well-known:` **`http`** `:example.com` ->
  `http://example.com/.well-known/did.json`
- "KID" suffixes, e.g. `did:well-known:issuer.example.com:cambridge#kid-id-1` <br />
  Which resolves to -> `https://issuer.example.com/.well-known/did.json/cambridge`

## Implementations

- TODO

## Editing and building the specification

This specification uses [ReSpec](https://github.com/w3c/respec/) html. Just edit `index.html` and the draft will be rendered correctly.

When it's time to do a static snapshot, we use the ReSpec UI in the browser to export static HTML.

## Note re well-known

You do NOT need to register your instance of a `did:well-known` with IANA.  Please do NOT attempt to do so.  As things stabilize, the editors of this specification may register the file(s) of this specification with the well-known uris registry.  These registries are for the paths to files themselves that are specified, not for individual implementations.
