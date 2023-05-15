#### Parser Content
```Java
{
Name = beyondtrust-bi-json-user-unlock-success-unlock
  ParserVersion = v1.0.0
  Conditions = [ """"operation":"Unlock"""", """"vendor":"BeyondTrust"""", """"product":"BeyondInsight"""", """"eventdesc":""" ]

json-beyondtrust-activity = {
  Vendor = BeyondTrust
  Product = BeyondInsight
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Fields = [
    """"eventdate":"({time}\w\w\w\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)""",
    """"sourcehost":"({host}[\w\-\.]+)""",
    """"sourceip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """"user":"(({domain}[^\\\/]+)\\+)?(Internal process|({user}[^"]+))""",
    """"operation":"({operation}[^"]+)""",
    """"failed":"({result}\d)""",
    """"ipaddress":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """"target":"Asset:({dest_host}[\w\-\.]+)\sMAccount:({account}[\w\-\.]+)""",
    """"target":"Domain:[^:]+?MAccount:({account}[\w\-\.]+)""",
    """"target":"[^"]+?ManagedAccount=({account}[\w\-\.]+)""",
    """"target":"[^\/,]+\/({dest_host}[\w\-\.]+),\sAccount\s""",
    """({app}BeyondInsight)"""
    ]
 
}
```