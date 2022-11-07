#### Parser Content
```Java
{
Name = cisco-asa-cef-vpn-login-success-113039
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "epoch"
  Conditions = [ """|CISCO|ASA|""", """|113039|""" ]
  Fields = [
    """\srt=({time}\d*)""",
    """\|({event_code}113039)""",
    """\sduser=(?:({domain}[^\s]+?)\\+)?({user}.+?)\s+([\w.]+=|$)""",
    """\sdhost=({dest_host}.+?)\s+([\w.]+=|$)""",
    """\sdst=({dest_ip}[a-fA-F\d.:]+)""",
    """\sdvchost=({host}.+?)\s+([\w.]+=|$)""",
  ]
  DupFields = [ "host->dest_host" , "user->account"]
  ParserVersion = "v1.0.0"


}
```