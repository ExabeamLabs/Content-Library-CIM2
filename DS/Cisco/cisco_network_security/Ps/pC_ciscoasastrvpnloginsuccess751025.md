#### Parser Content
```Java
{
Name = cisco-asa-str-vpn-login-success-751025
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = Cisco Network Security
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss","MMM dd yyyy HH:mm:ss"]
    Conditions = [ """assigned to session""", """-751025""" ]
    Fields = [
      """({time}\w{1,3}\s\d{1,2}\s\d\d\d\d\s\d\d:\d\d:\d\d)\s*(\S+\s+)?:\s%\w+\-"""
      """({time}\d+-\d+-\d+T\d+:\d+:\d+)""",
      """\d\d:\d\d\s+({host}[\w.\-]+)\s+:\s+%\w+\-""",
      """Username:(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))) IKEv2 """,
      """Local:({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """Remote:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """IPv4 Address=(?:0\.0\.0\.0|({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))""",
      """IPv6 address=(?:0\.0\.0\.0|({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))""",
      """Group:({realm}[^\s]+)""",
      """%ASA-({priority}\d+)-({event_code}\d+)"""
    ]
  

}
```