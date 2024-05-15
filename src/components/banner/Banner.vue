<template>
    <div class="banner" id="banner">
        <div class="banner-shadow">
            <div class="container">
                <div class="banner-content">
                    <div class="content">
                        <div class="content-box">
                            <h1>Réserver votre place <br> <span id="reserveColor">Voyager en toute sécurité</span></h1>
                            <p>Envie de voyager sur Parakou ? ZAC Transport vous emmène grâce à son vaste réseau de
                                lignes
                                de bus ! Nos billets de bus pas chers vous permettent de voyager facilement et à petit
                                prix
                                où vous voulez, pour le travail ou pour vous évader.</p>
                            <div class="btn-content">
                                <button>voir plus</button>
                            </div>
                        </div>
                    </div>

                </div>
            </div>
            <!--             <div class="container">
                <AbsolutReserveForm />
            </div> -->

          <!--   <div class="banner_content_reservation">
                <div class="baner_content_reservation_content">
                    <form action="" id="reservation_content">
                        <div class="input-group">
                            <label for="#">Aller - Retour</label>
                            <select name="" id="">
                                <option value="Cotonou">Cotonou</option>
                                <option value="Ouidah">Ouidah</option>
                                <option value="Porto-Novo">Porto-Novo</option>
                                <option value="Abomey">Abomey</option>
                            </select>
                        </div>
                        <div class="input-group">
                            <label for="#">Départ de</label>
                            <input type="text" name="startDate" id="startDate" placeholder="depart">
                        </div>
                        <div class="input-group">
                            <label for="#">Arrivée à</label>
                            <input type="text" name="endDate" id="date" placeholder="arrivé">
                        </div>
                        <div class="input-group">
                            <label for="#">Date de voyage</label>
                            <input type="date" name="endDate" id="date">
                        </div>
                        <div class="input-group" style="display: flex; align-items: center;">
                            <button id="submit"><span class="mdi mdi-send"></span></button>
                        </div>
                    </form>
                </div>
            </div> -->
        </div>
    </div>
</template>


<style scoped>
.banner {
    height: calc(100vh - 150px);
    background-image: url('/public/assets/images/bg1.jpeg');
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
}

.banner-shadow {
    background-color: rgba(10, 10, 131, 0.514);
    height: calc(100vh - 150px);
}

.content {
    display: flex;
    height: calc(100vh - 150px);
    align-items: center;
}

.content-box {
    width: 800px;
}

.content-box h1 {
    color: #fff;
    font-size: 54px;
    font-weight: bold;
    line-height: 1.4;
}

.content-box p {
    color: #ffffffa4;
    font-size: 18px;
    line-height: 1.4;
    margin-top: 15px;
}

#reserveColor {
    color: #f35525;
}

.btn-content {
    margin-top: 35px;
}

.btn-content button {
    padding: 15px 35px;
    border: none;
    border-radius: 4px;
    outline: none;
    font-size: 18px;
    cursor: pointer;
}

.btn-content button:hover {
    background-color: #f35525;
    color: #fff;
}




/* form  */

.banner_content_reservation {
    position: absolute;
    bottom: -20pX;
    transform: translateY(50px);
    border-radius: 9px;
    left: 50%;
    transform: translate(-50%);
    background-color: #fff;
    box-shadow: rgba(0, 0, 0, 0.15) 0px 5px 15px 0px;
}

.baner_content_reservation_content {
    padding: 35px;
    display: flex;
    /*    height: 80px; */
    align-items: center;
}

form#reservation_content {
    display: flex;
    gap: 25px;
}

form#reservation_content label {
    display: block;
}

.reservation_content select,
.reservation_content input {
    display: block;
    padding: 15px 25px;
}

#reservation_content select,
#reservation_content input {
    width: 200px;
    padding: 10px 15px;
    outline: none;
    border-radius: 4px;
    border: solid 2px orangered;
}

#reservation_content #submit {
    width: 40px;
    height: 40px;
    border-radius: 50%;
    cursor: pointer;
    outline: none;
    border: none;
    background: linear-gradient(105deg, rgba(255, 77, 30, 1) 0%, rgba(255, 44, 109, 1) 100%);
}

#reservation_content #submit .mdi-send {
    font-size: 23px;
    color: #fff;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}

@media (max-width : 794px) {
    form#reservation_content {
        display: flex;
        width: 100%;
        flex-direction: column;
        gap: 25px;
    }

    .banner_content_reservation {
        position: absolute;
        bottom: -20pX;
        width: 80%;
        width: 80%;
        background-color: #fff;
        box-shadow: rgba(0, 0, 0, 0.15) 0px 5px 15px 0px;
    }

    #reservation_content select,
    #reservation_content input {
        width: 100%;
    }

    .banner_content_linear_gradient h2 {
        font-size: 3em;
        padding-bottom: 101px;
    }
}
</style>