<template>
    <div class="contact-content">
        <div class="container">
            <div class="row">
                <div class="col-lg-7">
                    <div id="map" style="height: 500px; overflow: hidden;">
                        <iframe
                            src="https://www.google.com/maps/embed?pb=!1m17!1m12!1m3!1d3965.117759553162!2d2.41199257499168!3d6.378797093611543!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m2!1m1!2zNsKwMjInNDMuNyJOIDLCsDI0JzUyLjQiRQ!5e0!3m2!1sfr!2srw!4v1715683460045!5m2!1sfr!2srw"
                            width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy"
                            referrerpolicy="no-referrer-when-downgrade"></iframe>
                    </div>
                    <div class="row">
                        <div class="col-lg-6">
                            <div class="item phone">
                                <img src="/public/assets/images/phone-icon.png" alt="" style="max-width: 52px;">
                                <h6>+229 000000<br><span>Phone Number</span></h6>
                            </div>
                        </div>
                        <div class="col-lg-6">
                            <div class="item email">
                                <img src="/public/assets/images/email-icon.png" alt="" style="max-width: 52px;">
                                <h6> bus@reser.com<br><span>Business Email</span></h6>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-lg-5">
                    <form id="contact-form" action="" method="post">
                        <div class="row">
                            <div class="col-lg-12">
                                <fieldset>
                                    <label for="name">Nom complet</label>
                                    <input type="name" name="name" id="name" placeholder="Your Name..."
                                        autocomplete="on" required>
                                </fieldset>
                            </div>
                            <div class="col-lg-12">
                                <fieldset>
                                    <label for="email">Adresse email</label>
                                    <input type="text" name="email" id="email" pattern="[^ @]*@[^ @]*"
                                        placeholder="Your E-mail..." required="">
                                </fieldset>
                            </div>
                            <div class="col-lg-12">
                                <fieldset>
                                    <label for="subject">Objet</label>
                                    <input type="subject" name="subject" id="subject" placeholder="Subject..."
                                        autocomplete="on">
                                </fieldset>
                            </div>
                            <div class="col-lg-12">
                                <fieldset>
                                    <label for="message">Message</label>
                                    <textarea name="message" id="message" placeholder="Your Message"></textarea>
                                </fieldset>
                            </div>
                            <div class="col-lg-12">
                                <fieldset>
                                    <button type="submit" id="form-submit" class="orange-button">Send Message</button>
                                </fieldset>
                            </div>
                        </div>
                    </form>
                </div>
            </div>
        </div>
    </div>
</template>