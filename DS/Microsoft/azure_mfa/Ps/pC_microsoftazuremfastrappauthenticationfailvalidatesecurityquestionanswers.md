#### Parser Content
```Java
{
Name = microsoft-azuremfa-str-app-authentication-fail-validate-security-question-answers
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Azure MFA
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ pfsvc: """, """|validate_security_question_answers: user""", """updated authentication result.""", """callStatus = Undefined error code""" ]
  Fields = [
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s({host}[^\s]+)\spfsvc:""",
    """({event_name}validate_security_question_answers)""",
    """user\s+"?(({email_address}[^"@\s]+@[^"\s]+)|(({domain}[^\\\s]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """({additional_info}Undefined error code)"""
    ]


}
```