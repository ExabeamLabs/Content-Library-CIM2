#### Parser Content
```Java
{
Name = juniper-ps-str-vpn-login-success-sessionstarted
    ParserVersion = v1.0.0
    Vendor = Ivanti
    Product = Ivanti Pulse Secure
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [
""": Session started for user""", """Juniper:"""
]
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
      """"@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
      """\sfw=({dest_host}({host}[\w\-\.]+))""",
      """({dest_host}({host}[\w\-\.]+))\s*:\s*\S+\s*\-\s*({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d).*?: Session started for user""",
      """,\s+hostname\s+({src_host}[\w.\-]+)""",
      """({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s*(Juniper|PulseSecure)"""
      """\- \[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]"""
      """\- \[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\s+([\w\s]+?::)?(({domain}[^\\]+)\\)?(({email_address}[^@]+@[^\.]+\.[^\(]+)|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\(({realm}[^\[]+)?\)\[(?!Machine Cert)"""
      """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s""",
      """with IP(?:v4 address)?\s+({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
      """\srealm=[\\"]*({realm}.+?)[\\"]*(\s+\w+=|\s*")""",
      """\sroles=[\\"]*({role}.+?)[\\"]*(\s+\w+=|\s*")""",
      """\svpn=[\\"]*({vpn_client}.+?)[\\"]*(\s+\w+=|\s*")""",
      """user=({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*")"""
    ]
  

}
```