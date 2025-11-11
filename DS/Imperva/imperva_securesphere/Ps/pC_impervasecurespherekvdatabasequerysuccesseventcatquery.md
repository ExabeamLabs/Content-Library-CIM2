#### Parser Content
```Java
{
Name = imperva-securesphere-kv-database-query-success-eventcatquery
  ParserVersion = v1.0.0
  Vendor = Imperva
  Product = Imperva SecureSphere
  TimeFormat = "yyyy-MM-dd HH:mm:ss Z"
  Conditions = [ """db_query=""", """db_username=""", """event_cat=Query,""", """service_name=""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d [+-]\d\d\d\d)""",
    """app="({app}[^",]+)""",
    """db_query="?({db_query}.+?)",\s""",
    """db_username="?({account}({db_user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """dst_ip="?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """dst_port="?({dest_port}\d+)"""
    """event_cat="?({event_category}[^,"]+)"""
    """event_id="?({alert_id}[^,\s"]+)"""
    """group_name="?({group_name}[^",]+)"""
    """object="?({object}[^",]+)"""
    """operation="({operation}[^"]+)"""
    """operation=({operation}[^",]+)"""
    """policy="?({policy_name}[^",]+)"""
    """server_group="?({additional_info}[^",]+)"""
    """service_name="?({service_name}[^",]+)"""
    """src_ip="?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """src_port=({src_port}\d+)"""
    """src_username="?({src_user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  ]
}  

{
  Name = imperva-securesphere-kv-alert-trigger-success-catsecurity
  ParserVersion = v1.0.0
  Vendor = Imperva
  Product = Imperva SecureSphere
  TimeFormat = "yyyy-MM-dd HH:mm:ss Z"
  Conditions = [ """db_query=""", """db_username=""", """cat=Security,""", """alert_severity=""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d [+-]\d\d\d\d)""",
    """alert_severity=({alert_severity}[^,]+)""",
    """db_query="?({db_query}.+?)",\s""",
    """db_username="?({account}({db_user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """db_name="?({db_name}[^,"]+)"""
    """schema="?({db_schema}[^",]+)"""
    """dst_ip="?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """dst_port="?({dest_port}\d+)"""
    """event_cat="?({alert_type}[^,"]+)"""
    """event_id="?({alert_id}[^,\s"]+)"""
    """object="?({object}[^",]+)"""
    """operation="({alert_name}({operation}[^"]+))"""
    """operation=({alert_name}({operation}[^",]+))"""
    """policy="?({policy_name}[^",]+)"""
    """description="({additional_info}[^"]+)"""
    """service_name="?({service_name}[^",]+)"""
    """src_ip="?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """src_port=({src_port}\d+)"""
    """src_host="?({src_host}[\w.-]+)"""
    """cat=({category}Security)"""
    """server_group="?({server_group}[^",]+)"""  
    """sql_error="({sql_error}[^"]+)""""  
  ]


}
```