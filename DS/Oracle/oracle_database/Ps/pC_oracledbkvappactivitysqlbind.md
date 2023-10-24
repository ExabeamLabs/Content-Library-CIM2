#### Parser Content
```Java
{
Name = oracle-db-kv-app-activity-sqlbind
  Vendor = Oracle
  Product = Oracle Database
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"userhost":""",""""sqlbind":""",""""auditid":""" ]
  Fields = [
    """"ntimestamp#":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""",
    """"userhost":"({host}[\w\-.]+)"""",
    """"userid":"({db_user}[^"]+)"""",
    """"sessionid":"({session_id}[^"]+)"""",
    """"dbid":"({db_id}[^"]+)"""",
# action_code is removed
    """"comment\$text":"({additional_info}[^"]+)""""
  ]
  DupFields = [ "db_user->user" ]


}
```