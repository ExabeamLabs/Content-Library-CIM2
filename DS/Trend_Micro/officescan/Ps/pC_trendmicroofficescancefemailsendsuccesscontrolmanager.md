#### Parser Content
```Java
{
Name = trendmicro-officescan-cef-email-send-success-controlmanager
  ParserVersion = v1.0.0
  Vendor = Trend Micro
  Product = OfficeScan
  TimeFormat = "epoch"
  Conditions = [ """|Trend Micro|Control Manager|""" ]
  Fields = [
    """\Wrt=({time}\w+\s+\d+\s+\d+\s+\d+:\d+:\d+\s+\w+[\+\-]\d+:\d+)""",
    """\Wrt=({time}\d{13})""",
    """({host}[\w\-.]+)\s+CEF:""",
    """\Wdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\Wdvchost=({host}[^\s]+)""",
    """\WflexString1=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\s+\w+=""",
    """\WflexString2=({email_recipients}.+?)\s+\w+=""",
    """\WflexString2=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """\Wmsg=({email_subject}.+?)\s+\w+=""",
    """\WeventId=({alert_id}[^\s]+)""",
    """\Wcs1=({alert_name}.+?)\s+(\w+=|$)""",
    """\|Trend Micro\|Control Manager\|[^|]+\|[^|]+\|({alert_name}[^|]+)\|""",
    """\|Trend Micro\|Control Manager\|[^|]+\|[^|]+\|[^|]+\|({alert_severity}[^|]+)\|""",
    """\|Trend Micro\|([^|]+\|){2}({alert_type}[^|]+)""",
    """\Wfname=({email_attachment}.+?)\s+\w+=""",
    """\Wfname=[^=]+?(\.({file_ext}[^\s;\.\(\)]+))\s*(\(.*\))?\s+(\w+=|$)""",
    """\Wsuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+=""",
    """\WfilePath=({file_path}.+?)\s+\w+=""",
    """\Wdhost=({src_host}[\w\-.]+)""",
    """\Wdst=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wcs5=({action}.+?)\s+(\w+=|$)""",
    """\WdeviceFacility=({device_facility}.+?)\s+(\w+=|$)""",
    """\Wduser=(({domain}[^\\\s@]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(\w+=|$)""",
    """\Wduser=({email_address}[^\\\s@;,]+@[^\\\s@;,]+).*?\s+(\w+=|$)""",
    """\Wsuser=({last_name}[^,\(]+),\s*({first_name}[^,\)\=]+?)(\s*\([^\)]*\))?\s+(\w+=|$)""",
    """cn3Label=Security_Threat_Type.*?\Wcn3=({alert_severity}.+?)\s+(\w+=|$)""",
    """\sfileHash=({hash_md5}\S+)""",
  ]
  DupFields = [ "email_attachment->file_name" ]


}
```