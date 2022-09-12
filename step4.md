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
 <a href='command:katapod.loadPage?[{"step":"step3"}]'
   class="btn btn-dark navigation-top-left">⬅️ Back
 </a>
<span class="step-count"> Step 4 of 7</span>
 <a href='command:katapod.loadPage?[{"step":"step5"}]' 
    class="btn btn-dark navigation-top-right">Next ➡️
  </a>
</div>

<!-- CONTENT -->

<div class="step-title">Keyspaces with SimpleStrategy</div>

✅ Create a keyspace with name `simple_keyspace_1` that uses `SimpleStrategy` and a replication factor of `1`:

```
CREATE KEYSPACE simple_keyspace_1
WITH replication = {'class': 'SimpleStrategy', 
                    'replication_factor': 1};
```

The `replication_factor` option specifies a replication factor for the entire cluster. 
That means that `SimpleStrategy` does not respect datacenter layouts and, therefore, is not a good choice 
for production. 


✅ Create a keyspace with name `simple_keyspace_2` that uses `SimpleStrategy` and a replication factor of `2`.
Use tab completion in `cqlsh` to your advantage.

<details>
  <summary>Solution</summary>

```
CREATE KEYSPACE simple_keyspace_2
WITH replication = {'class': 'SimpleStrategy', 
                    'replication_factor': 2};
```

</details>

<!-- NAVIGATION -->
<div id="navigation-bottom" class="navigation-bottom">
 <a href='command:katapod.loadPage?[{"step":"step3"}]'
   class="btn btn-dark navigation-bottom-left">⬅️ Back
 </a>
 <a href='command:katapod.loadPage?[{"step":"step5"}]'
    class="btn btn-dark navigation-bottom-right">Next ➡️
  </a>
</div>

