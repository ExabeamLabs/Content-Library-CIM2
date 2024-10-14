#### Parser Content
```Java
{
Name = citrix-cvapps-json-endpoint-logout-desktopstop
  ParserVersion = v1.0.0
  Vendor = Citrix
  Product = Citrix Virtual Apps
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"event":"desktop-stop"""", """"system":"Citrix-XenApp"""", """"clientname":"""", """"servername":"""" ]
  Fields = [
    """exa_json_path=$.enddate,exa_field_name=time""",
    """exa_json_path=$.username,exa_regex=(({email_address}[^@"]+@[^\."]+\.[^"]+)|(({domain}[^\\"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """exa_regex=({event_name}desktop-stop)""",
    """exa_json_path=$.servername,exa_field_name=host""",
    """exa_json_path=$.clientaddress,exa_regex=(0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """exa_json_path=$.clientname,exa_field_name=src_host""",
    """exa_json_path=$.clientplatform,exa_field_name=os""",
    """exa_json_path=$.connectedviaipaddress,exa_regex=({src_translated_ip}[a-fA-F:\d.]+)"""
  ]


}
```