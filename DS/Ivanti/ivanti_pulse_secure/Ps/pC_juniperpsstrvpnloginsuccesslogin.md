#### Parser Content
```Java
{
Name = juniper-ps-str-vpn-login-success-login
   ParserVersion = v1.0.0
   Vendor = Ivanti
   Product = Ivanti Pulse Secure
   TimeFormat = "yyyy-MM-dd HH:mm:ss"
   Conditions = [ 
"""PulseSecure:"""
"""Remote address for user"""
]
   Fields = [
     """PulseSecure: (\S+\s\S+\s\S+\s)?({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d) - (::ffff:)?({host}\S+) - \[(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\] ([\w\s]+?::)?(({email_address}[^@\s\(]+@[^\.\s]+\.[^\s]+)|(({domain}[^\\]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))\(""",
     """changed from (::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))? to (::ffff:)?({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
     """({os}iOS|Android|BlackBerry|iPhone OS|Windows Phone|BeOS|(?:W|w)indows\s+\d{1,2}|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin)"""
     """\]\s+([\w\s]+?::)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^\(]+))?\(({realm}[^\)]+)?"""
   ]
   DupFields = [ "user->account" ]
  

}
```