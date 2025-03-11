#### Parser Content
```Java
{
Name = cisco-mma-kv-network-traffic-firewall-1
  Vendor = "Cisco"
  Product = Cisco Network Security
  TimeFormat = "epoch_sec"
  Conditions = [ """firewall src=""", """ dst=""", """ protocol=""", """ pattern:""" ]
  Fields = [
    """\s({time}\d{10})\.\d+\s+({host}[\w.\-]+)\s+\w*firewall\s"""
    """\d\d:\d\d:\d\d ({host}[\w.\-]+)\s+\d+\s+({time}\d+)\.\d+ """
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s"""
    """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s"""
    """\sprotocol=({protocol}\w+)\s"""
    """\ssport=({src_port}\d+)"""
    """\sdport=({dest_port}\d+)"""
    """\smac=({src_mac}[a-fA-F\d.:]+)"""
    """\spattern:\s*({result}\d|[\w\s]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```