#### Parser Content
```Java
{
Name = cylance-protect-json-alert-trigger-detection
  ParserVersion = v1.0.0
  Vendor = Cylance
  Product = Cylance PROTECT
  ExtractionType = json
  TimeFormat = ["MM/dd/yyyy hh:mm:ss a","M/dd/yyyy hh:mm:ss a"]
  Conditions = [ """The Cosmopolitan of Las Vegas""", """Background Detection""", """"Last Reported User":""" ]
  Fields = [
    """exa_json_path=$.Created,exa_field_name=time"""
    """exa_json_path=$.['Device Name'],exa_field_name=host"""
    """exa_json_path=$.['IP Addresses'],exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.['Last Reported User'],exa_regex=(({domain}[^\\\/,]+)?[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
    """exa_json_path=$.['Serial Number'],exa_field_name=alert_id"""
    """exa_json_path=$.Policy,exa_field_name=alert_name"""
    """exa_json_path=$.['Background Detection'],exa_field_name=direction"""
# is_online is removed
# offline_date is removed
# online_date is removed
    """exa_json_path=$.Zones,exa_field_name=zone"""
  ]


}
```