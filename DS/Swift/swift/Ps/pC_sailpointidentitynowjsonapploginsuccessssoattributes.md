#### Parser Content
```Java
{
Name = "sailpoint-identitynow-json-app-login-success-ssoattributes"
Conditions = [
""""type": "SSO""""
""""stack": """"
""""attributes":"""
]
ParserVersion = "v1.0.0"

s-sailpoint-activity.Fields} [
    """"application":\s*"((null)|({app}[^"]+))"""",
    """"info":\s*"((NONE)|({additional_info}[^"]+))""""
  ]
  ParserVersion = "v1.0.0"
},

${SwiftAllianceWebPlatformTemplates.Swift-Alliance-Web-Platform}{
    Name = swift-s-cef-user-password-modify-fail-changefailed
    Product = Swift
    Conditions = [ """|SWIFT|Alliance Web Platform|""", """|password.changeFailed|"""]
    ParserVersion = "v1.0.0"
},

{
  Name = barracuda-firewall-kv-vpn-login-success-accountinglogin
  ParserVersion = v1.0.0
  Vendor = Barracuda
  Product = Barracuda Cloudgen Firewall
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [ """ CP-FW Session """, """ Accounting LOGIN """ ]
  Fields = [
    """\sCP-FW Session\s+\S*?({user}[^\-:]+):""",
    """\suser=(|({user}.+?))(\s+\w+=|\s*$)""",
    """\sIP=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sstart="({time}\d\d\d\d/\d\d/\d\d \d\d:\d\d:\d\d)""",
  
}
```