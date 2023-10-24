#### Parser Content
```Java
{
Name = "bitglass-casb-json-file-write-success-uploaded"
  Vendor = "Bitglass"
  Product = "Bitglass CASB"
  TimeFormat = "dd MMM yyyy HH:mm:ss"
  Conditions = [
    """, Uploaded"""
    """ api.bitglass.com """
  ]
  Fields = [
    """"time":\s*"({time}\d+ \w+ \d\d\d\d \d\d:\d\d:\d\d)""",
    """"instancename":\s*"({host}[^"]+)"""",
    """"user":\s*"(({user}[\w\.\-]{1,40}\$?)"|({full_name}[^",]+))""",
    """"email":\s*"({email_address}[^"]+)"""",
    """"device":\s*"({os}[^"]+)"""",
    """"application":\s*"({app}[^"]+)"""",
    """"ipaddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"activity":\s*"({access}[^"]+)",""",
    """"filename":\s*"({src_file_name}[^"]+?(\.({file_ext}[^."]+))?)",""",
    """"useragent":\s*"({user_agent}.+?)",""",
    """"url":\s*"({file_url}.+?)",""",
  ]
  ParserVersion = "v1.0.0"
  DupFields = [ "src_file_name->file_name" ]


}
```