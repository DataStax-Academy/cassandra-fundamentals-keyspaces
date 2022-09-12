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
 <a href='command:katapod.loadPage?[{"step":"step4"}]'
   class="btn btn-dark navigation-top-left">⬅️ Back
 </a>
<span class="step-count"> Step 5 of 7</span>
 <a href='command:katapod.loadPage?[{"step":"step6"}]'
    class="btn btn-dark navigation-top-right">Next ➡️
  </a>
</div>

<!-- CONTENT -->

<div class="step-title">Keyspaces with NetworkTopologyStrategy</div>

✅ Create a keyspace with name `production_keyspace_1` that uses `NetworkTopologyStrategy` and a replication factor of `1` for `DC-West`:

```
CREATE KEYSPACE production_keyspace_1
WITH replication = {'class': 'NetworkTopologyStrategy', 
                    'DC-West': 1};
```

With `NetworkTopologyStrategy`, a replication factor is specified for each datacenter separately. 
In the above example, the `DC-West` datacenter will have a single copy of data. 
Not replicating data to `DC-East` could be a valid use case but usually there will be replicas in each datacenter. 

✅ Create a keyspace with name `production_keyspace_2` that uses `NetworkTopologyStrategy` 
and `1` replica in each datacenter:

<details>
  <summary>Solution</summary>

```
CREATE KEYSPACE production_keyspace_2
WITH replication = {'class': 'NetworkTopologyStrategy', 
                    'DC-West': 1,
                    'DC-East': 1};
```

</details>

<!-- NAVIGATION -->
<div id="navigation-bottom" class="navigation-bottom">
 <a href='command:katapod.loadPage?[{"step":"step4"}]'
   class="btn btn-dark navigation-bottom-left">⬅️ Back
 </a>
 <a href='command:katapod.loadPage?[{"step":"step6"}]'
    class="btn btn-dark navigation-bottom-right">Next ➡️
  </a>
</div>

