#### Parser Content
```Java
{
Name = "microsoft-o365-xml-file-write-success-mailboxpermission-tl"
    Vendor = "Microsoft"
    Product = "Microsoft 365"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "succeeded"
      "><channel>"
      "mailboxpermission"
    ]
    Fields = [
      "(?i)SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^\\s\\<]+)"
      "(?i)><Message>Cmdlet ({result}[^\"\\\\\\.]+)"
      "(?i)<Channel>({app}.+?)<\\/Channel>"
      "(?i)AccessRights=\\{({additional_info}.+?)\\}\\}</Data><Data>.+?({full_name}[^\\\\\\/]+?)<\\/Data>"
      "(?i), User=({object}[^,]+)"
      "(?i)<Data>\\{Identity=({resource}[^,]+)"
      "(?i)<EventData><Data>({operation}.+?)<\\/Data>"
      "(?i)User=(({domain}[^\\\\]+)\\\\)?({user}[^\\s,]+)"
    ]
    ParserVersion = "v1.0.0"
  

}
```