#### Parser Content
```Java
{
Name = ca-pamsc-xml-user-password-read-commandinitiator
  ParserVersion = v1.0.0
  Vendor = CA Technologies
  Product = CA Privileged Access Manager Server Control
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """ pam - metric DETAIL """, """<type>viewAccountPassword</type>""", """<k>commandInitiator</k>""" ]
  Fields = [
    """({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\+\d\d:\d\d)\s+({host}[^\s]+)\s""",
    """<type>({operation}[^<]+)<""",
    """<k>commandInitiator<\/k><v>({object}[^<]+)<""",
    """<k>adminUserID<\/k><v>(({email_address}[^@<]+?@[^<]+?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))<\/v>""",
    """<k>reason<\/k><v>({result_reason}[^<]+)<""",
    """<k>reasonDetails<\/k><v>({additional_info}[^<]+)<""",
    """<k>TargetAccount.userName<\/k><v>({dest_user}[^<]+)<""",
    """<k>TargetApplication.name<\/k><v>({target}[^<]+)<""",
    """<k>authentication<\/k><v>({auth_method}[^<]+)<""",
  ]


}
```