#### Parser Content
```Java
{
Name = pan-ngfw-csv-app-activity-general
  ParserVersion = v1.0.0
  Product = Palo Alto NGFW
  Conditions = [ """,SYSTEM,""", """,SYSTEM,general,""" ]
  Fields=${DLPaloAltoParsersTemplates.pan-system-1.Fields}[
    """SYSTEM,({event_subtype}[^,]+),([^,]*,){3}([^,]+),""", #dl field removed
# job_id is removed
    """User:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
# commit_description is removed
    """({event_name}Failed password for root)\s+\w+\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s+port\s+({src_port}\d+)\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  ]

pan-system-1 {
    Vendor = Palo Alto Networks
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","MMM dd yyyy HH:mm:ss","yyyy/MM/dd HH:mm:ss"]
    Fields = [
      """SYSTEM,([^,]+,){2}({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z),""",
      """SYSTEM[^"]+?({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)""",
      """SYSTEM,("[^"]*",|[^,]*,){18}({host}[\w\-\.]+),""",
      """:\d\d:\d\d\s+({host}[\w\-\.]+)\s""",
      """,({asset_id}\d+),SYSTEM,""",
      """({event_category}SYSTEM)""",
      """SYSTEM,({event_subtype}[^,]+),""",
      """SYSTEM,([^,]*,){9}({severity}[^,]+),""",
      """SYSTEM,(?:[^,]*,){10}"*\s*({additional_info}[^",]+?)(?:\.*"|\.\s|\.*,|\s(\d{1,3}\.){3}\d{1,3}:\d+)""",
      """Private IP:\s?({src_translated_ip}[^,\s]+)""",
      """User\s*(name:)?\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\.?(\s|,|"|$)""",
      """User\s*(name:)?\s+({email_address}[^@\s]+@[^\s,]+?)(\.\\"|\.")?,""",
      """Client OS( version)?:\s+({os}[^":]+)(,|\.)""",
      """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
      """,({serial_num}\d+),SYSTEM,"""
      """,SYSTEM,([^,]*,){10}("[^"]+")?,([^,]*,){7}({device_name}({host}[^",]+))"""
      
}
```