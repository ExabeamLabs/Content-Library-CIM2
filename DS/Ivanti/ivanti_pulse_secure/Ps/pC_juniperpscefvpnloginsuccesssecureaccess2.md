#### Parser Content
```Java
{
Name = juniper-ps-cef-vpn-login-success-secureaccess-2
ParserVersion = "v1.0.0"
Conditions = [ """CEF:""", """|McAfee|""", """|SecureAccess""", """Primary Authentication For User|""" ]

n-forwarded-juniper-vpn = {
  Vendor = Ivanti
  Product = Ivanti Pulse Secure
  TimeFormat = "epoch"
  Fields = [
    """\srt=({time}\d{13})""",
    """\sshost=({host}.+?)(\s+\w+=|"*\s*$)""",
    """\ssuser=({user}[^\s@"]+)\s+(\w+=|$)""",
    """\ssuser=({email_address}[^\s@"]+@[^\s@"]+)""",
    """\ssuser=({full_name}[^\s@"\=]+\s+[^\s@"\=]+?)(\s+\w+=|"*\s*$)""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sdst=({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sdeviceTranslatedAddress=({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\Wact=({result}.+?)\s+(\w+=|$)""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  ]
  DupFields = ["user->account"
}
```