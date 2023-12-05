#### Parser Content
```Java
{
Name = secureauth-idp-kv-user-password-reset-fail-passwordreset
  ParserVersion = "v1.0.0"
  Conditions = [ """EventID="""", """ PasswordReset Exception: """, """RequestID=""", """BrowserSession=""", """PEN=""", """Appliance=""" ]
  DupFields = [ "additional_info->failure_reason" ]


}
```