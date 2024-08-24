<script>
    let generalEmail = "info@examplequiz.com";
    let supportEmail = "support@examplequiz.com";
    let feedbackEmail = "feedback@examplequiz.com";
    let phoneNumber = "[Your Phone Number]";
    let supportPhoneNumber = "[Support Phone Number]";
  
    let socialMedia = {
      facebook: "https://www.facebook.com/examplequiz",
      twitter: "https://twitter.com/examplequiz",
      instagram: "https://www.instagram.com/examplequiz",
    };
  
    let mailingAddress = {
      companyName: "[Your Company Name]",
      streetAddress: "[Street Address]",
      city: "[City]",
      state: "[State]",
      zipCode: "[ZIP Code]",
      country: "[Country]",
    };
  </script>
  
  <style>
    /* Add your custom styles here */
  </style>
  
  <main>
    <section>
      <h2>Contact Us</h2>
  
      <p>Thank you for your interest in our quiz! If you have any questions, concerns, or feedback, please feel free to reach out to us. We value your input and are here to assist you.</p>
  
      <h3>General Inquiries:</h3>
      <ul>
        <li>Email: <a href="mailto:{generalEmail}">{generalEmail}</a></li>
        <li>Phone: {phoneNumber}</li>
      </ul>
  
      <h3>Technical Support:</h3>
      <ul>
        <li>Email: <a href="mailto:{supportEmail}">{supportEmail}</a></li>
        <li>Phone: {supportPhoneNumber}</li>
      </ul>
  
      <h3>Feedback and Suggestions:</h3>
      <ul>
        <li>Email: <a href="mailto:{feedbackEmail}">{feedbackEmail}</a></li>
      </ul>
  
      <h3>Social Media:</h3>
      <ul>
        <li>Facebook: <a href="{socialMedia.facebook}" target="_blank">Facebook Page</a></li>
        <li>Twitter: <a href="{socialMedia.twitter}" target="_blank">Twitter</a></li>
        <li>Instagram: <a href="{socialMedia.instagram}" target="_blank">Instagram</a></li>
      </ul>
  
      <h3>Mailing Address:</h3>
      <p>
        {mailingAddress.companyName}<br>
        {mailingAddress.streetAddress}<br>
        {mailingAddress.city}, {mailingAddress.state} {mailingAddress.zipCode}<br>
        {mailingAddress.country}
      </p>
    </section>
  </main>
  