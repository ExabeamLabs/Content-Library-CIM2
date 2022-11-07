#### Parser Content
```Java
{
Name = mcafee-sncasb-kv-app-success-mvision
  Vendor = McAfee
  Product = Skyhigh Networks CASB
  ParserVersion = "v1.0.0" 
  TimeFormat = "MMM dd yyyy HH:mm:ss.SSS z"
  Conditions = [  """|McAfee|MVISION Cloud|""", """usrName =""", """devTime=""", """cat="""]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}[^\s]+)""",
    """devTime=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d\.\d+ \w+)""",
    """src=(0\.0\.0\.0|({src_ip}[\da-fA-F:\.]+))""",
    """response=\[({result}[^\]\s]+)""",
    """dst=({dest_host}[^\s]+)""",
    """usrName =(({email_address}[^@]+@[^@\s]+)|({user}[^\s]+))\s+\w+=""",
    """activityName =\[({operation}[^\]\s]+)""",
    """userInfoFirstName =({first_name}[^\s]+)""",
    """userInfoLastName =({last_name}[^\s]+)""",
    """objectName =({object}[^=]+?)\s+\w+=""",
    """auditEventTypeEventTypeName =({operation}[^=]+?)\s+\w+=""",
    """serviceNames=\[({app}[^\]]+)""",
    """({app}MVISION Cloud)""",
    """eventInfo=({additional_info}[^=]+?)\s+\w+="""
  ]


}
```