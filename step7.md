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
 <a href='command:katapod.loadPage?[{"step":"step6"}]'
   class="btn btn-dark navigation-top-left">⬅️ Back
 </a>
<span class="step-count"> Step 7 of 7</span>
 <a href='command:katapod.loadPage?[{"step":"finish"}]'
    class="btn btn-dark navigation-top-right">Next ➡️
  </a>
</div>

<!-- CONTENT -->

<div class="step-title">Working with keyspaces</div>

Try the following five CQL shell commands and CQL statements that are applicable to keyspaces. 

✅ List the names of all keyspaces in the cluster:
```
DESCRIBE KEYSPACES;
```

✅ Output all CQL statements that can be used to recreate the given keyspace
and all the schema objects that belong to it:
```
DESCRIBE KEYSPACE production_keyspace_2;
```

✅ Alter properties of the given keyspace:
```
ALTER KEYSPACE production_keyspace_2
WITH replication = 
     {'class': 'NetworkTopologyStrategy',
      'DC-West': 3, 'DC-East': 5};
```

✅ Set the given keyspace as the current working keyspace:
```
USE production_keyspace_2;
```

✅ Remove the given keyspace and all the objects that belong to it:
```
DROP KEYSPACE production_keyspace_1;
```

<!-- NAVIGATION -->
<div id="navigation-bottom" class="navigation-bottom">
 <a href='command:katapod.loadPage?[{"step":"step6"}]'
   class="btn btn-dark navigation-bottom-left">⬅️ Back
 </a>
 <a href='command:katapod.loadPage?[{"step":"finish"}]'
    class="btn btn-dark navigation-bottom-right">Next ➡️
  </a>
</div>

