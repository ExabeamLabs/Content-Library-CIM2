#### Parser Content
```Java
{
Name = mcafee-es-kv-alert-trigger-success-endpointsecurity
  ParserVersion = v1.0.0
  Conditions = [ """DetectingProductName =McAfee Endpoint Security""" ]

mcafee-dlp-alert = {
  Vendor = McAfee
  Product = McAfee Endpoint Security
  TimeFormat = "epoch"
  Fields = [
    """StartTime=({time}\d+)""",
    """,HostName =({host}[^,]+)""",
    """,(targetprocessname|sourceprocessname)=({process_path}({process_dir}[^,]*[\\\/]+)?({process_name}[^,\\\/]+))""",
    """,(sourceusername|targetusername)=(({domain}[^,\\\/]+)[\\\/]+)?({user}[^,\\\/]+),""",
    """,sourcehostname=({dest_host}[^,]+)""",
    """,threatseverity=({alert_severity}[^,]+)""",
    """,threattype=({alert_type}[^,]+)""",
    """,producthostname=({host}[^,]+)""",
    """,targethostname=({src_host}[^,]+)""",
    """,threatname=({alert_name}[^,]+)""",
    """_DB_DRIVER=({db_driver}[^,]+)""",
    """_DB_PORT=({db_port}\d+)""",
    """_DB_HOST=({host}[^,]+)""",
    """_DB_NAME=({db_name}[^,]+?)\s*(,|$)""",
  
}
```