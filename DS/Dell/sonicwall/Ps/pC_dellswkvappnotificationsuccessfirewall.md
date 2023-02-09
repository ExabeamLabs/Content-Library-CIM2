#### Parser Content
```Java
{
Name = dell-sw-kv-app-notification-success-firewall
  Vendor = Dell
  Product = Sonicwall
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """id=firewall""", """msg="Interface statistics report""" ]
  Fields = [
    """\stime="({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)""",
    """\smsg="({event_name}[^"]+)""",
# serial_number is removed
    """\sc=({category_id}\d+)""",
    """\sm=({message_id}\d+)""",
# message_count is removed
    """\sif=({interface}.+?)(\s+\w+=|\s*$)""",
# unicast_packets_in is removed
# broadcast_packets_in is removed
    """\sbytesRx=({bytes_in}\d+)""",
# unicast_packets_out is removed
# broadcast_packets_out is removed
    """\sbytesTx=({bytes_out}\d+)""",
  ]


}
```