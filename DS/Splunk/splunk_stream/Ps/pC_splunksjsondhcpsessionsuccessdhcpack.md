#### Parser Content
```Java
{
Name = splunk-s-json-dhcp-session-success-dhcpack
  Vendor = Splunk 
  Product = Splunk Stream
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """"opcode":"""", """ip:udp:dhcp""", """"giaddr":"""", """"flow_id":"""" ]
  Fields = [
    """"timestamp":"({time}[^"]+)"""",
    """"bytes":({bytes}\d+),""",
    """"bytes_in":({bytes_in}\d+),""",
    """"bytes_out":({bytes_out}\d+),""",
    """"dest_ip":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """"dest_mac":"({dest_mac}[^"]+)"""",
    """"dest_port":({dest_port}\d+),""",
    """"dns_server":\[({dns_ip_flow}[^\]]+)\]""",
    """"domain_name":\[({domain}[^\]]+)\]""",
    """"opcode":"({event_name}[^"]+)"""",
    """"router":\[({router_ip_flow}[^\]]+)\]""",
    """"src_ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"src_mac":"({src_mac}[^"]+)"""",
    """"src_port":({src_port}\d+),""",
    """"subnetmask":"({router_subnet}[^"]+)"""",
    """"transaction_id":({trans_id}[^,]+),""",
    """({protocol}dhcp)""",
    """"yiaddr":"({assigned_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
    """"ip_lease_time":({ip_lease_time}\d+),""",
    """"host_name":"({host}[^"]+)"""",
  ]
  ParserVersion = "v1.0.0"


}
```