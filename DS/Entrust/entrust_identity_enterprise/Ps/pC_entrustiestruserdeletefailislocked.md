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
"""({additional_info}Maximum authentication.+?is locked.)"""
"""User (({email_address}[^\@\s]+@[^\s]+)|(({domain}[^\\\/]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)) is locked."""
]
ParserVersion = "v1.0.0"


}
```