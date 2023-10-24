#### Parser Content
```Java
{
Name = "cisco-ise-cef-endpoint-login-success-authpassed"
Vendor = "Cisco"
Product = "Cisco ISE"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
"""|CISCO|ISE|"""
"""msg=NOTICE Passed-Authentication"""
"""app=Radius"""
]
Fields = [
"""\srt=({time}\d+)"""
"""\srt=({time}[A-Za-z]{3} \d\d \d{4} \d\d:\d\d:\d\d)"""
"""\sdvchost=({host}[^\s]+)"""
"""\sduser=(?:|(({domain}[^\\=]+)\\+)?({user}(?:({computer_name}([A-F0-9]{2}\-){5}[A-F0-9]{2})|.+?)))\scn1="""
"""\sdhost=({dest_host}[^\s]+)"""
"""\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\sdst=({auth_server}[^\s]+)"""
"""\sshost=({src_host}[^\s]+)"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```