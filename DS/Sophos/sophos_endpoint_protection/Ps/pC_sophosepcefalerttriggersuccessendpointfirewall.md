#### Parser Content
```Java
{
Name = sophos-ep-cef-alert-trigger-success-endpointfirewall
  Conditions = [ """|sophos|sophos central|""", """|Event::Endpoint::WindowsFirewall::Blocked|""", """group=ENDPOINT_FIREWALL""" ]
  ParserVersion = "v1.0.0"

cef-sophos-dlp-alert = {
  Vendor = Sophos
  Product = Sophos Endpoint Protection
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """\Wrt=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """CEF:([^\|]*\|){4}({alert_type}[^\|]+)""",
    """CEF:([^\|]*\|){5}({alert_name}[^:.\|]+)(:\s({target}[^\|]+))?""",
    """CEF:([^\|]*\|){5}({additional_info}[^\|]+)""",
    """CEF:([^\|]*\|){5}({alert_name}[^:.\|]+).+?Username:\s*(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Rule names:\s*′({rule}[^′]+).+?Data Control action:\s*({result}[^\s]+)\s+File type:\s*({file_type}.+?)\s+File size:\s*({bytes}\d+)\s+({additional_info}.+?Destination path:\s*({target}.+?)\s+Destination type:[^\|]*)""",
    """CEF:([^\|]*\|){6}({alert_severity}[^\|]+)""",
    """\Wdhost=({src_host}[\w\-.]+)\s+(\w+=|$)""",
    """\Wsuser=((({dest_host}[^\s\\]+)\\+)({user}[\w\.\-\!\#\^\~]{1,40}\$?)|(n\/a|({full_name}[^\\]+?)))\s+(\w+=|$)""",
    """\Wid=({alert_id}[^\s]+)""",
  
}
```