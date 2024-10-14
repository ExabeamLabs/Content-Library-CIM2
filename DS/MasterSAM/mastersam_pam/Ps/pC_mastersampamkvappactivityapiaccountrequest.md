#### Parser Content
```Java
{
Name = mastersam-pam-kv-app-activity-apiaccountrequest
  Vendor = MasterSAM
  Product = MasterSAM PAM
  ParserVersion = "v1.0.0"
  Conditions = [ """ Activity:api_account_request """ ]
  Fields = ${DLMasterSAMParsersTemplates.mastersam-pam-events-1.Fields} [
    """\Wresource_name=({target}.+?)\s+(\w+=|$)""",
    """\Waccount_name=({object}.+?)\s+(\w+=|$)""",
  ]

mastersam-pam-events-1 = {
  Vendor = MasterSAM
  Product = MasterSAM PAM
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Fields = [
    """({host}[\w\-.]+)\s+Event Time:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+)""",
    """\WUser:\s*(({domain}[^\\\s]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """\Wname=({dest_host}[\w\-.]+)\s+(\w+=|$)""",
    """\Whost=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wprotocol=({protocol}.+?)\s+(\w+=|$)""",
    """\Wstatus=({action}.+?)\s+(\w+=|$)""",
    """\Wfailed_message=({failure_reason}.+?)\s+(\w+=|$)""",
    """\WActivity:\s*({operation}.+?)\s+User:""",
  
}
```