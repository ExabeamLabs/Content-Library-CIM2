#### Parser Content
```Java
{
Name = rsa-netwitness-cef-app-login-success-httpsrequest
  Vendor = RSA
  Product = RSA Netwitness Platform
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """custom-condition-cont-10052""", """DATA_ACCESS|HttpRequest"""]
  Fields = [
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|-)\d\d:\d\d)\s*({host}[^\s]+)""",
    """\ssrc=(null|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """\sspt=({src_port}\d+)""",
    """\ssuser=(Unknown|({user}[^\s]+))""",
    """\ssourceServiceName =({app}.+?)\s*\w+=""",
    """\sdeviceExternalId=({external_id}.+?)\s*\w+=""",
    """\sdeviceProcessName =({process_name}.+?)\s*\w+=""",
    """\soutcome=({result}.+?)\s*\w+=""",
    """\smsg=(null|({result}.+?))\s*\w+=""",
    """\scs1=(null|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s*\w+=""",
    """\scs2=(null|({group_name}.+?))\s*\w+=""",
    """\sactionType=(null|({action_type}.+?))\s*\w+=""",
    """\smethod\\*=({method}[^,\s]+)""",
    """\suserAgent\\*=({user_agent}.+?)\s*\w+\\*=""",
    """\squeryString\\*=({query_string}[^,\s]+)""",
    """\suri\\*=({uri}[^,\s]+)""",
  ]


}
```