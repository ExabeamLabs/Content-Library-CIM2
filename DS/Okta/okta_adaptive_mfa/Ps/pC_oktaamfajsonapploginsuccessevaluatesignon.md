#### Parser Content
```Java
{
Name = okta-amfa-json-app-login-success-evaluatesignon
  Vendor = Okta
  Product = Okta Adaptive MFA
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"eventType"""", """"policy.evaluate_sign_on"""", """policyType""" ]
  Fields = [
    """"published"+:"+({time}[^",]+)"+""",
    """"+actor"+:\{[^\{\}]*?"+alternateId"+:"+(system@okta\.com|({email_address}[^@]+@({domain}[^\.]+\.[^",]+))|(unknown|({user}[^",]+)))"+,""",
    """"+actor"+:\{[^\{\}]*?"+displayName"+:"+(Okta System|Okta Admin|unknown|({full_name}[^",]+))"+,""",
    """"policyType"+:"+({alert_type}[^",]+)""",
    """"eventType"+:"+({operation}[^",]+)""",
    """"+result"+:"+({result}[^",]+)"+,""",
    """"reason"+:"+({additional_info}[^",]+)"+""",
    """"severity"+:"+({alert_severity}[^",]+)"+""",
    """"+userAgent"+:(null|"+({user_agent}[^",]+))"+""",
    """"outcome"+:[^\]]*?"+result"+:"+FAILURE"+,"+reason"+:"+({failure_reason}[^"]+)"+""",
    """({app}(O|o)kta)"""
    """"type"+:"+AppInstance"+[^\}\]]*"displayName"+:"+({app}[^"]+?)\s*""""
  ]
  ParserVersion = "v1.0.0"
  DupFields = ["operation->event_name", "app->object"]


}
```