<!-- TOP -->
<div class="top">
  <img src="https://datastax-academy.github.io/katapod-shared-assets/images/ds-academy-logo.svg" />
  <div class="scenario-title-section">
    <span class="scenario-title">Apache Cassandra® Keyspaces and Data Replication Strategies</span>
    <span class="scenario-subtitle">ℹ️ For technical support, please contact us via <a href="mailto:aleksandr.volochnev@datastax.com">email</a> or <a href="https://dtsx.io/aleks">LinkedIn</a>.</span> 
  </div>
</div>

<!-- NAVIGATION -->
<div id="navigation-top" class="navigation-top">
 <a href='command:katapod.loadPage?[{"step":"step2"}]' 
   class="btn btn-dark navigation-top-left">⬅️ Back
 </a>
<span class="step-count"> Step 3 of 7</span>
 <a href='command:katapod.loadPage?[{"step":"step4"}]' 
    class="btn btn-dark navigation-top-right">Next ➡️
  </a>
</div>

<!-- CONTENT -->

<div class="step-title">Create a keyspace</div>

A keyspace is a namespace for a set of tables sharing a data replication strategy and some options. 
It is conceptually similar to a "database" in a relational database management system.

✅ Create the keyspace:
```
CREATE KEYSPACE killr_video
WITH replication = {
  'class': 'NetworkTopologyStrategy', 
  'DC-Houston': 1 }; 
```

Our keyspace name is `killr_video`. Any data in this keyspace will be replicated to datacenter `DC-Houston` 
using replication strategy `NetworkTopologyStrategy` and replication factor `1`. In production, however, we strongly 
recommend multiple datacenters and at least three replicas per datacenter for higher availability.

<!-- NAVIGATION -->
<div id="navigation-bottom" class="navigation-bottom">
 <a href='command:katapod.loadPage?[{"step":"step2"}]'
   class="btn btn-dark navigation-bottom-left">⬅️ Back
 </a>
 <a href='command:katapod.loadPage?[{"step":"step4"}]'
    class="btn btn-dark navigation-bottom-right">Next ➡️
  </a>
</div>
