#### Parser Content
```Java
{
Name = tripwire-t-cef-alert-trigger-success-filemodified
  Vendor = Tripwire Enterprise
  Product = Tripwire Enterprise
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """|Tripwire|Enterprise|""", """elementOIDLabel""" ]
  Fields = [
    """\|rt=({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d)""",
    """\|dvchost=({host}[^|]+)\|""",
    """\|duser=(?:not available|(({domain}[^\\]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))\|""",
    """\|Tripwire\|([^|]*\|){3}({alert_name}[^|]+)\|""",
    """\|cs2=({access}[^|]+)\|""",
    """\|cs3=({alert_type}[^|]+)\|""",
    """\|sproc=(?:not available|({process_path}[^|]+))\|""",
    """\|sproc=(?:not available|({process_dir}[^|]+)[\\\/]+[^\\\/]+)\|""",
    """\|sproc=(?:not available|([^|]+[\\\/]+)?({process_name}[^|]+))\|""",
    """\|fname=({file_path}[^|]+)\|""",
    """\|fname=({file_dir}[^|]+)[\\\/]+[^\\\/]+\|""",
    """\|fname=([^|]*[\\\/]+)?({file_name}[^\\\/|]+)\|""",
    """\|fname=[^|]+[\\\/]+[^\\\/|.]+\.({file_ext}[^\\\/|]+)\|""",
    """\|dhost=({dest_host}[^|]+)\|""",
    """\|cs1=({os}[^|]+) Server\|""",
    """\|cs6=(?:Unknown|({hash_type}[^|]+))\|""",
    """\|oldFileHash=(?:not available|({old_hash}[^|]+))\|""",
    """\|fileHash=(?:not available|({new_hash}[^|]+))\|"""
  ]
  ParserVersion = "v1.0.0"


}
```