#### Parser Content
```Java
{
Name = "checkpoint-ngfw-kv-http-session-urlfilter"
Vendor = "Check Point"
Product = "Check Point NGFW"
TimeFormat = "ddMMMyyyy HH:mm:ss"
Conditions = [
"""Product=URL Filtering"""
"""Action="""
"""|rule_name="""
]
Fields = [
""""({time}\d\d\w{3}\d\d\d\d\s\d\d:\d\d:\d\d)"""
"""Origin=({host}[^|\s]+)"""
"""URL=(?:-|({url}[^|\s]+))"""
"""User=({user}[\w\.\-]{1,40}\$?)\s"""
"""src_user_name=(|-|(({first_name}[^\s]+)\s({last_name}[^\s]+)\s\(({user}[\w\.\-]{1,40}\$?)))\)\s*\|"""
"""Action=(?:-|({action}[^|\s]+))"""
"""client_type_os=(?:-|({os}iOS|Android|BlackBerry|Windows Phone|BeOS|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin))"""
"""connection_count=(?:-|({count}\d+))"""
"""\|rule_name=(?:-|({rule}[^|]+))"""
"""\|SIP=(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
"""\|DIP=(?:-|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
"""\|SPort=(?:-|({src_port}\d+))"""
"""\|DPort=(?:-|({dest_port}\d+))"""
"""web_client_type=({user_agent}[^|\s]+)"""
"""Protocol=(?:-|({protocol}[^|\s]+))"""
"""IFDirection=(?:-|({direction}[^|\s]+))"""
"""Source=(?:[-\d.]+|({src_host}[^|\s]+))"""
"""Destination=(?:[-\d.]+|({dest_host}[^|\s]+))"""
"""XlateSIP=(?:-|({src_translated_ip}[A-Fa-f:\d.]+))"""
"""XlateDIP=(?:-|({dest_translated_ip}[A-Fa-f:\d.]+))"""
"""XlateDPort=(?:-|({dest_translated_port}\d+))"""
"""XlateSport=(?:-|({src_translated_port}\d+))"""
]
ParserVersion = "v1.0.0"


}
```