#### Parser Content
```Java
{
Name = github-g-sk4-repository-create-success-github
  ParserVersion = v1.0.0
  Vendor = GitHub
  Product = GitHub
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """CEF:""", """destinationServiceName =GitHub""", """"type":"""" ]
  Fields = [
    """"created_at":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""",
    """"display_login":"({user}[^"]+)"""",
    """"type":"({operation}[^"]+?)(?:Event|)"""",
    """\WrequestClientApplication=({app}[^=]+?)\s*(\w+=|$)""",
    """"repo":[^}]+?"name":"({resource}[^"]+)"""",
    """"repo":[^}]+?"name":"({object}[^"]+)"""",
    """\Wfname=({object}[^=]+?)\s*(\w+=|$)""",
    """\WfileType=({additional_info}[^=]+?)\s*(\w+=|$)""",
    """\Wmsg=({additional_info}[^=]+?)\s*(\w+=|$)""",
  ]


}
```