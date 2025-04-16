#### Parser Content
```Java
{
Name = cybereason-cr-cef-alert-trigger-success-malops
  ParserVersion = v1.0.0
  Vendor = Cybereason
  Product = Cybereason
  TimeFormat = ["epoch", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [ """destinationServiceName =Cybereason""", """"username":""", """"name":""", """dproc=Malops""" ]
  Fields = [
    """CEF:([^\|]*\|){6}({alert_severity}[^\|])"""
    """"detectionType":\{[^=]+?"values":\["({alert_type}[^"]+)"""",
    """"Machine"[^\]]+"name":"({dest_host}[^"]+)"""",
    """"User"[^\]]+"name":"(({domain}[^\\]+)?[\\]+)?(system|({user}[\w\.\-\!\#\^\~]{1,40}\$?)?)?""",
    """"creationTime":\{[^]}]+?"values":\["({time}\d{13})"""",
    """"malopLastUpdateTime":\{[^]}]+?"values":\["({time}\d{13})""""
    """\s+({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d{3}Z)\s+"""
    """"message":"({additional_info}[^"]+)"""",
    """"elementDisplayName":[^\]]+"values":\["({alert_name}[^"]+)"""",
    """"malopActivityTypes":\{"[^]}]+?"values":\["({threat_category}[^"]+)"""",
  ]


}
```