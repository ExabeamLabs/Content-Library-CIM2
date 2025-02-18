#### Parser Content
```Java
{
Name = trendmicro-ds-leef-endpoint-activity-success-integritymonitor
    Vendor = Trend Micro
    Product = Deep Security
    TimeFormat = ["yyyy-MM-dd HH:mm:ss","yyyy-MM-dd'T'HH:mm:ssZ"]
    Conditions = [ """LEEF:""", """|Trend Micro|Deep Security Agent|""", """cat=Integrity Monitor""" ]
    Fields = [
      """\Wcat=({alert_type}.+?)\s*(\w+=|$)""",
      """\Wname=({alert_name}.+?)\s*(\w+=|$)""",
      """\Wsev=({alert_severity}\d+)""",
      """\Wdvc(host)?=({host}(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-\.]+)))\s*(\w+=|$)""",
      """\Wact=({action}.+?)\s*(\w+=|$)""",
      """\Wmsg=({additional_info}.+?)\s*(\w+=|$)""",
      """\WfilePath=({file_path}(|({file_dir}.*?))[\\\/]*({file_name}[^\\\/]+?))\s*(\w+=|$)""",
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)\s*[^\s]+\s*LEEF:"""
      """suser=(N\/A|({user}NT AUTHORITY|[\w\.\-\!\#\^\~]{1,40}\$?))"""
      """sproc=(N\/A|({process_path}({process_dir}[^=]*[\\\/]+)?)({process_name}[^=]+?))\sentityType="""
    ]
    DupFields = [ "alert_name->event_name" ]
  ParserVersion = "v1.0.0"
  

}
```