#### Parser Content
```Java
{
Name = dell-sw-cef-vpn-login-success-userloginsuccessful
  ParserVersion = v1.0.0
  Vendor = Dell
  Product = Sonicwall
  TimeFormat = "epoch"
  Conditions = [ """|Sonicwall|VPN|""", """|User login successful|"""]
  Fields = [
    """\srt=({time}\d{13})""",
    """\sdvc=({host}\S+)""",
    """\sdvchost=({host}\S+)""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\sdhost=({dest_host}\S+)""",
    """\sduser=(|({user}.+?))\s+(\w+=|$)""",
    """\scs5Label=Portal\s.*cs5=({realm}.+?)\s+(\w+=|$)""",
    """\scs5=({realm}.+?)\s+(|\w+=.*)cs5Label=Portal\s""",
  ]
  DupFields = ["user->account"]


}
```