#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-notification-success-4793
  ParserVersion = "v1.0.0"
  Conditions = [ """eventid="4793"""", """Microsoft-Windows-Security-Auditing""" ]
  Fields = ${DLWindowsParsersTemplates.windows-events-2.Fields}[
    """({event_name}The Password Policy Checking API was called)""",
    """\sSecurity ID:\s*({user_sid}[^\s]+)""",
    """\sAccount Name:\s*({account}[^\s]+)""",
    """\sAccount Domain:\s*({domain}.+?)\s*Logon ID:""",
    """\sLogon ID:\s*({login_id}[^\s]+)""",
    """\sAdditional Information:\s*({domain}.+?)\s*Provided Account Name""",
    """\sStatus Code:\s*({action}.+?)\s*$""",
  ]

windows-events-2 = {
  Vendor = Microsoft
  Product = Windows
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d+Z\s*({host}[^\s]+)\s""",
    """eventid="+({event_code}\d+)""",
    """providername="+({provider_name}[^"]+)""",
    """userid="(?:[^\\]+\\+)?(SYSTEM|NETWORK SERVICE|({user}[^"]+))""",
    """\stask="+({operation}[^"]+)""",
    """\Weventrecordid="+({event_id}\d+)"""",
  ]
  DupFields = ["event_id->event_code"
}
```