#### Parser Content
```Java
{
Name = unix-ad-kv-endpoint-notification-netfiltercfg
    Vendor = Unix
    Product = Unix Auditd
    TimeFormat = ["yyyy-MM-dd HH:mm:ss", "MMM dd HH:mm:ss"]
    Conditions = ["""audit""", """NETFILTER_CFG"""]
    Fields = [
      """\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log({=host}[\w.\-]+)\s)?"""
      """msg=({event_name}.+?)\s+(\w+=|$)""",
      """type=({event_category}.+?)\s+(\w+=|$)""",
      """table=({table}.+?)\s+(\w+=|$)""",
# family is removed
# entries is removed
    ]
    DupFields = [ "host->dest_host" ]
	ParserVersion = "v1.0.0"


}
```