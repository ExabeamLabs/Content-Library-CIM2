#### Parser Content
```Java
{
Name = rsa-netwitness-cef-app-logout-success-logoff
  Vendor = RSA
  Product = RSA Netwitness
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = ["""AUTHENTICATION|Logoff"""]
  Fields = [
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|-)\d\d:\d\d)\s*({host}[^\s]+)""",
    """\ssrc=(null|({src_ip}[a-fA-F:\d.]+))""",
    """\sspt=({src_port}\d+)""",
    """\ssuser=(Unknown|({user}[^\s]+))""",
    """\ssourceServiceName =({app}.+?)\s*\w+=""",
    """\sdeviceExternalId=({external_id}.+?)\s*\w+=""",
    """\sdeviceProcessName =({process_name}.+?)\s*\w+=""",
    """\soutcome=({result}.+?)\s*\w+=""",
    """\smsg=(null|({result}.+?))\s*\w+=""",
    """\scs1=(null|({src_ip}.+?))\s*\w+=""",
    """\scs2=(null|({group_name}.+?))\s*\w+=""",
    """\sactionType=(null|({action_type}.+?))\s*\w+=""",
  ]
  ParserVersion = "v1.0.0"


}
```