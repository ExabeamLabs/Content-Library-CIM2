#### Parser Content
```Java
{
Name = ca-pamsc-kv-app-activity-admin
  ParserVersion = v1.0.0
  Conditions = [ """Transaction: admin""", """, Access/Protocol:""" ]

pam-events = {
  Vendor = MasterSAM
  Product = MasterSAM PAM
  TimeFormat = ["yyyy-MM-dd HH:mm:ss.SSS","yyyy-MM-dd HH:mm:ss.SS"]
  Fields = [
    """({host}[\w\-.]+)\s+Event Time:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+)""",
    """\WUser:\s*(({domain}[^\\\s]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """\Wname=({dest_host}[\w\-.]+)\s+(\w+=|$)""",
    """\Whost=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wprotocol=({protocol}.+?)\s+(\w+=|$)""",
    """\Wstatus=({result}.+?)\s+(\w+=|$)""",
    """\Wfailed_message=({failure_reason}.+?)\s+(\w+=|$)""",
    """\WActivity:\s*({operation}.+?)\s+User:""",
  
}
```