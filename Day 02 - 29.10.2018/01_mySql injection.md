<table border="1">
<tbody>
<tr>
<td>Version</td>
<td>


```sql
SELECT @@version
```

</td>
</tr>
<tr>
<td>Comments</td>
<td>


```sql
SELECT 1; #comment
SELECT /*comment*/1;
```

</td>
</tr>
<tr>
<td>Current User</td>
<td>


```sql
SELECT user();
SELECT system_user();
```

</td>
</tr>
<tr>
<td>List Users</td>
<td>

```sql
SELECT user FROM mysql.user;
```

</td>
</tr>
<tr>
<td>List Host info</td>
<td>

```sql
SELECT host, user, password FROM mysql.user;
```
</td>
</tr>
<tr>
<td>List Privileges</td>
<td>

```sql
SELECT grantee, privilege_type, is_grantable 
FROM information_schema.user_privileges; -- list user privs


SELECT host, user, Select_priv, Insert_priv, 
Update_priv, Delete_priv, Create_priv, Drop_priv, 
Reload_priv, Shutdown_priv, Process_priv, File_priv, Grant_priv, 
References_priv, Index_priv, Alter_priv, Show_db_priv, Super_priv, 
Create_tmp_table_priv, Lock_tables_priv, 
Execute_priv, Repl_slave_priv, Repl_client_priv 
FROM mysql.user;

 
SELECT grantee, table_schema, privilege_type 
FROM information_schema.schema_privileges;


SELECT table_schema, table_name, column_name, privilege_type 
FROM information_schema.column_privileges; -- list privs on columns
```

</td>
</tr>
<tr>
<td>List DBA Accounts</td>
<td>

```sql
SELECT grantee, privilege_type, is_grantable 
FROM information_schema.user_privileges 
WHERE privilege_type = 'SUPER';

SELECT host, user 
FROM mysql.user WHERE Super_priv = 'Y'; 
```

</td>
</tr>
<tr>
<td>Current Database</td>
<td>

```sql
SELECT database()
```

</td>
</tr>
<tr>
<td>List Databases</td>
<td>

```sql
SELECT schema_name FROM information_schema.schemata;
```

</td>
</tr>
<tr>
<td>List Columns</td>
<td>

```sql
SELECT table_schema, table_name, column_name 
FROM information_schema.columns 
WHERE table_schema != 'mysql'
AND table_schema != 'information_schema'
```

</td>
</tr>
<tr>
<td>List Tables</td>
<td>

```sql
SELECT table_schema,table_name 
FROM information_schema.tables 
WHERE table_schema != 'mysql' 
AND table_schema != 'information_schema'
```

</td>
</tr>
<tr>
<td>Find Tables From Column Name</td>
<td>

```sql
SELECT table_schema, table_name 
FROM information_schema.columns WHERE column_name = 'username'; 
# find table which have a column called ‘username’
```

</td>
</tr>

<tr>
<td>Select Nth Char</td>
<td>

```sql
SELECT substr('abcd', 3, 1); # returns c
```

</td>
</tr>
<tr>
<td>Bitwise AND</td>
<td>

```sql
SELECT 6 & 2; # returns 2
SELECT 6 & 1; # returns 0
```

</td>
</tr>
<tr>
<td>ASCII Value to Char</td>
<td>


```sql
SELECT char(65); # returns A
```

</td>
</tr>
<tr>
<td>Char to ASCII Value</td>
<td>

```sql
SELECT ascii('A'); # returns 65
```

</td>
</tr>
<tr>
<td>Casting</td>
<td>

```sql
SELECT cast('1' AS unsigned integer);<br>
SELECT cast('123' AS char);
```

</td>
</tr>
<tr>
<td>String Concatenation</td>
<td>


```sql
SELECT CONCAT('A','B'); #returns AB<br>
SELECT CONCAT('A','B','C'); # returns ABC
```

</td>
</tr>
<tr>
<td>If Statement</td>
<td>

```sql
SELECT if(1=1,'foo','bar'); # returns ‘foo’
```

</td>
</tr>
<tr>
<td>Case Statement</td>

```sql
SELECT CASE WHEN (1=1) THEN 'A' ELSE 'B' END; # returns A
```

</tr>

<tr>
<td>Time Delay</td>
<td>

```sql
SELECT SLEEP(5);
```

</td>
</tr>

<tr>
<td>Hostname, IP Address</td>
<td>

```sql
SELECT @@hostname;
```

</td>
</tr>
<tr>
<td>Create Users</td>
<td>

```sql
CREATE USER test1 IDENTIFIED BY 'pass1'; 
```

</td>
</tr>
<tr>
<td>Delete Users</td>
<td>

```sql
DROP USER test1; 
```

</td>
</tr>

<tr>
<td>Location of DB files</td>
<td>

```sql
SELECT @@datadir;
```

</td>
</tr>


</tbody>
</table>
