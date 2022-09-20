#### Parser Content
```Java
{
Name = unix-ad-kv-endpoint-notification-netfiltercfg
    Vendor = Unix
    Product = Unix Auditd
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = ["""audit""", """NETFILTER_CFG"""]
    Fields = [
      """msg=({event_name}.+?)\s+(\w+=|$)""",
      """type=({event_category}.+?)\s+(\w+=|$)""",
      """table=({table}.+?)\s+(\w+=|$)""",
# family is removed
# entries is removed
    ]
	ParserVersion = "v1.0.0"


}
```