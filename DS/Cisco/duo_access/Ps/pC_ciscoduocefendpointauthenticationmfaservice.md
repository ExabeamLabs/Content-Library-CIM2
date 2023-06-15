#### Parser Content
```Java
{
Name = cisco-duo-cef-endpoint-authentication-mfaservice
  Vendor = Cisco
  Product = Duo Access
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Duo|MFA Service|""", """reason=""", """|authentication-factor-executed|""" ]
  Fields = [
    """\Wrt=({time}\d{13})""",
    """\Wreason=({failure_reason}.+?)(\s+\w+=|\s*$)""",
    """\Woutcome=({action}.+?)(\s+\w+=|\s*$)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wduser=({user}.+?)(\s+\w+=|\s*$)""",
    """\Wdvchost=({host}.+?)(\s+\w+=|\s*$)""",
    """\Wcs4=({os}.+?)(\s+\w+=|\s*$)""",
    """\Wshost=({src_host}.+?)(\s+\w+=|\s*$)""",
    """\WrequestClientApplication=({user_agent}.+?)(\s+\w+=|\s*$)""",
    """\WflexString1=(?:n\/a|({factor}.+?))(\s+\w+=|\s*$)""",
    """\Wcs6=({new_enrollment}.+?)(\s+\w+=|\s*$)""",
  ]
  ParserVersion = "v1.0.0"


}
```