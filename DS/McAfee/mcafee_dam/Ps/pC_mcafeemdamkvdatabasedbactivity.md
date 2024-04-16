#### Parser Content
```Java
{
Name = "mcafee-mdam-kv-database-dbactivity"
  Vendor = McAfee
  Product = McAfee DAM
  TimeFormat = "dd MMM yyyy HH:mm:ss"
  Conditions = [ """db_user=""", """db_type=""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s+({host}[^\s]+)\s+(\w+=|$)""",
    """execution_time="({time}\d\d \w{3} \d{4} \d\d:\d\d:\d\d)""",
    """src_ip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """user="(NULL|(({domain}[^"]+)\\+)?({user}[\w\.\-]{1,40}\$?)\s*)"""",
    """cmdtype="({db_operation}[^"]+)"""",
    """sqlstmt="({db_query}.+?)\s*"+\s*(\w+=|$)""",
    """db_name="({db_name}[^"]+)"""",
    """src_host="({src_host}[^"]+)"""",
    """db_user="(NULL|(({db_domain}[^"]+)\\+)?({db_user}.+?)\s*)"""",
    """schema="(NULL|({db_schema}[^"]+))"""",
    """db_type="({app}[^"]+)"""",
    """sid="({user_sid}[^"]+)"""",
    """accessed_objects="(NULL|({additional_info}[^"]+))""""
  ]
  DupFields = [ "db_user->account" ]
  ParserVersion = "v1.0.0"


}
```