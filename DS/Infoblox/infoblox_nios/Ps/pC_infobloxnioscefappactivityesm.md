#### Parser Content
```Java
{
Name = infoblox-nios-cef-app-activity-esm
  Vendor = Infoblox
  Product = Infoblox NIOS
  ParserVersion = v1.0.0
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|McAfee|ESM|""", """Infoblox_NIOS """, """nitroUniqueId=""" ]
  Fields = [
    """({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s+CEF:"""
    """\srt=({time}\d{13})""",
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
        """\sshost=(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[\w\-.]+))""",
# nitro_norm_id is removed
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\sdmac=({dest_mac}[a-fA-F\d.:]+)""",
    """\|Infoblox_NIOS DHCP ({operation}[^\|]+)""",
    """CEF:[^\|]+\|([^\|]*\|){4}({event_name}[^\|]+)""",
  ]


}
```