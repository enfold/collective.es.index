Changelog
=========

1.0a2 (unreleased)
------------------

- Move to elasticsearch_dsl package for query generation

- Add celery support (requires latest collective.celery) tested with celery>=4.2.0

- Add new directives: max_blobsize, request_timeout, use_celery, indexed_chars

- No longer keeps the b64 encoded blob in ES index

- Add highlight support on search results

- basic plone 4 compatibility

- refactor code to avoid sending obj data in redis payload

- add stopgap solution for missing rid problem

- add a more detailed comment for code that skips highlights with no rid

- avoid generating index data twice for celery indexing, use relative path from root

- Retry on POSKeyError when using celery

- #2610885: Sleep for a few seconds in index task because retry isn't working
  with collective.celery tasks.
  [JL 2019-02-28]

- #2610885: Move sleep to before call to get_payload.
  [JL 2019-02-28]


1.0a1 (git tag)
---------------

- Initial release.
  [jensens]
