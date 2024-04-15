#### Parser Content
```Java
{
Name = "namespacerdirectory-nrd-xml-user-create-success-createuser-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Namespace rDirectory"
    Product = "Namespace rDirectory"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "rdirectorycreate user:"
      "modified by:"
    ]
    Fields = [
      "(?i)SystemTime=\\'({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<]+)"
      "(?i)Modified by:({user}.+?)\\s+(\\(.+?\\))?\\s+\\(({domain}[^\\/)]+)"
      "(?i)User:({account_name}.+?)\\s+\\(({account_domain}[^\\/)]+)"
      "(?i)\\[Principal Name\\]\\s*Add:({account_name}[^@]+)(@({account_domain}[^.]+))?[^\\[]*\\["
      "(?i)Credentials:({account_domain}[^\\\\]+)\\\\+([^\\s.]+\\.)*({account}[^\\s.]+)"
      "(?i)Add:13=({user_type}\\d+)\\[Employee Type\\]"
    ]
  

}
```