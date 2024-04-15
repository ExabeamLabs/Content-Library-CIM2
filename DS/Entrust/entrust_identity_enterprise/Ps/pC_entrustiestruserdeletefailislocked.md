#### Parser Content
```Java
{
Name = "entrust-ie-str-user-delete-fail-islocked"
Vendor = "Entrust"
Product = "Entrust Identity Enterprise"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""" Maximum authentication attempts exceeded. """
""" is locked."""
]
Fields = [
"""\[({time}\d{4}-\d\d-\d\d \d\d:\d\d:\d\d)(\]|,\]|,\d+\])"""
"""({event_description}Maximum authentication.+?is locked.)"""
"""User (({email_address}[^\@\s]+@[^\s]+)|(({domain}[^\\\/]+)[\\\/]+)?({user}[^\s]+)) is locked."""
]
ParserVersion = "v1.0.0"


}
```