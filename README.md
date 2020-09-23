<div align="center">

## SQL Injections \- The final solution to


</div>

### Description

Stop SQL Injections
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[marcojetson](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/marcojetson.md)
**Level**          |Beginner
**User Rating**    |5.0 (25 globes from 5 users)
**Compatibility**  |PHP 4\.0, PHP 5\.0
**Category**       |[Security](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/security__8-14.md)
**World**          |[PHP](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/php.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/marcojetson-sql-injections-the-final-solution-to__8-2576/archive/master.zip)





### Source Code

Here is a simple, yet effective, solution for avoiding SQL Injections.<br><br>
Let's see a SQL Injection vulnerable sentence:<br>
$r = mysql_query("SELECT * FROM s WHERE id = ".$_GET['id']."");<br><br>
And the solution:<br>
$r = mysql_query("SELECT * FROM s WHERE id = UNHEX('".bin2hex($_GET['id'])."')");<br><br>
By converting the var in php, and reconverting it in the SQL sentence there's no chance to inject code.<br><br><br>
tehwebmaster.blogspot.com / logikk.com.ar

