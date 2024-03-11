#### Parser Content
```Java
{
Name = dell-sw-cef-vpn-logout-success-loggedout
  Vendor = Dell
  Product = Sonicwall
  TimeFormat = "epoch"
  Conditions = [ """|Sonicwall|VPN|""", """logged out|"""]
  Fields = [
    """\srt=({time}\d{13})""",
    """\sdvc=({host}\S+)""",
    """\sdvchost=({host}\S+)""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\sdhost=({dest_host}\S+)""",
    """\sduser=(|({user}.+?))\s+(\w+=|$)""",
    """\scs4Label=Duration\s.*cs4=({session_duration}\d+)\s+(\w+=|$)""",
    """\scs4=({session_duration}\d+)\s+(|\w+=.*)cs4Label=Duration\s""",
  ]
  ParserVersion = "v1.0.0"


}
```