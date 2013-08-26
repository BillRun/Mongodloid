Mongodloid
==========

Mongo DB PHP Layer used by BillRun

http://billrun.net

Auto-Increment
==========
The library support auto increment feature which is useful on sharded environment. Please check Entity->createAutoInc and Collection->createAutoInc methods.
The dependency for this feature is to create the next collection with the unique indexes:
db.createCollection('counters');
db.counters.ensureIndex({coll: 1, seq: 1}, { unique: true, sparse: false, background: true});
db.counters.ensureIndex({coll: 1, oid: 1}, { unique: true, sparse: false, background: true});

LICENSE
=======
GPL-v2 and above
