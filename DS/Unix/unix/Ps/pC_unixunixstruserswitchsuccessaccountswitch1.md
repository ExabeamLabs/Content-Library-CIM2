#### Parser Content
```Java
{
Name = unix-unix-str-user-switch-success-accountswitch-1
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = ["yyyy-MM-dd HH:mm:ss", "MMM dd HH:mm:ss"]
  Conditions = [""" su[""", """ on """, """: (to """ ]
  Fields = [
    """\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?"""
    """(T|\s)\d\d:\d\d:\d\d(\.?\S+)?\s+(::ffff:)?({host}[\w\.\-]+)?\s*({event_code}su)(\[\w+\])?:\s+\(to\s+({account}[^)]+)\)\s+(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+on""",
    """(T|\s)\d\d:\d\d:\d\d(\.?\S+)?\s+(::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.-]+))\s""",
    """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s+""",
  ]
  DupFields = [ "account->dest_user" ]


}
```