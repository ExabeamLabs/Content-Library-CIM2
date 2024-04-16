#### Parser Content
```Java
{
Name = cisco-ise-kv-app-activity-administrativeandoperationalaudit
  Vendor = Cisco
  Product = Cisco ISE
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """ CISE_Administrative_and_Operational_Audit """ ]
  Fields = [
    """(::ffff:)?({host}[^\s]+)\s*CISE_Administrative_and_Operational_Audit""",
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d\.\d\d\d)(\s[+-]\d\d:\d\d)?""",
# config_version_id is removed
    """AdminInterface=({admin_interface}[^,]+)""",
# operation_message_text is removed
# acs_instance is removed
# administrator_login is removed
    """({event_name}CISE_Administrative_and_Operational_Audit)""",
    """({result}success|failure)""",
# connection_requested is removed
    """NOTICE\s+({operation}.+?),\s+ConfigVersion"""
  ]
  ParserVersion = "v1.0.0"


}
```