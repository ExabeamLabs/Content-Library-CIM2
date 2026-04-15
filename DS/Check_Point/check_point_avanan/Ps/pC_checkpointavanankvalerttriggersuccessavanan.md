#### Parser Content
```Java
{
Name = checkpoint-avanan-kv-alert-trigger-success-avanan
  ParserVersion = v1.0.0
  Conditions = [ """ Avanan """ , """action:""" ,"""severity:""" ]
  Vendor = Check Point
  Product = Check Point Avanan
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """\d\d:\d\d:\d\d.\d\d\d\d\d\d\s({host}[\w\-\.]+)"""
    """event_type:\s*({alert_name}[^";]+)"""
    """maliciouscontent:\s*({additional_info}[^;]+)"""
    """email_subject:\s*({email_subject}[^";]+)"""
    """verdict:\s*({alert_type}[^;]+)"""
    """resource:\s*({resource}[^";]+)"""
    """\sproduct:\s({product_name}[^;]+)"""
    """user:\s*(({first_name}[^\s,;]+)\s+({last_name}[^,\(;]+?);|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """\saction:\s({action}[^;]+);"""
    """rule_id:\s*({rule_id}[^;]+);"""
    """severity:\s*({alert_severity}[^;]+)"""
    """email_message_id:\s*({message_id}({alert_id}[^;]+))"""
    """\sreply_to:\s({reply_to}[\w\.\-\+@]+);"""
  ]


}
```