#### Parser Content
```Java
{
Name = oracle-avdf-kv-database-logout-success-logout
  Vendor = Oracle
  Product = Oracle Audit Vault and Database Firewall 
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [""" TARGET_TYPE="USER"""", """ EVENT_NAME="LOGOUT"""", """ COMMAND_CLASS="LOGOUT"""", """ SECURED_TARGET_NAME=""""]
  Fields = [
    """EVENT_TIME="({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)""",
    """SECURED_TARGET_NAME="({host}[^-]+)-({db_name}[^"]+)"""",
    """USER_NAME="({db_user}[^"]+)"""",
    """SERVICE_NAME="({db_name}[^"]+)"""",
    """EVENT_NAME="({event_name}[^"]+)"""",
    """RECORD_ID="({event_code}[^"]+)"""",
    """SECURED_TARGET_TYPE="({app}[^"]+)"""",
    """SERVICE_NAME="({db_name}[^"]+)""""
  ]


}
```