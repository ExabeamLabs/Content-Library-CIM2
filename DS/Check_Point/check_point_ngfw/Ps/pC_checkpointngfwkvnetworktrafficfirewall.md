#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-network-traffic-firewall
Vendor = "Check Point"
Product = "Check Point NGFW"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [
  """ProductName: VPN-1 & FireWall-1;"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+((\+|\-)\d\d:\d\d)?)"""
  """({host}[\w.\-]+)\s+CPLogToSyslog:"""
  """\WOriginSicName:\s*CN=({host}[\w.\-]+),O="""
  """\WAction:\s*(|({action}[^;]+?));"""
  """\Wservice_id:\s*(|({protocol}[^;]+?));"""
  """\WIfDir:\s*(|({direction}[^;]+?));"""
  """\Wuser:\s*(|({user}[^\(\);]+?));"""
  """\Wuser:\s*({full_name}.+?)\s*\(({account}.+?)\)"""
  """\Wsrc:\s*(|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?);"""
  """\Wdst:\s*(|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?);"""
  """\Wxlatesrc:\s*(|({src_translated_ip}[a-fA-F\d.:]+));"""
  """\Wrule_name:\s*(|({rule}[^;]+?));"""
  """\WProductName:\s*(|({app}[^;]+?));"""
  """\Wsvc:\s*({dest_port}\d+)"""
  """\Wsport_svc:\s*({src_port}\d+)"""
]
DupFields = [
  "action->event_name"
]
ParserVersion = "v1.0.0"


}
```