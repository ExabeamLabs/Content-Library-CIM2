#### Parser Content
```Java
{
Name = "ca-pamsc-xml-user-password-read-commandinitiator-tl"
    ParserVersion = "v1.0.0"
    Vendor = "CA Technologies"
    Product = "CA Privileged Access Manager Server Control"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Conditions = [
      " pam - metric detail "
      "<type>viewaccountpassword</type>"
      "<k>commandinitiator</k>"
    ]
    Fields = [
      "(?i)({time}\\d{4}-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\+\\d\\d:\\d\\d)\\s+({host}[^\\s]+)\\s"
      "(?i)<type>({operation}[^<]+)<"
      "(?i)<k>commandInitiator<\\/k><v>({object}[^<]+)<"
      "(?i)<k>adminUserID<\\/k><v>(({email_address}[^@<]+?@[^<]+?)|({user}[^<]+?))<\\/v>"
      "(?i)<k>reason<\\/k><v>({failure_reason}[^<]+)<"
      "(?i)<k>reasonDetails<\\/k><v>({additional_info}[^<]+)<"
      "(?i)<k>TargetAccount.userName<\\/k><v>({dest_user}[^<]+)<"
      "(?i)<k>TargetApplication.name<\\/k><v>({target}[^<]+)<"
      "(?i)<k>authentication<\\/k><v>({auth_method}[^<]+)<"
    ]
  

}
```