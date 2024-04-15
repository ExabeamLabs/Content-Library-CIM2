#### Parser Content
```Java
{
Name = "namespacerdirectory-nrd-xml-group-member-add-success-memberadd-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Namespace rDirectory"
    Product = "Namespace rDirectory"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "rdirectorymodify group:"
      "modified by:"
      "[member] add:"
    ]
    Fields = [
      "(?i)SystemTime=\\'({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<]+)"
      "(?i)Modified by:({user}.+?)\\s+(\\(.+?\\))?\\s+\\(({domain}[^\\/)]+)"
      "(?i)Credentials:({account_domain}[^\\\\]+)\\\\+([^\\s.]+\\.)*({account}[^\\s.]+)"
      "(?i)Group:({group_name}.+?)\\s+\\(({group_domain}[^\\/)]+)"
      "(?i)\\[Member\\]\\s*Add:CN=({account_name}[^,]+)"
      "(?i)\\[Member\\]\\s*Add:({user_dn}CN=.+?,({user_ou}OU.+?DC=[\\w-]+))"
      "(?i)\\[Member\\]\\s*Add:(?:CN|({account_name}[^<]+))"
    ]
  

}
```