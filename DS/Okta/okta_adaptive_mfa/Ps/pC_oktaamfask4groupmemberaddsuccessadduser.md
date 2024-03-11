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
    """"actor":\{[^\}]*?"type":"User","alternateId":"(({email_address}[^@"]+@[^"]+)|({user}[^"]+))"""",
    """"actor":\{[^\}]*?"type":"User"[^\}]*?"displayName":"({full_name}({first_name}[^"]+?)\s({last_name}[^"\s]+))"""",
    """"type":"UserGroup"[^\}]*?"displayName":"({group_name}[^"]+)"""",
    """"target":\[[^\]]*?"type":"User","alternateId":"({account_id}[^"]+)"""",
    """"target":\[[^\]]*?"type":"User","alternateId":"(({target_user_email}[^@"]+@[^"]+)|({dest_user}[^"]+))"""",
    """"ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"outcome":\{"result":"({result}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```