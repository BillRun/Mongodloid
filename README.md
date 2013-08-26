Mongodloid
==========

Mongo DB PHP Layer used by BillRun

http://billrun.net

Auto-Increment
==========
The library support auto increment feature which is useful on sharded environment. 

Please check createAutoInc method in Entity and Collection classes for simple usage.

The dependency for this feature is to create the next collection with the unique indexes:<br />
<code>db.createCollection('counters');<br />
db.counters.ensureIndex({coll: 1, seq: 1}, { unique: true, sparse: false, background: true});<br />
db.counters.ensureIndex({coll: 1, oid: 1}, { unique: true, sparse: false, background: true});
</code>

LICENSE
=======
GPL-v2 and above
