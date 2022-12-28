#### Parser Content
```Java
{
Name = unix-unix-str-network-traffic-fail-packetsendfail
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """%SSH-""", """-PACK_SND_FAIL: """, """Packet send failed""" ]
  Fields = [
    """s_id\s+="({dest_host}[^:]+):({dest_port}\d+)"""",
    """({event_name}Packet send failed)"""
  ]


}
```