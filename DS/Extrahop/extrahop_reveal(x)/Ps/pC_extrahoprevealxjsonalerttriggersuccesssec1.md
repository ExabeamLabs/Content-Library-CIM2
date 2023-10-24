#### Parser Content
```Java
{
Name = extrahop-revealx-json-alert-trigger-success-sec-1
  Vendor = Extrahop
  Product = Extrahop Reveal(x)
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """categories""", """sec.""", """"extrahop"""", """"event":""", """title"""]
  Fields = [
    """"start_time":"({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)""",
    """"detection_id":({alert_id}\d+)""",
    """"title":"({alert_name}[^"]+)""",
    """"categories":"({alert_type}[^"]+)""",
    """"risk_score":({original_risk_score}\d+)""",
    """"object":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))
?",[^,]+?ipaddr""",
    """"hostname":"({src_host}[\w.-]+)"""
    ]
    ParserVersion = "v1.0.0"


}
```