#### Parser Content
```Java
{
Name = juniper-ps-str-vpn-login-success-started
    ParserVersion = v1.0.0
    Vendor = Ivanti
    Product = Ivanti Pulse Secure
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ 
"""PulseSecure:"""
""": Session started for user"""
"""Network"""
]
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s-\s""",
      """({host}[\w\-\.]+)\s*:\s*\S+\s*\-\s*({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d).*?: Session started for user""",
      """({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|[\w\-\.]+)\s*(Juniper|PulseSecure):""",
      """PulseSecure:\s*({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)\s+\-\s+({host}[\w\-.]+)""",
      """\s+({host}[\w-.]+)\s+PulseSecure:""",
      """PulseSecure:\s*\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d\s+\-\s+({dest_host}[\w\-.]+)""",
      """,\s+hostname\s+({src_host}[\w.\-]+)""",
      """\s(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w.\-]+))\s+(Juniper|PulseSecure):""",
      """\- \[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]"""
      """\- \[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\s+([\w\s]+?::)?(({email_address}[^@\s\(]+@[^\.\s\(]+\.[^\s\(]+)|(({domain}[^\\]+)\\)?({user}[^\(]+))\(({realm}[^\[]+)?\)\[(?!Machine Cert)""",
      """with IP(?:v4 address)?\s+({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
      """Session started for user\s+\(({additional_info}[^\)]+)\)\s"""
    ]
    DupFields = [ "host->dest_host" , "user->account" ]
  

}
```