#### Parser Content
```Java
{
Name = microsoft-evapp-json-endpoint-activity-success-catchall
  ParserVersion = v1.0.0
  Product = Event Viewer - Application
  Conditions = [ """"EventID":""", """"Channel":"Application"""", """"ProviderName":"""" ]  

microsoft-json-events}{
  Name = microsoft-evsecurity-json-endpoint-activity-success-catchall
  ParserVersion = v1.0.0
  Product = Event Viewer - Security
  Conditions = [ """"EventID":""", """"Channel":"Security"""", """"ProviderName":"""" ]  
  Fields = ${WindowsParsersTemplates.microsoft-json-events.Fields}[
    """Subject:\s*Security ID:\s*({user_sid}[^:]+?)(\s+\w+){1,2}:\s"""
    """Subject:[^"]+?Account Name:\s*(({domain}[^:\\]+?)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+\w+){1,2}:\s"""
    """Subject:[^"]+?Account Domain:\s*({domain}[^:]+?)(\s+\w+){1,2}:\s"""
    """Subject:[^"]+?Logon ID:\s*({login_id}[^:]+?)(\s+\w+){1,2}:\s"""
  ]  
},

${WindowsParsersTemplates.microsoft-json-events}{
  Name = microsoft-evapp-json-endpoint-activity-success-catchall
  ParserVersion = v1.0.0
  Product = Event Viewer - Application
  Conditions = [ """"EventID":""", """"Channel":"Application"""", """"ProviderName":"""" ]  
},

${WindowsParsersTemplates.microsoft-json-events}{
  Name = microsoft-evsystem-json-endpoint-activity-success-catchall
  ParserVersion = v1.0.0
  Product = Event Viewer - System
  Conditions = [ """"EventID":""", """"Channel":"System"""", """"ProviderName":"""" ]  
}

{
  Name = claroty-ctd-cef-app-activity-success-catch-all
  Vendor = Claroty
  Product = CTD
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """CEF:""", """|CTD|""" ]
  Fields = [
      """CtdTimeGenerated=({time}\w\w\w \d\d \d\d\d\d \d\d:\d\d:\d\d)"""
      """start=({time}\w\w\w \d\d \d\d\d\d \d\d:\d\d:\d\d)"""
      """({time}\w\w\w \d\d \d\d\d\d \d\d:\d\d:\d\d)\s\w{3}\sCEF:""",
      """\|CTD\|([^\|]+\|){2}({alert_name}[^\|]+)\|({alert_severity}[^\|]+)""",
      """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s""",
      """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s""",
      """dhost=({dest_host}[\w\-\.]+)""",
      """cn2=({alert_id}\d+)""",
      """shost=({src_host}[^=]+)\s\w+=""",
      """smac=({src_mac}[^=]+)\s\w+=""",
      """dmac=({dest_mac}[^=]+)\s\w+=""",
      """\suser:\s({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
      """\suser\s'({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
      """msg=({additional_info}[^=]+)\s\w+="""
      """CtdMessage=({additional_info}[^=]+?)\s\w+="""
      """CtdCategory=({category}[^=]+?)\s\w+="""
      """CtdAlertLink=({url}[^=]+?)\s\w+="""
      """CtdAlertStatus=({alert_status}[^=]+?)\s\w+="""
      """CtdMitreAttackTechniqueIds=({mitre_labels}[^=]+?)\s\w+="""
      """proto=({protocol}[^=]+?)\s\w+="""
    ]
    DupFields = ["alert_name->alert_type","alert_name->event_name"]
    ParserVersion = "v1.0.0"
}
{
  Name = vmware-esxi-str-app-activity-hostd-1
  Vendor = VMware
  Product = VMware ESXi
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """Hostd: """ ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)\s+({host}[^\s]+)\s""",
    """Hostd:\s*({additional_info}[^=]+?)\s*$"""
  
}
```