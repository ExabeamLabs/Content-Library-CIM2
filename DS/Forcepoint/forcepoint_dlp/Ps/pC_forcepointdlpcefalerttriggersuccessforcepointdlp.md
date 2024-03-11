#### Parser Content
```Java
{
Name = forcepoint-dlp-cef-alert-trigger-success-forcepointdlp
  ParserVersion = v1.0.0
  Vendor = Forcepoint
  Product = Forcepoint DLP
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """|Forcepoint|Forcepoint DLP|""", """sourceServiceName =""" ]
  Fields = [
    """timeStamp=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+)""",
    """\Wdvc=(N\/A|({host}[A-Fa-f:\d.]+))""",
    """\Wdvchost=(N\/A|({host}[\w\-.]+))""",
    """({host}[\w\-.]+)\s+CEF:""",
    """\Wact=({action}.+?)(\s\-\s|\s+[\w\.]+=|$)""",
    """\Wduser=(N\/A|({target}[^\s;]+))""",
    """\sduser=({url}(\w+:\/+)?({web_domain}[^\\\/]+)[^\s]+)\s+\w+=""",
    """\Wfname=(N\/A|.*?[\/\\]*({file_name}[^\\\/=]+?))\s+\- [\d.]+ """,
    """\Wfname=(N\/A|.*? - ({bytes}[\d.]+)\s+({bytes_unit}[^\s;]+))""",
    """\Wfname=(N\/A|.*? - ({bytes_val}[\d.]+\s+[^\s;]+))""",
    """\Wmsg=\s*({additional_info}.+?)(\s+\-\s|\s+[\w\.]+=|$)""",
    """\Wcat=({alert_name}.+?)(\s\-\s|\s+[\w\.]+=|$)""",
    """\WsourceServiceName =({alert_type}.+?)\s+(on |\w+=)""",
    """\WloginName =(N\/A|({full_name}[^@\(=\\]+?)\s*(\([^\)]+\)?)?(@({domain}[^@\s]+))?)(\s\-\s|\s+[\w\.]+=|$)""",
    """\Wsuser=(({domain}[^\\\s,@=]+)\\+)?({user}[^\\\s,@=]+)\s+(\w+=|$)""",
    """\WloginName =(?:N\/A|(({domain}[^\\,]+)\\+)?({user}[^\\\s,]+))(\s\-\s|\s+[\w\.]+=|$)""",
    """\Wsuser=(Executive Inquiry Mailbox|({full_name}[^\\\s,@=]+?\s+[^\\,@=]+?))\s+(\w+=|$)""",
    """\Wsuser=({last_name}[^\\,=]+?),\s+({first_name}[^\\,=]+?)\s+(\w+=|$)""",
    """\Wsuser=({email_address}[^\\\s,@=]+?@[^\\\s,@=]+?)\s+(\w+=|$)""",
    """\WsourceIp=(?:N\/A|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """\WseverityType=({alert_severity}[^\s]+)""",
    """\WsourceHost=(?:N\/A|({src_host}[\w\-.]+))""",
    """\WdestinationHosts=(?:N\/A|(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w\-.]+)))""",
  ]
  SOAR {
    IncidentType = "dlp"
    DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "alert_type->description", "user->dlpUser", "alert_name->dlpPolicy", "alert_severity->sourceSeverity","file_name->dlpFileName", "bytes_val->dlpFileSize", "action->dlpActionTaken","host->dlpDeviceName"]
    NameTemplate = """Forcepoint DLP Alert ${alert_name} found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="device", Name ="src_address", Fields=["src_ip->ip_address", "src_host->host_name"]

}
```