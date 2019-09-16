<template>
    <div>
        <div class="slider__container">
            <div class="swiper-container slider slider__back" ref="back_slider">
              <!-- Wrapper -->
              <div class="carousel__wrapper swiper-wrapper">
                <div v-for="slide in pictures2" :key="slide.id" class="swiper-slide">
                  <div class=""></div>
                  <div>
                    <img :src="slide.src" alt="">
                  </div>
                </div>
              </div>
            </div>
            <div class="swiper-container slider slider__top" ref="top_slider">
                <!-- Wrapper -->
                <div class="carousel__wrapper swiper-wrapper">
                    <div v-for="slide in pictures" :key="slide.id" class="swiper-slide">
                      <div>
                        <img :src="slide.src" alt="">
                      </div>
                    </div>
                </div>
            </div>
          <div class="navigation">
            <base-arrow-left @click.native="slidePrev" class="button navigation__button-prev"/>
            <base-arrow-right @click.native="slideNext" class="button navigation__button-next"/>
          </div>
        </div>
    </div>
</template>

<script>
    import Swiper from "swiper/dist/js/swiper.js";
    import "swiper/dist/css/swiper.min.css";
    import BaseArrowLeft from "./BaseArrowLeft";
    import BaseArrowRight from "./BaseArrowRight";
    export default {
        name: "MainSlider",
        data() {
            return {
                swiperTop: null,
                swiperBack: null,
                sliderTimeout: null,
                pictures:[
                    {
                        name: '1',
                        src: '/kaboompics_Arc.jpg'
                    },
                    {
                        name: '2',
                        src: '/kaboompics_Modern.jpg'
                    },
                    {
                        name: '3',
                        src: '/photo-153.jpg'
                    }
                ],
                pictures2:[
                    {
                        name: '2',
                        src: '/kaboompics_Modern.jpg'
                    },
                    {
                        name: '3',
                        src: '/photo-153.jpg'
                    },
                    {
                        name: '1',
                        src: '/kaboompics_Arc.jpg'
                    },

                ]
            }
        },
        components: {
            BaseArrowRight,
            BaseArrowLeft,
            Swiper
        },
        computed: {
            arrayReverse(){
                let reversedPictures = this.pictures.slice(0);
                return reversedPictures.reverse();
            },
            swiperTopOptions() {
                return {
                    spaceBetween: 0,
                    loop: true,
                    slidesPerView: 1,
                    centeredSlides: true,
                    centerInsufficientSlides: true,
                    allowTouchMove: false,
                    // navigation: {
                    //     nextEl: '.button-next',
                    //     prevEl: '.button-prev',
                    // },
                    //spaceBetween: this.spaceBetween,
                    // thumbs: {
                    //     swiper: this.swiperThumbs
                    // },
                    // autoplay: {
                    //     delay: this.delayTime,
                    //     disableOnInteraction: false
                    // },
                    speed: 1000,
                    control: this.swiperBack
                };
            },
            swiperBackOptions() {
                return {
                    spaceBetween: 0,
                    loop: true,
                    slidesPerView: 1,
                    centeredSlides: true,
                    centerInsufficientSlides: true,
                    allowTouchMove: false,
                    // navigation: {
                    //     nextEl: '.button-next',
                    //     prevEl: '.button-prev',
                    // },
                    //spaceBetween: this.spaceBetween,
                    // thumbs: {
                    //     swiper: this.swiperThumbs
                    // },
                    // autoplay: {
                    //     delay: this.delayTime,
                    //     disableOnInteraction: false
                    // },
                    speed: 500
                };
            }
        },
        methods: {
            mountInstance() {

                this.swiperTop = new Swiper(this.$refs.top_slider, this.swiperTopOptions);
                this.swiperBack = new Swiper(this.$refs.back_slider, this.swiperBackOptions);
            },
            slidePrev(){
                this.swiperTop.slideNext(700, false);
                setTimeout(()=>{
                    this.swiperBack.slideNext(700, false);
                }, 400);

            },
            slideNext(){
                console.log(123);
                this.swiperTop.slidePrev(700, false);
                setTimeout(()=>{
                    this.swiperBack.slidePrev(700, false);
                }, 400);
            }
        },
        mounted() {
            this.mountInstance();
            // this.swiperTop.on('slideChange', () => {
            //     if (this.sliderTimeout) {
            //         clearTimeout(this.sliderTimeout);
            //     }
            //
            //     this.sliderTimeout = setTimeout(() => {
            //         this.swiperBack.slideTo(this.swiperTop.activeIndex);
            //     }, 300);
            // });
        },
    }
</script>

<style lang="less" scoped>
  .navigation{
    position: absolute;
    display: flex;
    .button{
      cursor: pointer;
    }
    &__button-next{

    }
  }
  .slider{

    &__back{
      position: absolute;
      width: 80rem;
      height: 52.5rem;
    }
    &__top{
      width: 86rem;
      height: 49rem;
      padding-top: 10rem;
    }

  }
  .swiper{
    &-slide-prev{
      //transform: translate3d(880px, -52px, -60px) rotateX(0deg) rotateY(0deg);
    }

    &-slide{
      display: flex;
      justify-content: flex-end;
      img{
        width: 100%;
        height: 100%;
        object-fit: cover;
      }
      &::before{
        content: '';
        display: block;
        width: 100%;
        height: 100%;
        position: absolute;
        background: var(--color-yellow);
        opacity: .8;
      }
    }
  }
</style>
