#### Parser Content
```Java
{
Name = "namespacerdirectory-nrd-xml-ds_object-activity-success-modifyuser-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Namespace rDirectory"
    Product = "Namespace rDirectory"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "rdirectorymodify user:"
      "modified by:"
    ]
    Fields = [
      "(?i)SystemTime=\\'({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<]+)"
      "(?i)Modified by:({user}.+?)\\s+(\\(.+?\\))?\\s+\\(({domain}[^\\/)]+)"
      "(?i)Credentials:({account_domain}[^\\\\]+)\\\\+([^\\s.]+\\.)*({account}[^\\s.]+)"
      "(?i)rdirectoryModify.+?\\(.+?\\)\\[({attribute}[^\\]]+)"
      "(?i)rdirectoryModify.+?\\(.+?\\)\\[.+?\\]\\s*Add:({new_attribute}.+?)(\\s*To:|<)"
      "(?i)rdirectoryModify.+?\\(.+?\\)\\[.+?\\]\\s*Change:({old_attribute}.+?)\\s*To:"
      "(?i)rdirectoryModify.+?\\(.+?\\)\\[.+?\\].+?To:({new_attribute}[^<\\[]+)"
      "(?i)rdirectoryModify User:({object}.+?)\\s*\\("
    ]
  

}
```