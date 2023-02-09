#### Parser Content
```Java
{
Name = citrix-cgateway-str-vpn-login-success
    ParserVersion = v1.0.0
    Vendor = Citrix
    Product = Citrix Gateway
    TimeFormat = "MM/dd/yyyy:HH:mm:ss"  
    Conditions = [ """SSLVPN ICASTART""", """username:domainname""" ]
    Fields = [
      """\w+\s+\d+\s+\d\d:\d\d:\d\d\s+({host}[\w\-.]+)\s""",
      """({host}[^\s]+)\s+\d\d\/\d\d\/\d\d:""",
      """dvchost=({host}[^\s]+)""",
      """shost=({src_host}[^\s]+)""",
      """dhost=({dest_host}[^\s]+)""",
      """({time}\d\d/\d\d/\d\d\d\d:\d\d:\d\d:\d\d)""",
      """username:domainname\s({user}[^:@]+)(:|@)({domain}[^\s]+[^\s:])?""",
      """Source\s({src_ip}[\w.:]+[^:]):\d+""",
      """Destination\s({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """applicationName\s({app}.+?) - startTime"""
    ]
  

}
```