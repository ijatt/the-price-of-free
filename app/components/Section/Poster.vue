<template>
  <section id="gallery" class="py-10">
    <div class="text-center mb-10">
      <h3 class="text-3xl font-bold text-purple">Awareness Poster</h3>
    </div>
    <div class="mt-6 flex justify-center">
      <div class="swiper awarenessSwiper w-full max-w-5xl">
        <div class="swiper-wrapper">
          <!-- Slide 1 -->
          <div class="swiper-slide flex justify-center">
            <div class="poster-frame">
              <img src="assets/img/p1.png" alt="" />
            </div>
          </div>

          <!-- Slide 2 -->
          <div class="swiper-slide flex justify-center">
            <div class="poster-frame">
              <img src="assets/img/p2.png" alt="" />
            </div>
          </div>

          <!-- Slide 3 -->
          <div class="swiper-slide flex justify-center">
            <div class="poster-frame">
              <img src="assets/img/p3.png" alt="" />
            </div>
          </div>
        </div>

        <!-- Pagination -->
        <div class="swiper-pagination mt-4"></div>

        <!-- Navigation arrows -->
        <div class="swiper-button-next"></div>
        <div class="swiper-button-prev"></div>
      </div>
    </div>
  </section>
</template>

<script lang="ts" setup>
import Swiper from "swiper";
import "swiper/swiper-bundle.css";
import { Navigation, Pagination } from "swiper/modules";

onMounted(() => {
  new Swiper(".awarenessSwiper", {
    modules: [Navigation, Pagination],
    slidesPerView: 1,
    spaceBetween: 20,
    loop: true,
    pagination: { el: ".swiper-pagination", clickable: true },
    navigation: {
      nextEl: ".swiper-button-next",
      prevEl: ".swiper-button-prev",
    },
  });
});
</script>

<style>
.awarenessSwiper {
  width: 100%;
  max-width: 500px; /* makes poster smaller */
  height: auto;
}

/* Make slides centered */
.awarenessSwiper .swiper-slide {
  display: flex;
  width: 250px;
  justify-content: center;
}

/* Limit poster height */
.awarenessSwiper img {
  width: 100%;
  height: 100%;
  object-fit: contain;
}

/* Make arrows clickable and visible */
.swiper-button-next,
.swiper-button-prev {
  z-index: 50 !important;
  color: #7c3aed;
  width: 40px;
  height: 40px;
  background: rgba(255, 255, 255, 0.8);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  top: 50% !important;
  transform: translateY(-50%);
}

.swiper-button-next:after,
.swiper-button-prev:after {
  font-size: 20px;
}

.swiper-button-next:hover,
.swiper-button-prev:hover {
  background: rgba(255, 255, 255, 1);
}
</style>
