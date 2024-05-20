<template>
    <div id="portfolio" class="our-portfolio section">
        <div class="container">
            <div class="row">
                <div class="col-lg-6 offset-lg-3">
                    <div class="section-heading  wow bounceIn" data-wow-duration="1s" data-wow-delay="0.2s">
                        <h2>Voir ce que nous <em id="lineare">proposons</em></h2>
                    </div>
                </div>
            </div>
            <div class="row">
                <div class="col-lg-3 col-sm-6">
                    <a href="#">
                        <div class="item wow bounceInUp" data-wow-duration="1s" data-wow-delay="0.3s">
                            <div class="hidden-content">
                                <h4>Location</h4>
                                <p>Louer une voiture offre la liberté de voyager à son propre rythme.</p>
                            </div>
                            <div class="showed-content">
                                <h4>Location des Véhicules</h4>
                            </div>
                        </div>
                    </a>
                </div>
                <div class="col-lg-3 col-sm-6">
                    <a href="#">
                        <div class="item wow bounceInUp" data-wow-duration="1s" data-wow-delay="0.4s">
                            <div class="hidden-content">
                                <h4>Livraison</h4>
                                <p>Notre service de livraison de colis garantit rapidité et fiabilité.</p>
                            </div>
                            <div class="showed-content">
                                <h4>Livraison de Colis</h4>
                            </div>
                        </div>
                    </a>
                </div>
                <div class="col-lg-3 col-sm-6">
                    <a href="#">
                        <div class="item wow bounceInUp" data-wow-duration="1s" data-wow-delay="0.5s">
                            <div class="hidden-content">
                                <h4>Réservation</h4>
                                <p>Réservez votre ticket de voyage en ligne pour un départ en toute sérénité.</p>
                            </div>
                            <div class="showed-content">
                                <h4>Réservation de Ticket</h4>
                            </div>
                        </div>
                    </a>
                </div>
                <div class="col-lg-3 col-sm-6">
                    <a href="#">
                        <div class="item wow bounceInUp" data-wow-duration="1s" data-wow-delay="0.6s">
                            <div class="hidden-content">
                                <h4>Carte de fidélité</h4>
                                <p>
                                <p>zac-GOLD, zac-PLATINIUM,Carte de fidélité VIP</p>
                                </p>
                            </div>
                            <div class="showed-content">
                                <h4>Carte de fidélité VIP</h4>
                            </div>
                        </div>
                    </a>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
/* 
---------------------------------------------
Portfolio
--------------------------------------------- 
*/

.our-portfolio {
    padding-top: 120px;
    margin-top: 0px;
}

.our-portfolio .section-heading h2 {
    text-align: center;
    margin: 0px 90px 0px 90px;
    margin-bottom: 120px;
    position: relative;
    z-index: 1;
}

.our-portfolio .item {
    position: relative;
}

.our-portfolio .item:hover .hidden-content {
    top: -100px;
    opacity: 1;
    visibility: visible;
}

.our-portfolio .item:hover .showed-content {
    top: 90px;
}

#lineare {
    color: red;
}

.our-portfolio .hidden-content {
    background: rgb(255, 77, 30);
    background: #2f2f80;
    padding: 30px;
    border-radius: 20px;
    text-align: center;
    opacity: 0;
    top: 0;
    visibility: hidden;
    position: absolute;
    z-index: 2;
    transition: all 0.5s;
}

.our-portfolio .hidden-content:after {
    width: 20px;
    height: 20px;
    position: absolute;
    background: rgb(255, 77, 30);
    content: '';
    left: 50%;
    bottom: -8px;
    margin-left: -5px;
    transform: rotate(45deg);
    background: #2f2f80;
    z-index: -1;
}

.our-portfolio .hidden-content h4 {
    font-size: 20px;
    font-weight: 700;
    color: #fff;
    margin-bottom: 20px;
}

.our-portfolio .hidden-content p {
    color: #fff;
}

.our-portfolio .showed-content {
    top: 0px;
    position: relative;
    z-index: 3;
    background-color: #fff;
    text-align: center;
    padding: 50px;
    border-radius: 20px;
    box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
    transition: all 0.5s;
}

.our-portfolio .showed-content img {
    max-width: 100px;
}


@media (max-width: 992px) {

    .our-portfolio .section-heading h2 {
        margin: 0px 0px 80px 0px;
    }

    .our-portfolio .item {
        margin-bottom: 15px;
    }
}
</style>