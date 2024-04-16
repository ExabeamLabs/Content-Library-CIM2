#### Parser Content
```Java
{
Name = manageengine-adssp-cef-user-unlock-success-unlockaccountsuccess
  ParserVersion = v1.0.0
  Conditions= [ """CEF:0|ManageEngine|ADSSP|""", """dvchost""", """DATE_TIME""", """ACTION_NAME\=Unlock Account Attempt""", """STATUS\=Success""" ]
  DupFields = [ "user->dest_user" ]


}
```