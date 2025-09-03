#### Parser Content
```Java
{
Name = openshift-o-kv-app-activity-annotations
  Product = OpenShift
  Vendor = Open Shift
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [
    """apiVersion""",
    """responseStatus""",
    """annotations"""  ]
  Fields =[
    """"*uid\\?"*(=>|:)\\?"*({user_id}[^"\\]+)""",
    """"*sourceIPs\\?"*:\[\\?"*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"*username\\?"*(=>|:)\\?"*({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """"*groups\\?"*(=>|:)\[\\?"*({group_name}[^"\\]+)""",
    """"*authorization.k8s.io\/decision\\?"*(=>|:)\\?"*({action}[^\s"]+?)\\?"""",
    """hostname:({host}[^\s]+)""",
    """({time}\d+\-\d+\-\d+T\d\d:\d\d:\d\d\.\d+Z)""",
    """"*code\\?"*(=>|:)({result}\d+)""",
    """"*message"*=>"*({event_name}[^"]+)""",
    """"*userAgent\\?"*:\\?"*({user_agent}.+?)\s*kubernetes""",
    """xA8username\\xD9."*({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """xA3uid\\xD9.({user_id}[^\\]+)""",
    """xA6groups\\x93.xB6({group_name}[^\\]+)""",
    """xA9sourceIPs\\x91.xA3({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\\xA9userAgent""",
    """xA9userAgent\\xD9v({user_agent}[^\\]+)\skubernetes""",
    """xBDauthorization.k8s.io\/decision\\xA5({action}[^\\]+)""",
    """xA8hostname\\xB4({host}[^\\]+)""",
    """message\\xB7({event_name}[^\\]+)""",
    """resource\\xAE({object}[^\\]+)"""
    """operation":"({operation}[^"]+)"""
    """"resource\\?":\\?"({resource}[^"\\]+)""",
    ]
    DupFields = [ "resource->object" ]
  ParserVersion = "v1.0.0"


}
```