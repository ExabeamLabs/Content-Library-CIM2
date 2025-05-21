#### Parser Content
```Java
{
Name = rsa-netwitness-cef-app-logout-success-logoff
  Vendor = RSA
  Product = RSA NetWitness Platform
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = ["""AUTHENTICATION|Logoff"""]
  Fields = [
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|-)\d\d:\d\d)\s*({host}[^\s]+)""",
    """\ssrc=(null|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """\sspt=({src_port}\d+)""",
    """\ssuser=(Unknown|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """\ssourceServiceName =({app}.+?)\s*\w+=""",
    """\sdeviceExternalId=({external_id}.+?)\s*\w+=""",
    """\sdeviceProcessName =({process_name}.+?)\s*\w+=""",
    """\soutcome=({result}.+?)\s*\w+=""",
    """\smsg=(null|({result}.+?))\s*\w+=""",
    """\scs1=(null|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s*\w+=""",
    """\scs2=(null|({group_name}.+?))\s*\w+=""",
    """\sactionType=(null|({operation}.+?))\s*\w+=""",
  ]
  DupFields = [ "operation->action_type"]
  ParserVersion = "v1.0.0"


}
```