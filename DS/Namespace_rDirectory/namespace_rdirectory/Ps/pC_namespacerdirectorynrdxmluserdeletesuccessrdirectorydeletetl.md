#### Parser Content
```Java
{
Name = "namespacerdirectory-nrd-xml-user-delete-success-rdirectorydelete-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Namespace rDirectory"
    Product = "Namespace rDirectory"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "rdirectorydelete:"
      "modified by:"
    ]
    Fields = [
      "(?i)SystemTime=\\'({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<]+)"
      "(?i)Modified by:({user}.+?)\\s+(\\(.+?\\))?\\s+\\(({domain}[^\\/)]+)"
      "(?i)Credentials:({account_domain}[^\\\\]+)\\\\+([^\\s.]+\\.)*({account}[^\\s.]+)"
      "(?i)Delete:\\s*({dest_user}.+?)\\s+\\(({dest_domain}[^\\/)]+)"
    ]
    DupFields = [
      "host->dest_host"
      "dest_user->account_name"
    ]
  

}
```