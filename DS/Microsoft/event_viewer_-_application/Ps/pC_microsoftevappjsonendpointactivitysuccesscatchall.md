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