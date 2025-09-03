#### Parser Content
```Java
{
Name = unix-unix-mix-endpoint-logout-sessionclosed
  Vendor = Unix
  Product = Unix
  ParserVersion = "v1.0.0"
  TimeFormat = ["MMM dd HH:mm:ss", "yyyy-MM-dd HH:mm:ss"]
  Conditions = [ """ pam_unix""", """session closed for user """ ]
  Fields = [
    """\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d (::ffff:)?({host}(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({src_host}[\w\-.]+))) ({event_code}\S+)""",
    """({time}\w+\s+\d+\s+\d+:\d+:\d+)\s+(::ffff:)?({host}(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({src_host}[\w\-.]+)))\s+""",
    """({event_code}[^\s:\[]+?)(\[[^\]]*\])?:\s*pam_unix""",
    """%FTD-({priority}\d+)-({event_code}\d+)""",
    """(({event_name}session closed for user)\s*(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))""",
  ]


}
```