#### Parser Content
```Java
{
Name = exabeam-search-json-app-activity-success-searchquery
    Product = Search
    Conditions = [""""Exabeam Audit Event"""", """"event_type":"dl-search-activity"""", """"activity":"Search query"""", """"app":"Exabeam Data Lake""""]
    Fields = ${EXAParsersTemplates.exa-events.Fields} [
      """query:\s*\[({query}[^]]+)\]"""
    ]
    DupFields = ["query->object"]
    ParserVersion = "v1.0.0"
  
exa-events = {
    Vendor = Exabeam
    Product = Advanced Analytics
    TimeFormat = "epoch"
    Fields = [
      """"time":({time}\d{13})""",
      """"host":"({host}[^"]+)""",
      """"src_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """"user":"((\[saml\])?({email_address}[^"@]+@[^"@]+)|({user}[^"\s]+))"""",
      """"activity":"({operation}[^"]+)""",
      """"additional_info":"({additional_info}.+?),?\s*"\}\}""",
      """"app":"({app}[^"]+)""",
    
}
```