#### Parser Content
```Java
{
Name = microsoft-m365auditlogs-kv-file-download-success-exportartifact
  ParserVersion = v1.0.0
  Product = M365 Audit Logs
  Conditions = [ """SESSID=""", """RESULTCODE=""", """WORKLOAD=""", """COMMAND=ExportArtifact""", """WORKSPACENAME=""", """OBJECT=""" ]
  Fields = ${DLMicrosoftParsersTemplates.logrhythm-o365-app-activity.Fields}[
    """WORKLOAD=({resource}[^=]+?)\s+\w+=""",
    """DATASETNAME=({data_set_name}[^=]+?)\s+\w+=""",
    """ISSUCCESS=({result}[^=]+?)\s+\w+=""",
  ]

logrhythm-o365-app-activity = {
  Vendor = Microsoft
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """\sTS=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """USER=(Unknown|({email_address}[^@\s]+@[^\s\.]+?\.[^\s]+?)|({user}[^\s@]+)(@({email_domain}[^\s]+))?)\s+\w+=""",
    """DOMAIN=(|({domain}[^\s]+?))\s+\w+=""",
    """WORKLOAD=({app}[^=]+?)\s+\w+=""",
    """COMMAND=({event_name}[^=]+?)\s+\w+=""",
    """OBJECT=(Unknown \(Unknown\)|({object}[^=]+?))\s+\w+=""",
    """\sFILENAME=({file_name}[^=]+?(\.({file_ext}[^\s\=\.]+))?)\s+\w+=""",
    """SIP=({src_ip}[a-fA-F\d:.]+)""",
    """USERAGENT=\s*(|({user_agent}[^\n]+?))\s*(\w+=|$)""",
    """ITEMTYPE=({file_type}[^=]+?)\s+\w+=""",
    """RESULTCODE=({result}[^=]+?)\s+\w+="""
  ]
  DupFields = [ "event_name->operation" 
}
```