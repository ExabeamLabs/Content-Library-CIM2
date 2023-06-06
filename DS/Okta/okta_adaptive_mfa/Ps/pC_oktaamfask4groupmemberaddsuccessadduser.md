#### Parser Content
```Java
{
Name = okta-amfa-sk4-group-member-add-success-adduser
  Vendor = Okta
  Product = Okta Adaptive MFA
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"eventType":"group.user_membership.add"""", """"Add user to group membership"""", """"actor":""", """"alternateId":"""" ]
  Fields=[
    """"published":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}Z)""",
    """"actor":\{[^\}]*?("type":"User",)?"alternateId":"(({email_address}[^@"]+@[^"]+)|({user}[^"]+))"""",
    """"actor":\{[^\}]*?("type":"User"[^\}]*?)?"displayName":"(Okta System|({full_name}({first_name}[^"]+?)\s({last_name}[^"\s]+)))"""",
    """"type":"User".*?"displayName":"({group_name}[^"]+)".*?"id":"({group_id}[^"]+)".*?"type":"UserGroup"""",
    """\{"id":"({group_id}[^"]+)","type":"UserGroup"[^\}]*?"displayName":"({group_name}[^"]+)"""",
    """"target":\[[^\]]*?("type":"User",)?"alternateId":"({account_id}[^"]+)"""",
    """"target":\[[^\]]*?("type":"User",)?"alternateId":"(({dest_email_address}[^@"]+@[^"]+)|({dest_user}[^"]+))"""",
    """"ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"ipAddress":"?(null|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?),?"?""",
    """"outcome":\{"result":"({result}[^"]+)"""",
    """duser=({dest_user}[^\s]+)\s*""",
    """"target(s)?":[^\]]+?"displayName":"({member}[^",]+)[^\]\}]+?("type":"User")?"""
  ]
  ParserVersion = "v1.0.0"


}
```