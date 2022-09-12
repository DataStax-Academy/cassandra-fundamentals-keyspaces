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
 <a href='command:katapod.loadPage?[{"step":"intro"}]'
   class="btn btn-dark navigation-top-left">⬅️ Back
 </a>
<span class="step-count"> Step 1 of 7</span>
 <a href='command:katapod.loadPage?[{"step":"step2"}]' 
    class="btn btn-dark navigation-top-right">Next ➡️
  </a>
</div>

<!-- CONTENT -->

<div class="step-title">Keyspace</div>

A *keyspace* is a namespace for a set of tables sharing a data replication strategy and some options. 
It is conceptually similar to a "database" in a relational database management system. 
Tables, materialized views, indexes and other schema objects are always defined within a keyspace.

To create a keyspace, Cassandra Query Language has the `CREATE KEYSPACE` statement with the following simplified syntax:

<pre class="non-executable-code">
CREATE KEYSPACE [ IF NOT EXISTS ] keyspace_name
    WITH REPLICATION = { replication_map };
</pre>

A *keyspace name* can contain alphanumeric characters and underscores. 
By default, names are case-insensitive, but case sensitivity can be forced by using double quotation marks around a name.

A *replication map* specifies a data replication strategy and replication factors. 
`SimpleStrategy` and `NetworkTopologyStrategy` are two available choices for prototyping/learning and production, respectively.

<!-- NAVIGATION -->
<div id="navigation-bottom" class="navigation-bottom">
 <a href='command:katapod.loadPage?[{"step":"intro"}]'
   class="btn btn-dark navigation-bottom-left">⬅️ Back
 </a>
 <a href='command:katapod.loadPage?[{"step":"step2"}]'
    class="btn btn-dark navigation-bottom-right">Next ➡️
  </a>
</div>
