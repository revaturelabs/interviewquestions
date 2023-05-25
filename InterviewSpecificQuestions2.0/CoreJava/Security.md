## Technical

1. How does Java process the JWT?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Java can process JWT (JSON Web Token) by decoding the JWT to extract the claims and verifying the signature to ensure that the token has not been tampered with. Java provides several libraries and frameworks for processing JWT, such as JJWT, Nimbus JOSE + JWT, and Apache Shiro. To process a JWT in Java, the code typically involves extracting the token from the HTTP header or request parameter, verifying the token signature using a secret key, and then parsing the token payload to obtain the claims. Once the claims are obtained, they can be used to authorize and authenticate the user.

</blockquote>

</details>

---

2. What is JWT authentication? 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

JWT authentication is a method of authentication that uses JSON Web Tokens (JWTs) to authenticate users. The JWT contains encoded information about the user, such as their identity and roles, and is used to verify their authenticity when they attempt to access a protected resource or endpoint. The authentication process involves exchanging a user's credentials (such as username and password) for a JWT, which is then sent with each subsequent request to the server to verify the user's identity.

</blockquote>

</details>

---

3. What is OAuth?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

OAuth (Open Authorization) is an open standard protocol used for secure and delegated access to sensitive data by allowing users to grant third-party applications access to their resources without sharing their credentials. It provides a secure, token-based mechanism to authenticate and authorize users to access web applications and services. OAuth is widely used by major tech companies such as Google, Facebook, and Twitter, among others.

</blockquote>

</details>

---

4. How to find the JWT expiration date?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The expiration date of a JWT is typically included as one of the claims within the JWT payload. This claim is known as "exp" and its value is a Unix timestamp that represents the expiration date and time of the token.

To find the expiration date of a JWT, you can decode the JWT payload and retrieve the "exp" claim. Once you have the Unix timestamp, you can convert it to a human-readable date and time using a programming language's built-in date/time functions.

Alternatively, some JWT libraries may provide helper methods that allow you to easily retrieve the expiration date from a decoded JWT.
