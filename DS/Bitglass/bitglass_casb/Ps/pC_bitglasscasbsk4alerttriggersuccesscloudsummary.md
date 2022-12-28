#### Parser Content
```Java
{
Name = bitglass-casb-sk4-alert-trigger-success-cloudsummary
    Product = Bitglass CASB
    Vendor = Bitglass
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Conditions = ["""security-threat-detected|""", """cn1Label=Is Violating""", """dproc=cloudsummary"""]
    Fields = [
      """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
      """\sproto=({alert_name}.+?)(\s+\w+=|\s*$)""",
      """\sproto=({alert_type}.+?)(\s+\w+=|\s*$)""",
      """\ssourceServiceName =({app}.+?)(\s+\w+=|\s*$)""",
      """\sduser=({target}.+?)(\s+\w+=|\s*$)""",
      """\sduser=({object}.+?)(\s+\w+=|\s*$)""",
      """\ssuser=({email_address}[^@=]+@[^@=]+?)(\s+\w+=|\s*$)""",
      """\ssuser=({user}[^@]+?)(\s+\w+=|\s*$)""",
      """\sfname=\s*({additional_info}.+?)(\s+\w+=|\s*$)""",
      """\sfname=\s*({file_name}.+?(\.({file_ext}[^\.\s]+))?)\s+(\w+=|$)""",
      """\sfileType=({file_type}.+?)(\s+\w+=|\s*$)""",
      """\sfsize=({bytes}\d+)(\s+\w+=|\s*$)""",
      """\sstatus=({alert_type}.+?)(\s+\w+=|\s)""",
    ]
  ParserVersion = "v1.0.0"
  

}
```