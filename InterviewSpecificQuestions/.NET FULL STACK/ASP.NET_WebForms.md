## Technical

1. What are the events in Page life cycle? In whuch event are the controls fully loaded?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

All events of the page life cycle. But the main ones are given below:

- `Init` - This event fires after each control has been initialized.
- `Load` – All the controls are ready at this event.
- `PreRender` - Allows final changes to the page or its control.
- `Render` - The Render method generates the client-side HTML
- `Unload` - This event is used for cleanup code.

*In PAGE LOAD event controls are fully loaded.*

</blockquote>

</details>

---

2. What is the difference between `Server.Transfer()` and `Response.Redirect()`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

Both `Response.Redirect()` and `Server.Transfer()` methods are used to redirect the user's browser from one page to another page.

`Response.Redirect` uses round trip back to the client for redirecting the page.It is a slow technique, but it maintains the URL history in the client browser for all pages.

Suppose a client will send a request for Page1.aspx to the server. See this Page1.aspx present on the server. Now inside this Page1.aspx after some logic it has to be redirected to the Page2.aspx on some condition. So if you are using the `response.redirect`, then it will send the response back to the client and then it will again request the new page from the server. So, this is what we also call round trip, when you are going from position A to B and then you have to go to position C, for that you are coming back to position A and then going to position C, that is round trip which is not good and slow.

![Response_Redirect](https://github.com/revaturelabs/interviewquestions/blob/Feature/Kaveri-Revamped-IS-ques/InterviewSpecificQuestions/.NET%20FULL%20STACK/images/Response_Redirect.PNG)

In `Server.Transfer` page processing transfers from one page to the other page WITHOUT MAKING A ROUND-TRIP BACK to the client's browser. It is a faster technique, but it does not maintain the URL history in the client 
browser for all pages.In case of Server.Transfer transfer from Page1 to 2 will be direct without going back to the client like this. So it does not require round trip and hence very fast.

![Server_Transfer](https://github.com/revaturelabs/interviewquestions/blob/Feature/Kaveri-Revamped-IS-ques/InterviewSpecificQuestions/.NET%20FULL%20STACK/images/Server_Transfer.PNG)

</blockquote>

</details>

---

3. Write code to send E-Mail from an ASP.Net Application?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

``` C#

MailMessage mailMess = new MailMessage ();
mailMess.From = "abc@gmail.com";
mailMess.To = "xyz@gmail.com";
mailMess.Subject = "Test email";
mailMess.Body = "Hi This is a test mail.";
SmtpMail.SmtpServer = "localhost";
SmtpMail.Send (mailMess);

```

MailMessage and SmtpMail are classes defined `System.Web.Mail` namespace.

</blockquote>

</details>

---

4. What is CROSS PAGE POSTING?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

When we click submit button on a web page, the page post the data to the same page. The technique in which we post the data to different pages is called Cross Page posting. This can be achieved by setting POSTBACKURL property of the button that causes the postback. Findcontrol method of PreviousPage can be used to get the posted values on the page to which the page has been posted.

</blockquote>

</details>

---





