#### Parser Content
```Java
{
Name = pan-ngfw-kv-network-traffic-success-packetlog
	ParserVersion = v1.0.0
    Vendor = Palo Alto Networks
    Product = Palo Alto NGFW
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
    Conditions = [ """packet_log""", """as_name=""", """as_num=""", """direction=""" ]
    Fields = [
      """packet_log: ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}(-|\+)\d{4})"""
      """\saction=({action}.*?)(,\s\w+=|$)"""
      """\sproto=({protocol}.*?)(,\s\w+=|$)"""
      """\sdirection=({direction}.*?)(,\s\w+=|$)"""
      """\sreason=({additional_info}.*?)(,\s\w+=|$)"""
      """\ssrc=(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))(,\s\w+=|$)"""
      """\sdst=(({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?))(,\s\w+=|$)"""
      """\ssrc_port=({src_port}\d+)"""
      """\sdst_port=({dest_port}\d+)"""
    ]
  

}
```