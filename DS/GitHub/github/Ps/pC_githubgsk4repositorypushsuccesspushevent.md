#### Parser Content
```Java
{
Name = github-g-sk4-repository-push-success-pushevent
  ParserVersion = "v1.0.0"
  Conditions = [ """CEF:""", """destinationServiceName =GitHub""", """"type":"PushEvent"""" ]

sk4-github-events = {
    Vendor = GitHub
    Product = GitHub
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
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
    
}
```