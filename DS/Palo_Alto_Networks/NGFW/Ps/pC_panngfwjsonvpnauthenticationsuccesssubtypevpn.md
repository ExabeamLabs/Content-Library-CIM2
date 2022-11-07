#### Parser Content
```Java
{
Name = pan-ngfw-json-vpn-authentication-success-subtypevpn
 Conditions = [ """"LogType":"SYSTEM"""", """"Subtype":"vpn"""" ]
 Fields = ${DLPaloAltoParserTemplates.json-pan-system.Fields}[
   """({event_name}vpn)"""
 ]

json-pan-system = {
  Vendor = Palo Alto Networks
  Product = NGFW
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Fields = [
    """"EventTime":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\dZ)""",
    """"LogSourceName":"({host}[^"]+)""",
    """({event_category}SYSTEM)""",
    """"Subtype":"({subtype}[^"]+)"""",
    """"VendorSeverity":"({severity}[^"]+)"""",
    """"EventDescription":"({additional_info}[^"]+?)\s*"""",
    """"SourceIP":"({src_ip}[A-Fa-f.:\d]+)""",
    """"SourceUser":"({email_address}[^@]+@[^"]+)"""
    
}
```