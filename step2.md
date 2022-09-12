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
 <a href='command:katapod.loadPage?[{"step":"step1"}]'
   class="btn btn-dark navigation-top-left">⬅️ Back
 </a>
<span class="step-count"> Step 2 of 7</span>
 <a href='command:katapod.loadPage?[{"step":"step3"}]' 
    class="btn btn-dark navigation-top-right">Next ➡️
  </a>
</div>

<!-- CONTENT -->

<div class="step-title">Cluster, datacenters, racks, nodes</div>

✅ Use `nodetool` to gather information about the cluster:

```
docker exec -i -t Cassandra-1 bash -c 'nodetool status'
```

If the cluster only has one node in datacenter `DC-West`, **wait for the second node in datacenter `DC-East` to join** and run `nodetool status` again. The output should be similar to:

<pre class = >
Datacenter: DC-East
===================
Status=Up/Down
|/ State=Normal/Leaving/Joining/Moving
--  Address     Load       Tokens  Owns (effective)  Host ID                               Rack 
UN  172.17.0.3  38.05 KiB  16      100.0%            e5eb2dda-ed95-4081-9f45-f3903cd21a23  rack1

Datacenter: DC-West
===================
Status=Up/Down
|/ State=Normal/Leaving/Joining/Moving
--  Address     Load       Tokens  Owns (effective)  Host ID                               Rack 
UN  172.17.0.2  74.12 KiB  16      100.0%            bc1c6aa2-b3fd-45a6-8e62-db4d420fbfdc  rack1
</pre>


Take a note of the datacenter names and how many nodes are in each datacenter. 
Since the cluster has only two nodes, we can have at most two replicas. 
In a real-life production cluster, you can usually expect to have 3 or more nodes per datacenter and replication factors of 3 or higher.


<!-- NAVIGATION -->
<div id="navigation-bottom" class="navigation-bottom">
 <a href='command:katapod.loadPage?[{"step":"step1"}]'
   class="btn btn-dark navigation-bottom-left">⬅️ Back
 </a>
 <a href='command:katapod.loadPage?[{"step":"step3"}]'
    class="btn btn-dark navigation-bottom-right">Next ➡️
  </a>
</div>
