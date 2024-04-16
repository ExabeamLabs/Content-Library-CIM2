#### Parser Content
```Java
{
Name = bitglass-casb-cef-alert-trigger-success-filelink
  ParserVersion = v1.0.0
  Vendor = Bitglass
  Product = Bitglass CASB
  TimeFormat = "dd MMM yyyy HH:mm:ss"
  Conditions = [ """"action":"Alert"""", """"patterns":"""", """"application":"""", """"filelink":"""", """ api.bitglass.com """ ]
  Fields = [
    """CEF:([^\|]*\|){6}({alert_severity}[^\|])"""
    """"time":"({time}\d\d\s\w{1,3}\s\d\d\d\d\s\d\d:\d\d:\d\d)"""",
    """"patterns":"({alert_name}[^"]+)"""",
    """"status":"({alert_type}[^"]+)"""",
    """"folder":"({target}[^"]+)"""",
    """"filename":"({file_name}[^"]+?(\.({file_ext}[^"]+))?)"""",
    """"application":"({process_path}[^"]+)"""",
    """"owner":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
    """"filelink":"({additional_info}[^"]+)""""
  ]


}
```