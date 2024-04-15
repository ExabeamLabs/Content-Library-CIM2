#### Parser Content
```Java
{
Name = "cisco-asa-kv-radius-traffic-success-113004-1"
Vendor = "Cisco"
Product = "Cisco Adaptive Security Appliance"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
  """%ASA"""
  """-113004"""
  """AAA user """
  """ Successful"""
]
Fields = [
"""({time}\w{3} \d\d \d{4} \d\d:\d\d:\d\d)"""
"""\d\d:\d\d:\d\d\s+(::ffff:)?({host}[^\s]+)\s*:?"""
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d)\s+(::ffff:)?({host}\S+)\s+:?\s*%ASA"""
"""user\s*=\s*({first_name}\w+)\.({last_name}\w+)"""
"""user\s*=\s*((cn=({src_host}[^>,\s]+)(,[^>]+?dc=({domain}[^>,]+))?)|({email_address}[^@\s"]+@[^@\s"]+))"""
"""user\s*=\s*(({domain}[^\\s]+)\\+)?({user}[^=\s"]+)\s"""
"""server\s*=\s*(::ffff:)?({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""%(FTD|ASA)(-\w+)?-\d+-({event_code}\d+)[:\s]+({event_name}[^:]+)\s"""
]
DupFields = [
  "user->account"
]
ParserVersion = "v1.0.0"


}
```