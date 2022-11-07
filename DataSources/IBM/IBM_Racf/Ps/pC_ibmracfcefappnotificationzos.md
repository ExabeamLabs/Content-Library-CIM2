#### Parser Content
```Java
{
Name = ibm-racf-cef-app-notification-zos
  Vendor = IBM
  Product = IBM Racf
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """CEF:""", """Enterprise-IT-Security""", """ZOS""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d)\s+({host}\S+)""",
    """CEF:([^\|]*\|){4}({event_code}[^\|]+)\|({description}[^\|]+)\|""",
    """\sduser=(|({user}.+?))(\s+\w+=|\s*$)""",
    """\sduid=(|({user_id}.+?))(\s+\w+=|\s*$)""",
    """\ssuser=(|({user}.+?))(\s+\w+=|\s*$)""",
    """\sexternalID=(|({external_id}.+?))(\s+\w+=|\s*$)""",
    """\scat=(|({event_category}.+?))(\s+\w+=|\s*$)""",
    """\sfileId=(|({file_id}.+?))(\s+\w+=|\s*$)""",
    """\sfilePath=(|({file_path}.+?))(\s+\w+=|\s*$)""",
    """\scs3=(|({action}.+?))(\s+\w+=|\s*$)""",
    """\sdproc=(|({process_name}.+?))(\s+\w+=|\s*$)""",
    """\scs2=(|({result}.+?))(\s+\w+=|\s*$)""",
  ]


}
```