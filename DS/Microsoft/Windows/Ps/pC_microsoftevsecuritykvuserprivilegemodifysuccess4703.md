#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-user-privilege-modify-success-4703
  ParserVersion = "v1.0.0"
  Conditions = [ """eventid="4703"""", """Microsoft-Windows-Security-Auditing""" ]
  Fields = ${DLWindowsParsersTemplates.windows-events-2.Fields}[
    """({event_name}A token right was adjusted)""",
    """\sSecurity ID:\s*({user_sid}[^\s]+)""",
    """\sAccount Name:\s*({account}[^\s]+)""",
    """\sAccount Domain:\s*({domain}[^\s]+)""",
    """\sLogon ID:\s*({login_id}[^\s]+)""",
    """\sProcess ID:\s*({process_id}[^\s]+)""",
    """\sProcess Name:\s*({process_path}[^\s]+)""",
    """\sPrivileges:\s*({privileges}.+?)\s*Disabled Privileges:""",
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