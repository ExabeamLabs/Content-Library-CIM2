#### Parser Content
```Java
{
Name = oracle-db-str-database-query-success-sysdba
    Vendor = Oracle
    Product = Oracle Database
    TimeFormat = "MMM dd HH:mm:ss yyyy z"
    ParserVersion = "v1.0.0" 
    Conditions = [ """CLIENT USER:""", """PRIVILEGE :""", """ACTION :""", """'SYSDBA'""" ]
    Fields = [
      """\s({time}\w{3} \d\d \d\d:\d\d:\d\d \d\d\d\d [+-]\d\d:\d\d)""",
      """ACTION\s+:\[\d+\]\s+'\s*({db_query}({db_operation}\w+).*?)\s*'([\w\s]+\w+\s*:|$)""",
      """\sCLIENT USER:\[\d+\]\s*'({user}[^']+)'""",
      """\sDBID:\[\d+\]\s*'(|({db_name}[^']+))'""",
      """\sDATABASE USER:\[\d+\]\s*'(\/|({account}[^'\\\/\s]+))'""",
      """\sPRIVILEGE :\[\d+\]\s*'({privilege}[^']+)'""",
    ]
    DupFields = [ "user->user", "account->db_user" ]
 

}
```