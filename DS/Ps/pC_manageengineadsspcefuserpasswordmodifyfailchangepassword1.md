#### Parser Content
```Java
{
Name = manageengine-adssp-cef-user-password-modify-fail-changepassword-1
  ParserVersion = v1.0.0
  Conditions= [ """CEF:0|ManageEngine|ADSSP|""", """dvchost""", """DATE_TIME""", """ACTION_NAME\=Change Password""", """STATUS\=The specified password does not meet the password policy""" ]
  DupFields = [ "user->dest_user" ]


}
```