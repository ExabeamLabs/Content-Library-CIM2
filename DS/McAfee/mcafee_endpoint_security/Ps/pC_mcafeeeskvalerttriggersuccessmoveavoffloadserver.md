#### Parser Content
```Java
{
Name = mcafee-es-kv-alert-trigger-success-moveavoffloadserver
  ParserVersion = v1.0.0
  Conditions = [ """DetectingProductName =MOVE AV Offload Server""" ]
  Fields = ${McAfeeParsersTemplates.mcafee-dlp-alert.Fields}[
    """GeneratedTime=({time}\d{13})"""
  ]

mcafee-dlp-alert = {
  Vendor = McAfee
  Product = McAfee Endpoint Security
  TimeFormat = "epoch"
  Fields = [
    """detecttime=({time}\d{13})"""
    """StartTime=({time}\d{13})""",
    """,HostName =({host}[^,]+)""",
    """,(targetprocessname|sourceprocessname)=({process_path}({process_dir}[^,]*[\\\/]+)?({process_name}[^,\\\/]+))""",
    """,(sourceusername|targetusername|agentusername)=(({domain}[^,\\\/]+)[\\\/]+)?({user}[\w\.\-]{1,40}\$?),""",
    """,sourcehostname=({dest_host}[^,]+)""",
    """,threatseverity=({alert_severity}[^,]+)""",
    """,ThreatSeverity=({alert_severity}[^,]+)""",
    """,eventseverity=({alert_severity}[^,]+)""",
    """,threattype=({alert_type}[^,]+)""",
    """,producthostname=({host}[^,]+)""",
    """,targethostname=({src_host}[^,]+)""",
    """,threatname=({alert_name}[^,]+)""",
    """_DB_DRIVER=({db_driver}[^,]+)""",
    """_DB_PORT=({db_port}\d+)""",
    """_DB_HOST=({dest_host}[^,\.]+)""",
    """_DB_NAME=({db_name}[^,]+?)\s*(,|$)""",
    """,FilePath=({malware_file_name}[^,]+)""",
    """,ThreatName =({alert_name}[^,]+)""",
    """,eventname=({alert_name}[^,]+)""",
    """,Vulnerability Name =({alert_name}[^,]+)""",
    """,ThreatSourceProcessName =({process_name}[^,]+)""",
  
}
```