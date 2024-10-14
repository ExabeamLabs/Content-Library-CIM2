#### Parser Content
```Java
{
Name = zeek-z-str-dhcp-traffic-success-dhcp
  Vendor = Zeek
  Product = Zeek 
  TimeFormat = "epoch_sec"
  Conditions = [ """/dhcp.log""" ]
  Fields = [
    """({time}\d{10})\.\d{6}\s+({connection_id}[^\s]+)\s+(?:-|(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\s]+))\s+(?:-|(({src_port}\d+?)|[^\s]+))\s+(?:-|(({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\s]+))\s+(?:-|(({dest_port}\d+?)|[^\s]+))\s+(?:-|({src_mac}[^\s]+))\s+(?:-|({assigned_ip}[^\s]+))\s+(?:-|({lease_time}[^\s]+))\s+(?:-|({transaction_id}[^"]+)?)\s*"""
]
  DupFields = ["transaction_id->trans_id"]
  ParserVersion = "v1.0.0"


}
```