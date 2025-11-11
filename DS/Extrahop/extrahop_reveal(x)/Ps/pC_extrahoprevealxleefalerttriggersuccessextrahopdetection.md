#### Parser Content
```Java
{
Name = "extrahop-revealx-leef-alert-trigger-success-extrahopdetection"
  Vendor = "Extrahop"
  Product = "Extrahop Reveal(x)"
  TimeFormat = [ "MMM dd yyyy HH:mm:ss", "MMM dd yyyy HH:mm:ss Z", "yyyy-MM-dd'T'HH:mm:ss.SSSZ" ]  
  Conditions = [ """LEEF:""", """|ExtraHop|Reveal""", """|extrahop-detection|""", """categories=""", """title=""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+-\d+:\d+)\s*({host}[\w.-]+)\s"""
    """\Wstart_time=({time}\w{3} \d\d \d\d\d\d \d\d:\d\d:\d\d [+-]\d\d\d\d)"""
    """\Wdesc=({alert_description}.+?)\s*([¦|]\w+=|$)"""
    """\Woffender_ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """\Wvictim_ip=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """\Wtitle=({alert_name}.+?)\s*([¦|]\w+=|$)"""
    """\Wdet_url=({url}.+?)\s*([¦|]\w+=|$)"""
    """\Wrisk_score=({alert_severity}\d+)"""
    """\Wrisk_score=({original_risk_score}\d+)"""    
    """\Wcategories=({alert_type}.+?)\s*([¦|]\w+=|$)"""
  ]
  ParserVersion = "v1.0.0"


}
```