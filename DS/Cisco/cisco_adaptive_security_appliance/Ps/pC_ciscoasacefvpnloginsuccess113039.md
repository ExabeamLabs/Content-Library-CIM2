#### Parser Content
```Java
{
Name = cisco-asa-cef-vpn-login-success-113039
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "epoch"
  Conditions = [ """|CISCO|ASA|""", """|113039|""" ]
  Fields = [
    """\srt=({time}\d{13})""",
    """\|({event_code}113039)""",
    """\sduser=(?:({domain}[^\s]+?)\\+)?({user}.+?)\s+([\w.]+=|$)""",
    """\sdhost=({dest_host}.+?)\s+([\w.]+=|$)""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\sdvchost=({host}.+?)\s+([\w.]+=|$)""",
  ]
  DupFields = [ "host->dest_host" , "user->account"]
  ParserVersion = "v1.0.0"


}
```