#### Parser Content
```Java
{
Name = mastersam-pam-kv-app-activity-updateresource
  Vendor = MasterSAM
  Product = MasterSAM PAM
  ParserVersion = "v1.0.0"
  Conditions = [ """ Activity:update_resource """ ]

mastersam-pam-events-1 = {
  Vendor = MasterSAM
  Product = MasterSAM PAM
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Fields = [
    """({host}[\w\-.]+)\s+Event Time:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+)""",
    """\WUser:\s*(({domain}[^\\\s]+)\\+)?({user}[^\\\s]+)""",
    """\Wname=({dest_host}[\w\-.]+)\s+(\w+=|$)""",
    """\Whost=({dest_ip}[A-Fa-f:\d.]+)""",
    """\Wprotocol=({protocol}.+?)\s+(\w+=|$)""",
    """\Wstatus=({action}.+?)\s+(\w+=|$)""",
    """\Wfailed_message=({failure_reason}.+?)\s+(\w+=|$)""",
    """\WActivity:\s*({operation}.+?)\s+User:""",
  
}
```