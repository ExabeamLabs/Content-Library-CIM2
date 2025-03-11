#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-process-close-success-4689
  ParserVersion = "v1.0.0"
  Conditions = [ """eventid="4689"""", """Microsoft-Windows-Security-Auditing""" ]
  Fields = ${DLWindowsParsersTemplates.windows-events-2-dl.Fields}[
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d+Z\s*({host}[^\s]+)\s""",
    """({event_name}A process has exited)""",
    """\sSecurity ID:\s*({user_sid}[^\s]+)""",
    """\sAccount Name:\s*({account}[^\s]+)""",
    """\sAccount Domain:\s*({domain}[^\s]+)""",
    """\sLogon ID:\s*({login_id}[^\s]+)""",
    """\sProcess ID:\s*({process_id}[^\s]+)""",
    """\sProcess Name:\s*({process_path}[^\s]+?\s*({process_name}[^\s\\\/]+))\s"""
    """\sExit Status:\s*({action}[^\s]+)""",
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