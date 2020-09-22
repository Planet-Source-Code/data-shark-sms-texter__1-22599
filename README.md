<div align="center">

## SMS Texter


</div>

### Description

The Code will Login to Breathe.com, An SMS Based Web Site which allows it's users to send SMS Message to mobile phones throughout the UK.

( Please RATE this code )
 
### More Info
 
You will need 4 Text Boxes: txtnumber, txtmsg,txtpass & txtlogin.

2 Command Buttons: Cmdsendmessage & Cmdreset

1 Timer: Timer1

1 Web Browser: Webbrowser1


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Data Shark](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/data-shark.md)
**Level**          |Beginner
**User Rating**    |4.7 (14 globes from 3 users)
**Compatibility**  |VB 4\.0 \(32\-bit\), VB 5\.0, VB 6\.0
**Category**       |[Internet/ HTML](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/internet-html__1-34.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/data-shark-sms-texter__1-22599/archive/master.zip)





### Source Code

```
Private Sub cmdSendMessage_Click()
If txtlogin.Text <> "" And txtpass.Text <> "" Then
 login = "http://www.breathe.com/cgi-bin/login.cgi?&extension-attribute-11=" & txtlogin.Text & "&extension-attribute-12=" & txtpass.Text & "&SUBMIT"
 WebBrowser1.Navigate login
 Timer1.Enabled = True
 Else
 End If
End Sub
Private Sub cmdReset_Click()
txtlogin.Text = ""
txtpass.Text = ""
txtnumber.Text = ""
txtmsg.Text = ""
End Sub
Private Sub Timer1_Timer()
 If WebBrowser1.LocationURL = "http://www.breathe.com/?loggedin" Then
 message = "http://www.breathe.com/services/textmessaging.html?number=" & txtnumber.Text & "&message=" & txtmsg.Text & "&charleft=113%2F146&submit.x=19&submit.y=7"
 WebBrowser1.Navigate2 message
 Timer1.Enabled = False
 End If
End Sub
```

