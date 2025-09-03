#### Parser Content
```Java
{
Name = pan-ngfw-kv-network-traffic-success-end
Conditions = ["""type=TRAFFIC,""", """logset=Panorama,""", """subtype=end,""" ]
ParserVersion = "v1.0.0"

leef-paloalto-vpn-event-1.Fields}[
  """\|devTime=({time}\w{3}\s+\d+ \d\d\d\d \d\d:\d\d:\d\d \w+)\|"""
  """({result}(allow|deny))""",
  """PAN-OS Syslog Integration\|(?:({result}[^\|]+)\|){2}"""
  """cat=({category}[^\s|]+)"""
  """\|msg="*({event_name}[^\|"]+)"""
 
}
```