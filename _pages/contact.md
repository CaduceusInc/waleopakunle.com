---
title: "Contact"
layout: default
permalink: "/contact"
---

<form action="https://formspree.io/{{site.email}}" method="POST">    
    <p class="mb-4">Quick small favor: </p>
    <p class="mb-4">Have you spotted an error I made in my post bants?
                    Do you have suggestions on which papers you would like reviewed next? Would you like to collaborate on a deep learning project?
    <p class="mb-4">Please send your message to {{site.email}} and I will reply as soon as possible!</p>
    <div class="form-group row">
    <div class="col-md-6">
    <input class="form-control" type="text" name="name" placeholder="Name*" required>
    </div>
    <div class="col-md-6">
    <input class="form-control" type="email" name="_replyto" placeholder="E-mail Address*" required>
    </div>
    </div>
    <textarea rows="8" class="form-control mb-3" name="message" placeholder="Message*" required></textarea>    
    <input class="btn btn-success" type="submit" value="Send">

    <p class="mb-3"> </p>

    <p class="mb-3"> Thank you! I really value your feedback.</p>

</form>