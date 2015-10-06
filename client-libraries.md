# Onestop ID client libraries

<span style="color:red;">Migration Warning.</span> Throughout October 2015, we're moving feed and operator records from the [GitHub-based Feed Registry](https://github.com/transitland/transitland-feed-registry) into Transitland's [Datastore API](https://github.com/transitland/transitland-datastore/blob/master/README.md#api-endpoints). These client libraries will be updated after the migration is complete, but will be broken in the meantime. Thanks for your patience&mdash;and your interest in the Onestop ID scheme!

---

* [**transitland-(ruby)-client**](https://github.com/transitland/transitland-ruby-client)

* [**transitland-(python)-client**](https://github.com/transitland/transitland-python-client)

We welcome client libraries in new and different languages. Please [open an issue on this repository](https://github.com/transitland/onestop-id-scheme/issues/new) if you'd like to propose a new client.

## Environment Variables

When using existing client libraries (and writing future libraries), we suggest you use the following standard environment variables to share settings among interlocking modules:

environment variable name | default value | notes
------------------------- | ------------- | -----
`TRANSITLAND_FEED_REGISTRY_URL` | `https://github.com/transitland/transitland-feed-registry` | override if you need to work with a branch or a fork
`TRANSITLAND_FEED_REGISTRY_PATH` | `./tmp/transitland-feed-registry` | look here for a copy of the Feed Registry repo, before clone'ing a copy of the remote
`TRANSITLAND_DATASTORE_URL` | `http://datastore.transit.land/api/v1` | where to query for data or create changesets
`TRANSITLAND_DATASTORE_AUTH_TOKEN` | n/a | auth tokens are necessary to write to the Datastore (create a changeset or trigger a "feed eater" job)
