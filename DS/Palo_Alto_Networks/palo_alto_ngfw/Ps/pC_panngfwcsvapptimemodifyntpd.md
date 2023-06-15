#### Parser Content
```Java
{
Name = pan-ngfw-csv-app-time-modify-ntpd
  ParserVersion = v1.0.0
  Product = Palo Alto NGFW
  Conditions = [ """,SYSTEM,""", """,SYSTEM,ntpd,""" ]

pan-system-1 {
    Vendor = Palo Alto Networks
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """SYSTEM,([^,]+,){2}({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z),""",
      """SYSTEM[^"]+?({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)""",
      """SYSTEM,("[^"]*",|[^,]*,){18}({host}(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-\.]+)))""",
      """:\d\d:\d\d\s+({host}(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-\.]+)))\s""",
      """,({asset_id}\d+),SYSTEM,""",
      """({event_category}SYSTEM)""",
      """SYSTEM,({event_subtype}[^,]+),""",
      """SYSTEM,([^,]*,){9}({severity}[^,]+),""",
      """SYSTEM,(?:[^,]*,){10}"*({additional_info}[^",]+?)(?:\.*"|\.\s|\.*,|\s(\d{1,3}\.){3}\d{1,3}:\d+)""",
      """Private IP:\s?({src_translated_ip}[^,\s]+)""",
      """User\s*(name:)?\s+({user}[\w.'\-\\$]+?)\.?(\s|,|"|$)""",
      """User\s*(name:)?\s+({email_address}[^@\s]+@[^\s,]+?)(\.\\"|\.")?,""",
      """Client OS( version)?:\s+({os}[^":]+)(,|\.)""",
      """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
      ]
    DupFields = ["host->dest_host"
}
```