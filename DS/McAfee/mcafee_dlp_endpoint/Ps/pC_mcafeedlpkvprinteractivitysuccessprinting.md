#### Parser Content
```Java
{
Name = mcafee-dlp-kv-printer-activity-success-printing
  Vendor = McAfee
  Product = McAfee DLP Endpoint
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """IncidentType="""", """ViolationLocalTime="""", """RulesToDisplay=""", """Printing""", """FileName =""" ]
  Fields = [
     """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d{1,100}), IncidentId""",
     """\sApplicationProductName ="*({app}[^"]+)""",
     """\sTotalContentSize="*({bytes}\d+)""",
     """\sIP="*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
     """\sRulesToDisplay="*({event_name}[^"]+)""",
     """\sName ="*({host}[^"]+)""",
     """\sFileName ="*({object}[^"]+)""",
     """\sdestination="*({printer_name}[^"]+)""",
     """\sUsername_NTLM="*(({domain}[^\\]+)\\*)?({user}[^"]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```