#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-notification-success-4793
  ParserVersion = "v1.0.0"
  Conditions = [ """eventid="4793"""", """Microsoft-Windows-Security-Auditing""" ]
  Fields = ${DLWindowsParsersTemplates.windows-events-2-dl.Fields}[
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d+Z\s*({host}[^\s]+)\s""",
    """({event_name}The Password Policy Checking API was called)""",
    """\sSecurity ID:\s*({user_sid}[^\s]+)""",
    """\sAccount Name:\s*({account}[^\s]+)""",
    """\sAccount Domain:\s*({domain}.+?)\s*Logon ID:""",
    """\sLogon ID:\s*({login_id}[^\s]+)""",
    """\sAdditional Information:\s*([^:]+:\s*)?({domain}.+?)\s*Provided Account Name""",
    """\sStatus Code:\s*({action}.+?)\s*$""",
  ]

windows-events-2-dl = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """eventid="+({event_code}\d+)""",
    """providername="+({provider_name}[^"]+)""",
    """userid="(?:[^\\]+\\+)?(SYSTEM|NETWORK SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """\stask="+({operation}[^"]+)""",
    """\Weventrecordid="+({event_id}\d+)""""
  
}
```