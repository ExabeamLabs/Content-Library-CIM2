#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-user-privilege-assign-success-576
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"Special privileges assigned to new logon""", """"event_id":576,"""]
  Fields = [
    """({event_name}Special privileges assigned to new logon)""",
    """"@timestamp"\s*:\s*"({time}[^"]+)"""",
    """"(?:winlog\.)?computer_name"\s*:\s*"({host}[\w\-\.]+)""",
    """({event_code}576)""",
    """({ownership_privilege}SeTakeOwnershipPrivilege)""",
    """({environment_privilege}SeSystemEnvironmentPrivilege)""",
    """({debug_privilege}SeDebugPrivilege)""",
    """({tcb_privilege}SeTcbPrivilege)""",
    """"record_number"\s*:\s*"({event_id}\d+)"""",
    """"user"\s*:\s*\{.*?"identifier"\s*:\s*"({user_sid}[^"]+)"""",
    """"user"\s*:\s*\{.*?"domain":"({domain}[^"]+)"""",
    """"user"\s*:\s*\{.*?"name":"({user}[\w\.\-]{1,40}\$?)"""",
    """"(param4|Privileges)"\s*:\s*"({privileges}[^"]+)"""",
    """"(param3|LogonID|logon_id)"\s*:\s*"(-|({login_id}.+?))\s*"""",
    """"(param3|LogonID|logon_id)"\s*:\s*"\(([^,\s]+(,|\s))?(-|({login_id}.+?)\))"""",
  ]
  DupFields = ["host->dest_host"]


}
```