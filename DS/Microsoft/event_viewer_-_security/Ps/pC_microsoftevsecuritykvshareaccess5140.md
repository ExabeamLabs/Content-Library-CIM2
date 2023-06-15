#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-share-access-5140
    Vendor = Microsoft
    Product = Event Viewer - Security
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSZ"
    Conditions = [ """Exabeam Windows 5140""", """summary_windows_5140_data""" ]
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+[+-]\d+)""",
      """({event_code}5140)""",
      """({access}Read)""",
      """summary_windows_5140_data="+\d+:\d+:\d+\s*\d+-\d+-\d+:::({host}[^:::]+)?:::({login_id}[^:::]+)?:::({user}[^:::]+)?:::({domain}[^:::]+)?:::({file_type}[^:::]+)?:::({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))??:::({share_name}[^:::]+)?:::(?:\s*|({share_path}({d_parent}.*?)({d_name}[^\\]+?))(\\+)?)?"""
    ]
      DupFields=[ "host->dest_host" ]


}
```