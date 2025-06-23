#### Parser Content
```Java
{
Name = "symantec-bcpa-mix-http-session-get"
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ssz" ]
  ParserVersion = "v1.0.0"
  Conditions = [ """ OBSERVED """, """ GET """, """ http""" ]
  Fields = ${BlueCoatParserTemplates.bluecoat-proxy.Fields}[
    """CreatedDate\\=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """timestamp\\="*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d\d:\d\d)\s*({host}[\w\-.]+)\s*"""
  ]


}
```