#### Parser Content
```Java
{
Name = vectra-cd-kv-app-notification-account
  ParserVersion = v1.0.0
  Vendor = Vectra
  Product = Vectra Cognito Detect
  TimeFormat = "epoch_sec"
  Conditions = [ """vectra_standard_account""", """: ACCOUNT """, """account@"""]
  Fields = [
        """({host}[\w.\-]+)\s+vectra_standard_account""",
        """\saccountName ="({email_address}({user}[^"@]+)[^"]*?)"""",
        """\sthreat="({object}[^"]+)""",
        """\scategory="({event_name}[^"]+)""",
        """\sUTCTime="({time}\d{10})"""
  ]
  DupFields = [ "object->threat" ]


}
```