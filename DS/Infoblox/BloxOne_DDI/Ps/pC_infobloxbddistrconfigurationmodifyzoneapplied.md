#### Parser Content
```Java
{
Name = infoblox-bddi-str-configuration-modify-zoneapplied
	ParserVersion = v1.0.0
    Vendor = Infoblox
    Product = BloxOne DDI
    TimeFormat = "dd-MMM-yyyy HH:mm:ss.SSS"
    Conditions = [ """named[""", """: zone""" , """applied"""]
    Fields = [
      """\d\d:\d\d:\d\d ({host}\S+)""",
      """({time}\d\d-\w+-\d\d\d\d \d\d:\d\d:\d\d\.\d\d\d)""",
      """\sIN\s({query_type}\w{1,5})\s([^\s]+)\s({web_domain}[^\s]+)\s(\d+)\s(\d+)\s([^\s]+)\s({expiry_time}\d+)\s(\d+)""",
# DL Fields are removed
    ]
  

}
```