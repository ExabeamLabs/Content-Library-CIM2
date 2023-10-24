#### Parser Content
```Java
{
Name = symantec-dlp-kv-alert-trigger-success-riskseverity
  ParserVersion = v1.0.0
  Vendor = Symantec
  Product = Symantec DLP
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """, violatedPolicyRuleName: """, """,[CA Name: Risk Severity],""", """,[CA Name: SIFT Timestamp],""" ]
  Fields = [
    """\[CA Name: SIFT Timestamp\], \[CA value:\s*({time}\d+-\d+-\d+\s+\d+:\d+:\d+)""",
    """\[CA Name: Detection Server\], \[CA value:\s*({host}[\w\-.]+)""",
    """\[CA Name: First Name\], \[CA value:\s*(|({first_name}[^\]]+?))\s*\]""",
    """\[CA Name: Last Name\], \[CA value:\s*({last_name}[^\]]+)""",
    """\[CA Name: Account Name\], \[CA value:\s*({user}[\w\.\-]{1,40}\$?)""",
    """\[CA Name: Email\], \[CA value:\s*({email_address}[^\]\s@]+@[^\]\s@]+)""",
    """\[CA Name: Risk Severity\], \[CA value:\s*(|({alert_severity}[^\]]+?))\s*\]""",
    """, violatedPolicyRuleName:\s*({alert_name}[^\],]+?)\s*,""",
  ]
  DupFields = [ "alert_name->alert_type" ]


}
```