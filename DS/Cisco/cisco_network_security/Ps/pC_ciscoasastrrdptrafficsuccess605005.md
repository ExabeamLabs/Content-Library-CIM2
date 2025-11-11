#### Parser Content
```Java
{
Name = "cisco-asa-str-rdp-traffic-success-605005"
Vendor = "Cisco"
Product = Cisco Network Security
TimeFormat = ["MMM dd yyyy HH:mm:ss", "MMM dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
Conditions = [
  """Login permitted from"""
  """-605005"""
  """%ASA-"""
]
Fields = [
  """({time}\d{4}\-\d{2}\-\d{2}T\d{2}:\d{2}:\d{2}\.\d+((\+|\-)\d\d:\d\d)?)\s+""",
"""\s(({host}[\w.\-]+))\s+([-\s:]+)?%ASA""",
  """({time}[a-zA-Z]{3}\s\d{2}\s\d{0,4}\s*\d{2}:\d{2}:\d{2}).*?(ASA|FTD)"""
  """%(FTD|ASA)(-\w+)?-({priority}\d+)-({event_code}\d+)"""
  """\w+ \d+ \d+:\d+:\d+ ({host}[\w.\-]+)\s+:\s+%ASA"""  
  """Login permitted from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))([:\/]({src_port}\d+))?"""
  """Login permitted from .+? to ({domain}[^:]+)"""
  """Login permitted from .+?:({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """Login permitted from .+? to .+?/({auth}.+?) for user"""
  """user "+(({domain}[^\\\/"]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """Login permitted from .+? to .+?/({protocol}.+?) for user"""
]
ParserVersion = "v1.0.0"


}
```