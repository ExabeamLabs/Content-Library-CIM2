#### Parser Content
```Java
{
Name = oracle-db-str-database-query-success-sysdba
    Vendor = Oracle
    Product = Oracle Database
    TimeFormat = ["MMM dd HH:mm:ss yyyy z","yyyy-MM-dd'T'HH:mm:ss.SSSSSS"]
    ParserVersion = "v1.0.0" 
    Conditions = [ """CLIENT USER:""", """PRIVILEGE :""", """ACTION :""", """'SYSDBA'""" ]
    Fields = [
      """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+)[-|+]\d+:\d\d\s*({host}[\w\-.]+)""",
      """\s({time}\w{3} \d\d \d\d:\d\d:\d\d \d\d\d\d [+-]\d\d:\d\d)""",
      """ACTION\s+:\[\d+\]\s+'\s*({db_query}({db_operation}\w+).*?)\s*'([\w\s]+\w+\s*:|$)""",
      """\sCLIENT USER:\[\d+\]\s*'({user}[\w\.\-\!\#\^\~]{1,40}\$?)'""",
      """\sDBID:\[\d+\]\s*'(|({db_name}[^']+))'""",
      """\sDATABASE USER:\[\d+\]\s*'(\/|({account}[^'\\\/\s]+))'""",
      """\sPRIVILEGE :\[\d+\]\s*'({privileges}[^']+)'""",
    ]
    DupFields = [ "user->user", "account->db_user" ]
 

}
```