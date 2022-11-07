#### Parser Content
```Java
{
Name = mysql-m-sk4-database-query-success-message
    Vendor = Mysql
    Product = Mysql
    ParserVersion = v1.0.0
    TimeFormat = "yyyyMMdd HH:mm:ss"
    Conditions = [ """,QUERY,""", """"message"""", """"ttam_category":"database/mysql"""" ]
    Fields = [
      """message"+:"+[^,]*,({host}[^,]+)""",
      """message"+:"+({time}\d\d\d\d\d\d\d\d \d\d:\d\d:\d\d)""",
      """({app}mysql)""",
      """,QUERY,[^\}]+?(concat\([^\)]+\))?\s(?i)from\s+\`?({db_name}[^.,\`]+)\`?\.\`?({table_name}\w+)\`?""",
      """message"+:"+([^,]+,){2}({user}[^,]+),""",
      """message"+:"+([^,]+,){2}v(_|-)okta-(\w+-)?({user}\w+)(-|_priv_vault)""",
      """message"+:"+([^,]+,){3}({src_ip}[^,]+),""",
      """,QUERY,({db_name}[^,]+),""",
      """,QUERY,[^,]*,'(?:\/\*[^\/]+\/)?\s*({db_operation}\w+)""",
      """,QUERY,[^,]*,'(?:\/\*[^\/]+\/)?\s*({db_query}[^\}]+?)\s*',({error_code}\d+)?\s*""""
    ]
    DupFields = [ "host->dest_host" ]
  

}
```