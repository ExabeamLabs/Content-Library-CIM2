#### Parser Content
```Java
{
Name = ca-pamsc-kv-app-authentication-connection
  Conditions = [ """Transaction: connection""", """, Access/Protocol:""" ]
  Fields = ${DLPamParsersTemplates.pam-events.Fields}[
    """\sDetails:\s+({event_name}.+?)\s+with""",
# target_account is removed
    """\starget account Id\s*:\s*({dest_user_id}[^\s]+)"""
  ]
  ParserVersion = v1.0.0

pam-events = {
  Vendor = MasterSAM
  Product = MasterSAM PAM
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Fields = [
    """({host}[\w\-.]+)\s+Event Time:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+)""",
    """\WUser:\s*(({domain}[^\\\s]+)\\+)?({user}[^\\\s]+)""",
    """\Wname=({dest_host}[\w\-.]+)\s+(\w+=|$)""",
    """\Whost=({dest_ip}[A-Fa-f:\d.]+)""",
    """\Wprotocol=({protocol}.+?)\s+(\w+=|$)""",
    """\Wstatus=({result}.+?)\s+(\w+=|$)""",
    """\Wfailed_message=({failure_reason}.+?)\s+(\w+=|$)""",
    """\WActivity:\s*({operation}.+?)\s+User:""",
  
}
```