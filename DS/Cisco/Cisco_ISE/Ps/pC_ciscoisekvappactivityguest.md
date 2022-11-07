#### Parser Content
```Java
{
Name = cisco-ise-kv-app-activity-guest
  ParserVersion = "v1.0.0"
  Vendor = Cisco
  Product = Cisco ISE
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [""" CISE_Guest """]
  Fields = [
    """({host}\S+) ({event_name}CISE_Guest) (\S+\s+){3}({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)""",
    """\sUserName =({user}[^,;@\s]+?)(,|;)""",
    """\sUserName =({email_address}[^,;@\s]+@[^,;@\s]+?)(,|;)""",
# auditsessionid is removed
# guestusername is removed
    """IdentityGroup=({identity_group}[^,]+?),""",
    """(?i)(MacAddress)=({src_mac}[^,]+?),""",
# ipaddress is removed
# usertype is removed
    """Calling-Station-ID=({calling_station_id}[^,\s]+),""",
# called_station_id is removed
  ]


}
```