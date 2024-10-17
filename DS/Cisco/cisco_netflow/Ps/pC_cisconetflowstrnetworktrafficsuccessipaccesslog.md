#### Parser Content
```Java
{
Name = "cisco-netflow-str-network-traffic-success-ipaccesslog"
  ParserVersion = "v1.0.0"
  Vendor = "Cisco" 
  Product = "Cisco Netflow"
  TimeFormat = ["MMM dd yyyy HH:mm:ss","MMM d HH:mm:ss.SSS","MMM d HH:mm:ss.SSS z","MMM dd yyyy HH:mm:ss z","MMM  d HH:mm:ss.SSS","MMM  d HH:mm:ss.SSS z"]
  Conditions = [
    """6-IPACCESSLOG"""
    """ packet"""
  ]
  Fields = [
    """({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s+(\S+\s+){1,2}(\w+\s+\d+ \d\d:\d\d:\d\d(\.\d+)?)\s+\S+\s+\S+-6-IPACCESSLOG"""
    """({time}\w{3,4} \d{2} \d{4} \d{2}:\d{2}:\d{2})""",
    """\d{2}:\d{2}:\d{2}\s(\+\d+:\d+:\s)({host}[\w\-\.]+):""",
    """\slist\s\S+\s({result}\S+)\s(|({protocol}[^\.:]+)\s)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s*(\(({src_port}\d{1,5})\))?(\s(|({src_interface}\S+)))?(->\s({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\(({dest_port}\d{1,5})\)|\s\([^\)]+\))?,\s)?\d+\spacket"""
    """({packets}\d+)\s+packets?\s*$"""
    """:\s+({time}\w{3,4}\s*\d{1,2} \d{2}:\d{2}:\d{2}\.\d\d\d( \w{3})?)"""
    """\s({host}[\w.-]+)\:\s\w{3,4}\s*\d{1,2} \d{2}:"""
  ]


}
```