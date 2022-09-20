#### Parser Content
```Java
{
Name = infoblox-nios-cef-app-activity-esm
  Vendor = Infoblox
  Product = NIOS
  ParserVersion = v1.0.0
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|McAfee|ESM|""", """Infoblox_NIOS """, """nitroUniqueId=""" ]
  Fields = [
    """({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s+CEF:"""
    """\srt=({time}\d+)""",
    """\seventId=({event_code}\d+)""",
# nitro_unique_id is removed
# device_external_id is removed
# device_translated_address is removed
    """\sexternalId=({external_id}[^\s\=]+)""",
    """\scat=({category}.+?)\s+(\w+=|$)""",
# nitro_norm_id is removed
# device_direction is removed
# nitro_trust is removed
# nitro_app_id is removed
    """\ssntdom=({domain}[^\s\=]+)""",
        """\sshost=(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w\-.]+))""",
# nitro_norm_id is removed
    """\ssrc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sdst=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sdmac=({dest_mac}[a-fA-F\d.:]+)""",
    """\|Infoblox_NIOS DHCP ({operation}[^\|]+)""",
    """CEF:[^\|]+\|([^\|]*\|){4}({event_name}[^\|]+)""",
  ]


}
```