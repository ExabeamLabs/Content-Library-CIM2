#### Parser Content
```Java
{
Name = "cisco-fp-str-network-traffic-success-sip"
  ParserVersion = "v1.0.0"
  Vendor = "Cisco"
  Product = Cisco Network Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
   """%FTD"""
   """Pre-allocate SIP NOTIFY"""
  ]
  Fields = [
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
    """({time}\d+-\d+-\d+T\d+:\d+:\d+)"""
    """from ({src_interface}\w+):({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})(\/({src_port}\d{1,5}))?"""
    """to ({dest_interface}\w+):({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\/*(?:({dest_port}\d+))?"""
    """between ({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}) and ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """({event_name}Pre-allocate SIP NOTIFY TCP secondary channel)"""
    """for VPNDECRYPTED:({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\/({src_port}\d+)"""
  ]


}
```