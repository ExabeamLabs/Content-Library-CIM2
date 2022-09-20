#### Parser Content
```Java
{
Name = microsoft-o365-sk4-app-activity-success-movetofolder
  Vendor = Microsoft
  Product = Office 365
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = ["""New-InboxRule""" , """MoveToFolder"""]
  Fields = [
    """timestamp="({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""",
    """"CreationTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""",
    """MoveToFolder",.+?Value":"({target}[^\s"]+)""""
    """"ResultStatus":"({result}[^"]+)"""",
    """"ClientIP":"({src_ip}[^:]+):""",
    """({operation}MoveToFolder)"""",
    """additional_info="({additional_info}[^=]+?)(\s+\w+="|$)""",
    """msg=({additional_info}[^=]+?)\srequest=""",
    """user_email="({email_address}[^"@\s]+@({domain}[^"@\s]+))"""",
    """UserId":"({email_address}[^"\\]+@({domain}[^"]+))""",
    """app="({app}[^"]+)"""",
    """destinationServiceName =({app}.+?)\sdevice""",
    """UserId":"(\\.+)?\/({full_name}[^,\\"]+)\\"\s*on behalf""",
    """UserId":"(\\.+)?\/({last_name}[^,]+),\s*({first_name}[^\\"]+)\\"\s*on behalf"""
    """"SubjectOrBodyContainsWords":"({filter_key_words}[^"]+)"""
    """"Name":"MoveToFolder","Value":"({object}[^"]+?)\s*""""
  ]
  DupFields = ["domain->email_domain"]


}
```