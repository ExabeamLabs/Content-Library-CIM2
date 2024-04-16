#### Parser Content
```Java
{
Name = infoblox-bddi-str-configuration-modify-zoneapplied
	ParserVersion = v1.0.0
    Vendor = Infoblox
    Product = BloxOne DDI
    TimeFormat = ["MMM dd HH:mm:ss", "dd-MMM-yyyy HH:mm:ss.SSS"]
    Conditions = [ """named[""", """: zone""" , """applied"""]
    Fields = [
      """\d\d:\d\d:\d\d ({host}\S+)""",
      """({time}\w+\s+\d+ \d+:\d+:\d+)"""
      """({time}\d\d-\w+-\d\d\d\d \d\d:\d\d:\d\d\.\d\d\d)""",
      """\sIN\s({dns_query_type}\w{1,5})\s([^\s]+)\s({dns_query}[^\s]+)\s(\d+)\s(\d+)\s([^\s]+)\s(\d+)\s(\d+)""",
# DL Fields are removed
    ]
  

}
```