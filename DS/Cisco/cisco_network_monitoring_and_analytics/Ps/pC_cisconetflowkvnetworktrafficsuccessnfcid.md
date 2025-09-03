#### Parser Content
```Java
{
Name = "cisco-netflow-kv-network-traffic-success-nfc-id"
  ParserVersion = "v1.0.0"
  Vendor = "Cisco"
  Product = "Cisco Network Monitoring and Analytics"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
    """ t_int="""
    """ nfc_id="""
  ]
  Fields = [
    """\w+ \d\d \d\d:\d\d:\d\d ({host}[\w.\-]+)"""
    """\ssrc_ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """\ssrc_host=(unknown|({src_host}.+?))(\s+\w+=|\s*$)"""
    """\ssrc_port=({src_port}\d+)"""
    """\sdest_ip=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """\sdest_host=(unknown|({dest_host}.+?))(\s+\w+=|\s*$)"""
    """\sdest_port=({dest_port}\d+)"""
    """\stcp_flag=\"({tcp_flags}[^\"]+)"""
    """\spackets_in=({packets_in}\d+)"""
    """\sbytes_in=({bytes_in}\d+)"""
    """\spackets_out=({packets_out}\d+)"""
    """\sbytes_out=({bytes_out}\d+)"""
    """\sprotocol=({protocol}\d+)"""
  ]
  DupFields = [
    "bytes_in->bytes"
    "packets_in->packets"
  ]


}
```