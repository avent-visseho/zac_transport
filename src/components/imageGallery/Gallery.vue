<template>
    <div id="gallery">
        <div class="container">
            <div class="gallery-content">
                <div ref="slider" class="slider">
                    <!-- one -->
                    <div class="slides" style="--img:url('/public/assets/zacImages/b1.jpeg')">
                        <div class="content">
                            <h2>Welcome ...</h2>
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Qui est tempore quos id
                                consequuntur. Totam dolores culpa aliquam eum, tempore error enim nostrum corporis omnis
                                accusantium perspiciatis repellendus cum consequuntur.</p>
                        </div>
                    </div>
                    <!-- one -->
                    <div class="slides" style="--img:url('/public/assets/zacImages/b4.jpeg')">
                        <div class="content">
                            <h2>Welcome ...</h2>
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Qui est tempore quos id
                                consequuntur. Totam dolores culpa aliquam eum, tempore error enim nostrum corporis omnis
                                accusantium perspiciatis repellendus cum consequuntur.</p>
                        </div>
                    </div>
                    <!-- one -->
                    <div class="slides" style="--img:url('/public/assets/zacImages/b3.jpeg')">
                        <div class="content">
                            <h2>Welcome ...</h2>
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Qui est tempore quos id
                                consequuntur. Totam dolores culpa aliquam eum, tempore error enim nostrum corporis omnis
                                accusantium perspiciatis repellendus cum consequuntur.</p>
                        </div>
                    </div>
                    <!-- one -->
                    <div class="slides" style="--img:url('/public/assets/zacImages/b5.jpeg')">
                        <div class="content">
                            <h2>Welcome ...</h2>
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Qui est tempore quos id
                                consequuntur. Totam dolores culpa aliquam eum, tempore error enim nostrum corporis omnis
                                accusantium perspiciatis repellendus cum consequuntur.</p>
                        </div>
                    </div>
                    <!-- one -->
                    <div class="slides" style="--img:url('/public/assets/zacImages/b6.jpeg')">
                        <div class="content">
                            <h2>Welcome ...</h2>
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Qui est tempore quos id
                                consequuntur. Totam dolores culpa aliquam eum, tempore error enim nostrum corporis omnis
                                accusantium perspiciatis repellendus cum consequuntur.</p>
                        </div>
                    </div>
                    <!-- one -->
                    <div class="slides" style="--img:url('/public/assets/zacImages/b8.jpeg')">
                        <div class="content">
                            <h2>Welcome ...</h2>
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Qui est tempore quos id
                                consequuntur. Totam dolores culpa aliquam eum, tempore error enim nostrum corporis omnis
                                accusantium perspiciatis repellendus cum consequuntur.</p>
                        </div>
                    </div>
                </div>
                <div class="buttons">
                    <span @click="nextSlide" class="next"></span>
                    <span @click="prevSlide" class="prev"></span>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue';

const slider = ref(null);

const nextSlide = () => {
    if (slider.value) {
        const slides = slider.value.querySelectorAll('.slides');
        slider.value.appendChild(slides[0]);
        console.log('bonjour');
    }
};

const prevSlide = () => {
    if (slider.value) {
        const slides = slider.value.querySelectorAll('.slides');
        slider.value.insertBefore(slides[slides.length - 1], slides[0]);
        console.log('bonjour');
    }
};

onMounted(() => {
    const next = document.querySelector('.next');
    const prev = document.querySelector('.prev');

    if (next && prev) {
        next.addEventListener('click', nextSlide);
        prev.addEventListener('click', prevSlide);
    }

    const interval = setInterval(nextSlide, 3000); // Change slide every 10 seconds

    onBeforeUnmount(() => {
        clearInterval(interval); // Clean up the interval when the component is unmounted
    });
});
</script>

<style scoped>
#gallery {
    margin: 65px 0;
}

.gallery-content {
    /* position: static; */
    height: 800px;
    overflow: hidden;
    display: flex;
    justify-content: center;
    align-items: center;
}

.slider {
    position: absolute;
    inset: 80px 200px 80px 80px;
    background-color: #ccc;
}

.slider .slides {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    width: 240px;
    height: 320px;
    border-radius: 20px;
    background: var(--img);
    transition: 0.5s;
    background-position: center;
    background-size: cover;
    box-shadow: 0 25px 50px rgba(0, 0, 0, 0.5);
    display: flex;
    align-items: flex-end;
    justify-content: flex-start;
}

.slider .slides:nth-child(1),
.slider .slides:nth-child(2) {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    box-shadow: 0 25px 50px rgba(0, 0, 0, 0);
    background-size: cover;
    transform: translateY(0);
}

.slider .slides:nth-child(3) {
    left: calc(50% + 240px);
    background-size: cover;
}

.slider .slides:nth-child(4) {
    left: calc(50% + 500px);
    background-size: cover;
}

.slider .slides:nth-child(5) {
    left: calc(50% + 760px);
    background-size: cover;
}

.slider .slides:nth-child(6) {
    left: calc(50% + 1020px);
    background-size: cover;
    opacity: 0;
}

.buttons {
    position: absolute;
    bottom: 15px;
    display: flex;
    gap: 20px;
}

.buttons span {
    position: relative;
    width: 50px;
    height: 50px;
    background-color: #111;
    cursor: pointer;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 50%;
}

.buttons span::before {
    content: "";
    position: absolute;
    width: 15px;
    height: 15px;
    border-top: 4px solid #fff;
    border-bottom: 4px solid #fff;
    transform: rotate(315deg) translate(2px, 2px);
}

.buttons span:nth-child(2)::before {
    transform: rotate(135deg) translate(2px 2px);
}

.buttons span:active {
    opacity: 0.5;
}

.content {
    position: relative;
    padding: 40px;
    max-width: 600px;
    transition: 0.25s;
    transition-delay: 0s;
    transform: translateY(40px);
    z-index: 10000;
    opacity: 0;
}

.slider .slides:nth-child(1) .content,
.slider .slides:nth-child(2) .content {
    opacity: 1;
    transform: translateY(0);
}

.content h2{
    font-size: 42px;
}

.content h2,p{
    color: #fff;
    font-weight: bold;
}

/* responsivité */

@media screen and (max-width: 900px) {
    .slider {
        position: absolute;
        inset: 40px 40px 200px 40px;
    }

    .slider .slides {
        width: 100px;
        height: 100px;
        top: initial;
        bottom: -17 0px;
    }

    .slider .slides:nth-child(1),
    .slider .slides:nth-child(2) {
        top: initial;
        bottom: 0;
    }

    .slider .slides:nth-child(3) {
        left: 0;
    }

    .slider .slides:nth-child(4) {
        left: 120px;
    }

    .slider .slides:nth-child(5) {
        left: 240px;
    }

    .slider .slides:nth-child(6) {
        left: 360px;
    }
}
</style>